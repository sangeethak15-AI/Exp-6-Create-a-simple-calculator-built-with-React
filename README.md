# Exp-6-Create-a-simple-calculator-built-with-React
## AIM:
To create a simple calculator using react js

## SOFTWARE:
Visual Studio Code

## ALGORITHM:

1.Set up the React environment: Install Node.js and create a new React project using create-react-app. Open your terminal or command prompt and run the following commands
Open the project in your preferred code editor.

2.Replace the contents of 'src/App.js" with the following code

3.Replace the contents of "src/App.css" with the following CSS styles

4.Start the development server: In the terminal, run npm start to start the React development server.

5.Open your browser and visit http://localhost:3000 to see the calculator.
## PROGRAM:
### APP.JS
```
import React, { useState } from 'react';
import './App.css';

function App() {
  const [result, setResult] = useState('');

  const handleClick = (e) => {
    setResult(result.concat(e.target.name));
  };

  const handleClear = () => {
    setResult('');
  };

  const handleCalculate = () => {
    try {
      setResult(eval(result).toString());
    } catch (error) {
      setResult('Error');
    }
  };

  return (
    <body>
      <p>SIMPLE CALCULATOR</p>
      <div className="calculator">
        <input type="text" value={result} readOnly />
        <div className="keypad">
          <button name="7" onClick={handleClick}>7</button>
          <button name="8" onClick={handleClick}>8</button>
          <button name="9" onClick={handleClick}>9</button>
          <button className="operator" name="/" onClick={handleClick}>&divide;</button>
          <button name="4" onClick={handleClick}>4</button>
          <button name="5" onClick={handleClick}>5</button>
          <button name="6" onClick={handleClick}>6</button>
          <button className="operator" name="*" onClick={handleClick}>&times;</button>
          <button name="1" onClick={handleClick}>1</button>
          <button name="2" onClick={handleClick}>2</button>
          <button name="3" onClick={handleClick}>3</button>
          <button className="operator" name="-" onClick={handleClick}>&ndash;</button>
          <button name="0" onClick={handleClick}>0</button>
          <button name="." onClick={handleClick}>.</button>
          <button className="operator" id="equals" onClick={handleCalculate}>=</button>
          <button className="operator" name="%" onClick={handleClick}>%</button>
          <button className="operator clear" onClick={handleClear}>Clear</button>
        </div>
      </div>
    </body>
  );
}

export default App;
```
### APP.CSS:
```
.calculator {
  width: 300px;
  margin: 50px auto;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
}
body{
  background-color: rgb(242, 243, 237);
  margin:200px;
}
p{
  color:#f07a7a;
  text-align:center;
  font-size:40px;
  font-weight:700;
  
}

input[type="text"] {
  width: 100%;
  height: 40px;
  margin-bottom: 10px;
  font-size: 18px;
  padding: 5px;
  
}

.keypad {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 5px;
}

button {
  width: 100%;
  height: 40px;
  font-size: 18px;
  border: none;
  background-color: #e4aaaa;
  cursor: pointer;
}

.operator {
  background-color: #d73ef5;
  color: #fff;
}

#equals {
  background-color: #ec4590;
  color: #fff;
}
.operator.clear {
  grid-column: span 4;
}
```
## OUTPUT:
### IDLE:
![image](https://github.com/sangeethak15-AI/Exp-6-Create-a-simple-calculator-built-with-React/assets/93992063/e198f42f-ccc6-4321-a899-f8892f554b8a)

### CALCLUTION:
![image](https://github.com/sangeethak15-AI/Exp-6-Create-a-simple-calculator-built-with-React/assets/93992063/332b5766-9e90-49d4-8c45-bdc9232aa2fa)
![image](https://github.com/sangeethak15-AI/Exp-6-Create-a-simple-calculator-built-with-React/assets/93992063/3ab3567e-cf96-48b1-96a0-bb3301b81493)

## RESULT:
Thus the simple calculator using react js.
