# 🎯 Quiz Game
A simple, responsive, interactive quiz game built with HTML, CSS, and JavaScript.

## 🖥️ Live Demo
https://cherryrambler.github.io/Quiz-game/

## 📦 Project Structure
- index.html - Main HTML page
- style.css - Styling for all screens
- script.js - All quiz logic

## 🚀 Features
- Start screen with intro message
- Dynamic questions with answer buttons generated in JavaScript
- Progress bar showing quiz progress
- Score tracking
- Result screen with custom message based on performance
- Responsive design for mobile and desktop

## 📸 Screenshots
![Quiz Game](./Screenshots/Screenshot%202025-07-09%20013135.png)
![Quiz Game](./Screenshots/Screenshot%202025-07-09%20013145.png)
![Quiz Game](./Screenshots/Screenshot%202025-07-09%20013204.png)
![Quiz Game](./Screenshots/Screenshot%202025-07-09%20013216.png)
![Quiz Game](./Screenshots/Screenshot%202025-07-09%20013243.png)

## 🛠️ How to Run
1. Clone or download this repo.
2. Open index.html in your browser.

## 📚 What I Learned
I learned several modern JavaScript techniques while building this:

### 1️⃣ forEach for DOM elements
Used to loop through answers and add them to the page:

```
currentQuestion.answers.forEach((answer) => {
  const button = document.createElement("button");
  button.textContent = answer.text;
  button.classList.add("answer-btn");
  button.dataset.correct = answer.correct;
  button.addEventListener("click", selectAnswer);
  answersContainer.appendChild(button);
});
```

➡️ forEach makes it easy to loop through arrays and apply logic to each element.

### 2️⃣ Arrow Functions
Used for cleaner, more modern function syntax:

```
currentQuestion.answers.forEach((answer) => {
  // arrow function syntax
});
```

➡️ Arrow functions are shorter and don't bind their own this .

### 3️⃣ dataset
Used to store custom data in HTML elements:

```
button.dataset.correct = answer.correct;
```

➡️ dataset is an easy way to attach extra data to elements (e.g. marking answers as correct/incorrect).

### 4️⃣ Array.from()
Converts a NodeList to an Array so we can use forEach:

```
Array.from(answersContainer.children).forEach
((button) => {
  if (button.dataset.correct === "true") {
    button.classList.add("correct");
  } else if (button === selectedButton) {
    button.classList.add("incorrect");
  }
});
```
➡️ NodeList doesn’t have all Array methods, so Array.from() is very useful.

## 🎨 Styling
- Light, clean card layout
- Highlight correct/incorrect answers
- Animated progress bar
- Responsive design with media queries

## 🤝 Credits
Based on this YouTube tutorial: https://youtu.be/kAiX0itnonM?si=fGAqYxqhtEwWVcQY

## 💡 Future Improvements
- Add more questions
- Add timer functionality
- Store high scores in localStorage
- Add sound effects or animations