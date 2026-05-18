# Quizzler

A quiz game built with Python and Tkinter that fetches true/false questions from the Open Trivia Database and lets the user answer them through a simple GUI.

## What it is

`Quizzler` is a desktop quiz application that presents a series of True/False questions. The app tracks the current score, provides visual feedback for correct and incorrect answers, and disables the buttons when the quiz ends.

## How it works

- `main.py` loads the question data from `data.py`, converts each item into a `Question` object, and starts the quiz UI.
- `data.py` calls the Open Trivia Database API using `requests` to fetch 10 boolean questions.
- `question_model.py` defines the `Question` class, storing question text and the correct answer.
- `quiz_brain.py` manages the quiz logic: question ordering, score tracking, and answer checking.
- `ui.py` creates the Tkinter window, displays questions, handles user input via True/False buttons, and updates the score and background color as feedback.

## Requirements

- Python 3.x
- `tkinter` (included in most Python installations; on Linux install `python3-tk` if needed)
- `requests` library

Install the required Python package with:

```bash
pip install requests
```

## Run

From the `Quizzler` folder, run:

```bash
python main.py
```

## Notes

- The game requires an internet connection because `data.py` fetches questions from the Open Trivia Database API at startup.
- The images used for the True and False buttons are stored in `images/true.png` and `images/false.png`.
- After the final question, the app displays a completion message and disables the buttons.

## Files

- `main.py` — entry point that builds the question bank and starts the quiz interface.
- `data.py` — downloads question data from the Trivia API.
- `question_model.py` — stores question text and correct answer.
- `quiz_brain.py` — quiz logic, score keeping, and answer validation.
- `ui.py` — Tkinter user interface and button handling.
- `images/true.png`, `images/false.png` — button icons.

Enjoy the quiz!
