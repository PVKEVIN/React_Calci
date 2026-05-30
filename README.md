# Ex04 Simple Calculator - React Project
## Date:27/5/26
## Name: Kevin P
## Register Number: 212224040159

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
```
App.js
import React, { useState } from "react";
import "./App.css";

function App() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clear = () => setInput("");

  const calculate = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="container">
      <h1>Calculator</h1>

      <input type="text" value={input} readOnly />

      <div className="buttons">
        <button onClick={clear}>C</button>
        <button onClick={() => handleClick("/")}>/</button>
        <button onClick={() => handleClick("*")}>*</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")}>+</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={calculate}>=</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>

        <button onClick={() => handleClick("0")}>0</button>
      </div>
    </div>
  );
}

export default App;
```
```
App.css
body {
  margin: 0;
  font-family: Arial;
  background: linear-gradient(to right, #667eea, #764ba2);
}

.container {
  width: 300px;
  margin: 80px auto;
  background: white;
  padding: 20px;
  border-radius: 12px;
  text-align: center;
}

input {
  width: 100%;
  height: 40px;
  margin-bottom: 20px;
  font-size: 18px;
  text-align: right;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 16px;
  border: none;
  background: #00adb5;
  color: white;
  border-radius: 6px;
  cursor: pointer;
}

button:hover {
  background: #007b80;
}
```

## OUTPUT
<img width="1639" height="810" alt="image" src="https://github.com/user-attachments/assets/1a0d4308-010b-4c81-aed0-a684725bc534" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
