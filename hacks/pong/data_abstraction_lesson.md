---
layout: opencs
title: Pong Game Lesson
permalink: /pong-lessons/abstraction
---


### Pong Game Lessons Java Script


### Roles

| Role            | Name                 |
|:---------------:|:--------------------:|
| 🧭 Scrum Master | **Devin Bir**        | 
| 📋 Assistant Scrum/Enginner | **Jonah Larsson**   |
| 🧪 Tester | **Malachi Mendoza**         |
| 🧪 Tester | **Aarush Bandi**         |
| 🏁 Tester/Finisher    | **Santiago Alverado**         | 
| 💻 Engineer/Finisher   | **Sri Rohit Varma Datla**         | 

### **Lessons On JavaScript**

---

### Lessons: 💻 Data Abstraction

📌 What is **Data Abstraction**?
Data abstraction is a concept in programming that focuses on hiding the full implementation of something with a simpler interface, making this thing reusable and easier to use.
Examples:
- Classes
- Abstract classes 
- Abstract methods
- Functions
- Much more


We will be explaining data abstraction using pong
### 🧩 Explanation of different types of data abstraction with pong
**Functions**
```
function declareWinner(winner){
  winnerMsg.textContent = `${winner} Wins!`;
  running = false;
}
``` 
Take, for example, this function. Inside the curly braces ("{}") there is the implementation of the function.
Put simply, this function prints out who won the game on screen. Then, it ends the game by setting the "running" boolean to false.
The part where data abstraction starts is actually function definition. Instead of having to write the code inside the function every time you want to end the game, a function is declared with a parameter called "winner".
Now, when you want to declare a winner you can simply write:
```
declareWinner(player1);
```
> Note: The variable "player1" can be replaced with any other variable that satisfies the function.

This is an example of data abstraction due to the fact that the code inside of the function is hidden and instead interfaced with a simple function call.

<b>Example #2: Classes</b>

Think of classes like blueprints. They outline how to make specific things, and later in the code you can make an object (an instance of the class) based on the original template.

```
// the class
class Car {

  // constructor of the class, creates/initializes the object
  constructor(make, model, year) {
    this.make = make;
    this.model = model;
    this.year = year;
  }

  // function that displays what the car is (ex: This car is a 2016 Volkswagen Tiguan)
  displayInfo() {
    console.log('This car is a ${this.year} ${this.make} ${this.model}`)
  }
}

// making an object(instance) of the class
const myCar = new car("Toyota", "Corolla", 2020);

// calling a function on the object
myCar.diplayInfo(); // outputs "This car is a 2020 Toyota Corolla"
```

In this example, you can see how we made a new class called "car", which then allowed us to make an "instance" of the car that we could model into whatever we wanted. When we use the car class, you don't need to know how the car is built internally. Instead, all of the info is stored inside the class, and can be hidden or "abstracted" away.

## 🧪 Practice Challenges

### Challenge 1: What would you type to make a new class with the name House? (Add brackets)

<p>Type your answer in the text box and press "Check Answer"</p>

<div id="answer-console">
  <input type="text" id="class-answer" placeholder="Enter here..." />
  <button onclick="checkClassAnswer()">Check Answer</button>
  <p id="class-feedback"></p>
  <canvas id="class-confetti"></canvas>
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
  #class-answer {
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
  #class-feedback {
    margin-top: 10px;
    font-weight: bold;
  }
  #class-confetti {
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
  function checkClassAnswer() {
    const input = document.getElementById("class-answer").value.trim();
    const feedback = document.getElementById("class-feedback");
    const correctAnswer = "class House {}";

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

### Challenge 2: Make a constructor for the house with the parameters cost, age, and size (add brackets, don't add this.)

<div id="answer-console">
  <input type="text" id="constructor-answer" placeholder="Type answer here..." />
  <button onclick="checkAnswer()">Check Answer</button>
  <p id="constructor-feedback"></p>
  <canvas id="constructor-confetti"></canvas>
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
  #constructor-answer {
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
  #constructor-feedback {
    margin-top: 10px;
    font-weight: bold;
  }
  #constructor-confetti {
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
    const input = document.getElementById("constructor-answer").value.trim();
    const feedback = document.getElementById("constructor-feedback");
    const correctAnswer = "constructor(cost, age, size) {}";

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

### Challenge 3: Make an instance of the House class with the name myHouse without parameters (don't forget the semicolon!)

<div id="answer-console">
  <input type="text" id="const-response" placeholder="Type answer here..." />
  <button onclick="checkAnswer()">Check Answer</button>
  <p id="const-feedback"></p>
  <canvas id="const-confetti"></canvas>
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
  #const-response {
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
  #const-feedback {
    margin-top: 10px;
    font-weight: bold;
  }
  #const-confetti {
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
    const input = document.getElementById("const-response").value.trim();
    const feedback = document.getElementById("const-feedback");
    const correctAnswer = "const myHouse = new House();";

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

---

### **Homework**
In order to learn this topic of data abstraction, you have to practice:

> **Task:** Making multiple new classes. Each class should be able to have clearly defined parameters. Make at least 2 new instances of that class with different paramaters (maybe add other commands as well, ex: functions like displayInfo or make some new ones!)
