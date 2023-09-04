#### 1. [Course Roadmap and Projects](#1)

#### 2. [Building Our First React App!](#2)

#### 3. [Watch Before You Start!](#3)

#### 4. [Read Before You Start!](#4)

#### 5. [Downloading Course Material](#5)

---

<br>

### 1. Course Roadmap and Projects<a id='1'></a>

<br>

### 2. Building Our First React App!<a id='2'></a>

- [React App sandbox ](https://codesandbox.io/s/react-first-app-advice-52879f?file=/src/App.js:0-695)

- In App.jsx

```js
import { useEffect, useState } from "react";

export default function App() {
  const [advice, setAdvice] = useState("");
  const [count, setCount] = useState(0);

  async function getAdvice() {
    const res = await fetch("https://api.adviceslip.com/advice");
    // convert responce into json
    const data = await res.json();
    // update state
    setAdvice(data.slip.advice); // update advice from json data
    setCount((c) => c + 1); // update count using arrow function
  }

  useEffect(function () {
    getAdvice();
  }, []);

  return (
    <div>
      <h1>{advice}</h1>
      <button onClick={getAdvice}>Get advice</button>
      <Message count={count} />
    </div>
  );
}

function Message(props) {
  return (
    <p>
      You have read <strong>{props.count}</strong> pieces of advice
    </p>
  );
}
```

<br>

### 3. Watch Before You Start!<a id='3'></a>

<br>

### 4. Read Before You Start!<a id='4'></a>

<br>

### 5. Downloading Course Material<a id='5'></a>

<br>
