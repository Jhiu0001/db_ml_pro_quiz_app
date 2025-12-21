# Databricks Machine Learning Professional Quiz App
# DBML_PRO_Quiz.v0.1.0 - James Hiu - Dec.21.2025

A Flask-based quiz application designed to deliver structured, repeatable quizzes from JSON-based test banks.  
The app supports both multiple-choice and multi-select questions, deterministic answer shuffling, and configurable quiz lengths.

---

## Features

- Flask web application
- JSON-driven question banks
- Multiple Choice (MC) and Multi-Select (MS) support
- Deterministic answer randomization per question
- Sequential or randomized question order
- Session-based scoring and progress tracking
- Clean, minimal UI with explanations for incorrect answers
- Modular test bank structure for easy expansion

---

## Project Structure
db_ml_pro_quiz_app/
├─ quiz.py # Flask application logic
├─ templates/
│ ├─ quiz.html # Main quiz interface
│ ├─ quiz_start.html # Quiz configuration page
│ ├─ quiz_end.html # Final score summary
│ └─ test_question_template.json
├─ test_bank/ # JSON test banks
│ ├─ Q1-Q10.json # questions are sourced from paid mock exams provider sites
│ ├─ Q11-Q20.json # I try to keep it to 10 questions per file for readability
├─ Testing/
│ ├─ Q21-Q30.json # New questions go into this folder then corresponding directory lines are commented/uncommented in the quiz.py
│ ├─ Q31-Q40.json # I would be editing for typos, and visual presentation (UI/UX) of new questions before moving files from Testing to test_bank.

---

## How It Works

1. Questions are loaded from one or more JSON files at startup
2. Users configure quiz length and randomization options
3. Questions are served sequentially during the session
4. Answer choices are shuffled deterministically using question IDs
5. Scores and progress are tracked using Flask sessions
6. Explanations are shown for incorrect answers

---

## Running the App Locally

### Prerequisites
- Python 3.9+
- Flask

