# ResumeMatchr 🧪

**A smart, lenient, student-friendly resume-to-job matcher built with Flask and LLMs.**

This lightweight web application takes a PDF resume and matches it against a curated list of job descriptions using an LLM-powered scoring function. It's designed to help students see how their resumes align with real-world roles, offering hope and clarity—without harsh judgment.

---

## ⚙️ Features

- Upload a PDF resume and select a country.
- Get scored job matches with soft color-coded visualization.
- Backed by OpenRouter's LLMs for nuanced understanding.
- Built with ❤️ for students. Every resume gets a fair chance.

---

## 🧠 How It Works

1. Extracts and cleans resume text using `PyMuPDF`.
2. Selects a random subset of job descriptions based on country.
3. Sends the resume + job description to an LLM for relevance scoring.
4. Boosts scores slightly for a more encouraging UX.
5. Visualizes results with HSL-colored confidence indicators.

---

## 🛠️ Installation

```yaml
clone repository
run cells to install dependencies
put your API key
Run app
```

Dependencies include:

- Flask
- PyMuPDF (`fitz`)
- OpenAI (for OpenRouter API)
- Gensim
- NumPy
- nest_asyncio

---

## 🔑 API Key

You **must** add your [OpenRouter API key](https://openrouter.ai/) to this line in `app.ipynb`:

```python
OPENROUTER_API_KEY = "your-api-key-here"
```

---

## 🚀 Usage

```yaml
Just run the app cell
```

A browser tab will auto-launch at `http://127.0.0.1:5000`. Upload your resume and select your region.

---

## 🌍 Country Matching

Each country determines how many job descriptions will be compared. Modify the `eu_countries` list to adjust:

```python
eu_countries = [
    {"name": "Europe", "value": 15},
    ...
]
```

---

## 📎 To-Do

- Load job descriptions dynamically
- Restore and fine-tune Doc2Vec fallback
- UI improvements & HTML templating
- More regions and job categories

---

## ⚠️ Disclaimer

This project is for educational and demo purposes. Be nice. Don't steal the API key.

---

## 📄 License

MIT — use freely, improve generously.

---

Let me know if you'd like a fancy project banner or additional setup scripts.
