# Weather Chatbot

A data-driven chatbot that answers weather questions, built in Python in a Jupyter notebook. It starts as a simple list-based bot and grows in four stages into a chatbot that loads its knowledge from a JSON file and uses natural language preprocessing (NLTK) to understand what the user types.

## How the Chatbot Was Built

The notebook builds the chatbot in four parts, each adding a new concept:

| Part | Concept | What it adds |
|------|---------|--------------|
| 1 | Lists, conditions and string concatenation | A simple bot that matches words against a fixed list of inputs and replies from a list of responses |
| 2 | Dictionaries and regular expressions | Pattern matching with regular expressions, modular functions, and remembering the user's name and favourite colour |
| 3 | File handling | Loading patterns and responses from `intents.json` and mapping patterns to intents and responses with dictionaries |
| 4 | Text preprocessing with NLTK | Cleaning user input (lowercasing, punctuation, stopwords) and applying stemming and lemmatization before matching |

## Final Chatbot Features

- Asks for your timezone and greets you with good morning, afternoon or evening.
- Asks for your name and location and uses them in its replies.
- Preprocesses what you type (lowercase, punctuation and stopword removal, tokenizing, lemmatizing) and matches it against the patterns in `intents.json`.
- Picks a random response from the matching intent, with your name and location filled in.
- Falls back to a polite "could you rephrase that?" when nothing matches.
- Type `bye` at any time to exit.

## Topics It Knows

The 12 intents in `intents.json`:

`greeting`, `goodbye`, `current_weather`, `weather_forecast`, `temperature_query`, `seasonal_weather`, `extreme_weather`, `weather_safety`, `climate_vs_weather`, `uv_index`, `humidity_conditions` and `air_quality`.

Each intent has a list of example patterns and a list of possible responses, so you can add new topics by editing the JSON file.

## Project Structure

| File | Purpose |
|------|---------|
| `weather-chatbot.ipynb` | The notebook with all four parts of the chatbot |
| `intents.json` | Patterns and responses for each intent |
| `WEATHER CHATBOT MID REPORT.pdf` | Project report |

## Run Locally

You need Python 3 and Jupyter.

```bash
git clone https://github.com/ayeshaatif07/Weather-Chatbot.git
cd Weather-Chatbot
pip install nltk pytz jupyter
jupyter notebook weather-chatbot.ipynb
```

Then:

1. Run the cells from top to bottom. The NLTK data (`punkt_tab`, `stopwords`, `wordnet`) downloads automatically in Part 4.
2. Run the last code cell, which starts the chatbot.
3. Answer the timezone, name and location questions, then chat. Type `bye` to exit.

Keep `intents.json` in the same folder as the notebook.

## Author and Credits

- **Author:** Ayesha Atif
- **Coursework:** Programming with Data – Midterm
- Notebook structure and exercise instructions provided by the course.
- Built with Python, [NLTK](https://www.nltk.org/) and [pytz](https://pythonhosted.org/pytz/).
