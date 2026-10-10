# Final Project - Emotion Detection

**Final Project** for the AI-based Web Application Development course
(`oaqjp-final-project-emb-ai`).

A Flask web application that performs emotion detection on customer feedback using IBM
Watson's embeddable NLP `EmotionPredict` service. Enter text in the browser and the app
returns the scores for anger, disgust, fear, joy, and sadness, along with the dominant
emotion.

## Features

- Web interface for submitting text to analyze
- Emotion detection: anger, disgust, fear, joy, and sadness
- Identifies the dominant emotion
- Error handling for blank or invalid input (HTTP status code 400)
- Unit tests for the emotion detector
- Static code analysis with a 10/10 pylint score

## Project Structure

```
.
├── server.py                       # Flask app and routes
├── EmotionDetection/
│   ├── __init__.py                 # Package import
│   └── emotion_detection.py        # Calls the Watson emotion API
├── templates/
│   └── index.html                  # Web page
├── static/
│   └── mywebscript.js              # Front-end logic
├── test_emotion_detection.py       # Unit tests
├── LICENSE
└── README.md
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

The emotion detector can also be used directly in Python:

```python
from EmotionDetection.emotion_detection import emotion_detector

result = emotion_detector("I love this new technology.")
print(result)
# {'anger': ..., 'disgust': ..., 'fear': ..., 'joy': ..., 'sadness': ...,
#  'dominant_emotion': 'joy'}
```

## Running Tests

```bash
python -m unittest test_emotion_detection.py
```

## Static Code Analysis

```bash
pip install pylint
python -m pylint server.py
```

## License

See the [LICENSE](LICENSE) file for details.
