---
layout: opencs
title: Pong Game Lesson
permalink: /pong-lessons/
---


### Pong Game Lessons Java Script


### Roles

| Role            | Name                 | GitHub |
|:---------------:|:--------------------:|:------:|
| 🧭 Scrum Master | **Devin Bir**        | [GitHub](https://github.com/kush1434) |
| 📋 Assistant Scrum | **Jonah Larsson**   | [GitHub](https://github.com/frogle-dev) |
| 💻 Engineer     | **Malachi Mendoza**         | [GitHub](https://github.com/ellioty15) |
| 💻 Engineer     | **Aarush Bandi**         | [GitHub](https://github.com/Bandi-A-54547) |
| 💻 Engineer     | **Sri Rohit Varma Datla**         | [GitHub](https://github.com/douprojo) |
| 💻 Engineer     | **Santiago Alverado**         | [GitHub](https://github.com/Flv0ur) |

### **Lessons On JavaScript**

### Lessons: 💻 Mathmatical Expresions

📌 What Is a Mathematical Expression in Code?
In programming, a mathematical expression is a line of code that calculates a value using numbers, variables, and operators—just like in math class!
Example:
let result = 5 + 3 * 2;


This calculates 5 + (3 × 2) and stores the result in result.

🧩 Key Operators in JavaScript

| Operator         | Symbol | Example     | Result | JS Code to Get Result       |
|------------------|--------|-------------|--------|-----------------------------|
| Addition         | `+`    | `2 + 3`     | `5`    | `console.log(2 + 3);`       |
| Subtraction      | `-`    | `5 - 2`     | `3`    | `console.log(5 - 2);`       |
| Multiplication   | `*`    | `4 * 3`     | `12`   | `console.log(4 * 3);`       |
| Division         | `/`    | `10 / 2`    | `5`    | `console.log(10 / 2);`      |
| Remainder        | `%` | `7 % 3`     | `1`    | `console.log(7 % 3);`       |
| Exponentiation   | `**`   | `2 ** 3`    | `8`    | `console.log(2 ** 3);`      |


🧠 Variables in Expressions
You can use variables to store values and build expressions:
let x = 10;
let y = 3;
let total = x + y * 2; // total = 10 + (3 × 2) = 16



🔍 Order of Operations
Just like in math, JavaScript follows PEMDAS:
- Parentheses
- Exponents
- M/D Multiplication/Division (left to right)
- A/S Addition/Subtraction (left to right)
let result = (4 + 2) * 3; // = 6 × 3 = 18



🧪 Practice Challenge
Try writing this in JavaScript:
let a = 5;
let b = 2;
let c = 3;
let expression = a * b + c ** 2 - (a + c);
console.log(expression);


### Challenge 1:

<!-- 🎉 Answer Console with Confetti -->
<h3>🎯 Challenge: What is the out put when you type let 10 * 20 + 5?</h3>
<p>Type your answer below and hit "Check Answer"</p>

<div id="answer-console">
  <input type="text" id="user-answer" placeholder="Your answer..." />
  <button onclick="checkAnswer()">Check Answer</button>
  <p id="feedback"></p>
  <canvas id="confetti-canvas"></canvas>
</div>

<style>
  #answer-console {
    margin-top: 20px;
    padding: 10px;
    background: #222;
    color: #fff;
    font-family: monospace;
    border-radius: 8px;
    position: relative;
  }
  #user-answer {
    width: 60%;
    padding: 8px;
    font-size: 1em;
    background: #333;
    color: #fff;
    border: 1px solid #555;
    border-radius: 4px;
  }
  button {
    padding: 8px 12px;
    margin-left: 10px;
    background: #0f0;
    color: #000;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  #feedback {
    margin-top: 10px;
    font-weight: bold;
  }
  #confetti-canvas {
    position: absolute;
    top: 0;
    left: 0;
    pointer-events: none;
    width: 100%;
    height: 100%;
  }
</style>

<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
<script>
  function checkAnswer() {
    const input = document.getElementById("user-answer").value.trim();
    const feedback = document.getElementById("feedback");
    const correctAnswer = "205";

    if (input === correctAnswer) {
      feedback.textContent = "✅ Correct! You nailed it!";
      feedback.style.color = "#0f0";
      confetti({
        particleCount: 200,
        spread: 95,
        origin: { y: 0.6 }
      });
    } else {
      feedback.textContent = "❌ Try again!";
      feedback.style.color = "#f00";
    }
  }
</script>

### 🖥️ Interactive JavaScript Console

Type a command below and click **Run** to see the result.

<div id="console-container">
  <input type="text" id="console-input" placeholder="Type JavaScript here..." />
  <button onclick="runCommand()">Run</button>
  <pre id="console-output"></pre>
</div>

<style>
  #console-container {
    margin-top: 20px;
    padding: 10px;
    background: #1e1e1e;
    color: #eee;
    font-family: monospace;
    border-radius: 8px;
  }
  #console-input {
    width: 70%;
    padding: 8px;
    font-size: 1em;
    background: #333;
    color: #fff;
    border: none;
    border-radius: 4px;
  }
  button {
    padding: 8px 12px;
    margin-left: 10px;
    background: #007acc;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  #console-output {
    margin-top: 10px;
    white-space: pre-wrap;
  }
</style>

<script>
  function runCommand() {
    const input = document.getElementById("console-input").value;
    const output = document.getElementById("console-output");
    try {
      const result = eval(input);
      output.textContent = `> ${input}\n${result}`;
    } catch (err) {
      output.textContent = `> ${input}\nError: ${err.message}`;
    }
  }
</script>

---

