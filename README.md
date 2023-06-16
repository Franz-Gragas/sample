# sample


import React, { useState, useRef } from "react";

function App() {
  const inputRef = useRef(null);
  const resultRef = useRef(null);
  const [result, setResult] = useState(0);

  function plus(e) {
    e.preventDefault();
    const inputValue = parseFloat(inputRef.current.value);
    setResult(result + inputValue);
    inputRef.current.value = "";
  }

  function minus(e) {
    e.preventDefault();
    const inputValue = parseFloat(inputRef.current.value);
    setResult(result - inputValue);
    inputRef.current.value = "";
  }

  function times(e) {
    e.preventDefault();
    const inputValue = parseFloat(inputRef.current.value);
    setResult(result * inputValue);
    inputRef.current.value = "";
  }

  function divide(e) {
    e.preventDefault();
    const inputValue = parseFloat(inputRef.current.value);
    setResult(result / inputValue);
    inputRef.current.value = "";
  }

  function resetNumber(e) {
    e.preventDefault();
    inputRef.current.value = "";
  }

  function resetAnswer(e) {
    e.preventDefault();
    setResult(0);
  }

  return (
    <div className="App">
      <div>
        <h1>Simple Calculator (Finals)</h1>
      </div>
      <form>
        <h2>Answer: {result}</h2>
        <input ref={inputRef} type="number" placeholder="Type a number" />
        <br />
        <br />
        <button onClick={plus}>Plus</button>
        <button onClick={minus}>Minus</button>
        <button onClick={times}>Times</button>
        <button onClick={divide}>Divide</button>
        <button onClick={resetNumber}>Reset Number</button>
        <button onClick={resetAnswer}>Reset Answer</button>
      </form>
    </div>
  );
}

export default App;
