from flask import Flask, request, render_template
import pickle

# Load model and vectorizer
model = pickle.load(open("model.pkl", "rb"))
vectorizer = pickle.load(open("vectorizer.pkl", "rb"))

app = Flask(__name__)

@app.route("/", methods=["GET", "POST"])
def home():
    prediction = ""
    
    if request.method == "POST":
        text = request.form["news_text"]
        text_transformed = vectorizer.transform([text])
        result = model.predict(text_transformed)[0]
        prediction = "REAL NEWS" if result == 1 else "FAKE NEWS"

    return render_template("index.html", prediction=prediction)

if __name__ == "__main__":
    app.run(debug=True)
