# Sentiment Analyzer

A Flask web application that analyzes the sentiment of a given text using IBM Watson's
embeddable NLP sentiment service. Enter text in the browser and the app returns whether it
is positive, negative, or neutral along with a confidence score.

## Features

- Web interface for submitting text to analyze
- Sentiment classification: positive, negative, or neutral
- Confidence score for each prediction
- Error handling for invalid or empty input
- Unit tests for the analyzer

## Project Structure

```
.
??? server.py                     # Flask app and routes
??? SentimentAnalysis/
?   ??? __init__.py
?   ??? sentiment_analysis.py     # Calls the Watson sentiment API
??? templates/
?   ??? index.html                # Web page
??? static/
?   ??? mywebscript.js            # Front-end logic
??? test_sentiment_analyzer.py    # Unit tests
??? LICENSE
??? README.md
```

## Requirements

- Python 3.x
- Flask
- requests

Install the dependencies:

```bash
pip install flask requests
```

## Running the Application

Start the Flask server:

```bash
python server.py
```

Then open your browser at [http://localhost:5000](http://localhost:5000).

## Usage

The sentiment analyzer can also be used directly in Python:

```python
from SentimentAnalysis.sentiment_analysis import sentiment_analyzer

result = sentiment_analyzer("I love working with Python")
print(result)  # {'label': 'SENT_POSITIVE', 'score': ...}
```

## Running Tests

```bash
python -m unittest test_sentiment_analyzer.py
```

## License

See the [LICENSE](LICENSE) file for details.
