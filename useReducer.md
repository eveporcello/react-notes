```
import { useState, useReducer } from "react"

function App() {
  //const [status, setStatus] = useState(true);
  const [status, toggle] = useReducer(
    (status) => !status,
    false
  );
  return (
    <div>
      <h1>
        The restaurant is currently{" "}
        {status ? "open" : "closed"}.
      </h1>
      <button onClick={toggle}>
        {status ? "Close" : "Open"} Restaurant
      </button>
      <Header name="Alex" year={new Date().getFullYear()} />
      <Main
        dishes={dishObjects}
        openStatus={status}
        onStatus={toggle}
      />
    </div>
  );
}

export default App;

```
