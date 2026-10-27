# Code With AI Quiz

A small browser quiz built with HTML, CSS, and JavaScript. Open `index.html` and answer five multiple-choice questions about coding with AI, testing, CSS, and time complexity. Your score is shown at the end.

## Features

- One question at a time with four clickable options
- Instant advance after an answer (each question can only be answered once)
- Final score: `Your score is X out of 5`
- Navy-and-gold layout styled in a separate CSS file

## How to run

No build step or server is required.

1. Clone or copy this folder.
2. Open `index.html` in a browser (double-click the file, or drag it into a tab).

That is enough because the app is static: `index.html` loads `style.css` and `script.js` from the same folder.

## Project structure

```
Quiz/
├── index.html   # Page markup: title, question, options, result
├── style.css    # Layout and theme
├── script.js    # Questions, scoring, and UI updates
└── README.md
```

## How it works

`script.js` holds a `questions` array. Each item has:

- `question` — the prompt
- `options` — four possible answers
- `answer` — the correct option string

On load, `showQuestion()` renders the current prompt and builds a button for each option. Clicking a button calls `checkAnswer()`:

- If the choice matches `answer`, `score` increases by one
- The quiz moves to the next question
- After the last question, the heading becomes **Quiz Complete** and `#result` shows the score

## Questions

The current set covers:

1. What a large language model predicts (next token)
2. Conventional commit types (`feat`, `fix`, and similar)
3. That a unit test should fail before the bug is fixed
4. That webpage styling belongs in a CSS file
5. Nested loops and quadratic time complexity

## Adding or changing questions

Edit the `questions` array in `script.js`. Keep the same shape:

```javascript
{
    question: "Your question text?",
    options: ["Option A", "Option B", "Option C", "Option D"],
    answer: "Option A"
}
```

`answer` must match one of the `options` strings exactly.
