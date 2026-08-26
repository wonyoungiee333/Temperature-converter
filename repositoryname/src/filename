import "./App.css";
import { useState } from "react";

const App = () => {
  const [value, setValue] = useState("");
  //this gets the value from the input
  const [conversionType, setConversionType] = useState("");
  //this gets which conversion type was chosen
  const [result, setResult] = useState("");
  //this is the formatted output that'll be displayed

  function conversion() {
    if (value === "" || conversionType === "") return;
    //this prevents the function from happening if either values return null

    const convertedValue =
      conversionType === "ctof"
        ? Number(value) * 1.8 + 32
        : (Number(value) - 32) / 1.8;
    setResult(`Answer: ${Math.round(convertedValue)}\u00B0`);
    //this displays the result as a string
  }

  return (
    <>
      <center>
        <div id="container">
          <h1>Unit Converter</h1>
          <input
            id="input"
            type="number"
            title="input"
            value={value}
            onChange={
              (event) =>
                setValue(
                  event.target.value,
                ) /* onChange is more reliable in these inputs. it's set to preform an arrow function which uses setValue, a react hook that dynamically sets the value for input fields.*/
            }
          />
          {/* the input where we input the number to convert from f to c and vice versa */}
          <label>
            <input
              type="radio"
              name="conv"
              id="ctof"
              checked={conversionType === "ctof"}
              onChange={() => setConversionType("ctof")}
            />
            {/* converts it from celsius to farenheit */}
            Celsius =&gt; Fahrenheit
          </label>
          <label>
            <input
              type="radio"
              name="conv"
              id="ftoc"
              checked={conversionType === "ftoc"}
              onChange={() => setConversionType("ftoc")}
            />
            Fahrenheit =&gt; Celsius
          </label>
          {/* converts it from farenheit to celsius */}
        </div>
        <button type="button" onClick={conversion}>
          Submit
        </button>
        <div id="div">
          <p id="text">{result || "Answer:"}</p>{/* prints 'Answer: result' */}
        </div>
      </center>
    </>
  );
};
//AI was used to debug this app but other than that it was all written by me, a human. I fully understand these concepts, and I'm not a vibe coder. I just don't know how to use debuggers.
export default App;
