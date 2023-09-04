#### 8. [Section Overview](#8)

#### 9. [Why Do Front-End Frameworks Exist?](#9)

#### 10. [React vs. Vanilla JavaScript](#10)

#### 11. [What is React?](#11)

#### 12. [Setting Up Our Development Environment](#12)

#### 13. [Pure React](#13)

#### 14. [A Quick Look at React's Official Documentation](#14)

#### 15. [Setting Up a New React Project: The Options](#15)

#### 16. [Setting Up a Project With Create-React-App](#16)

---

<br>

### 8. Section Overview<a id='8'></a>

<br>

### 9. Why Do Front-End Frameworks Exist?<a id='9'></a>

<br>

### 10. React vs. Vanilla JavaScript<a id="10"></a>

[Compare code](https://codesandbox.io/s/react-first-app-advice-52879f?file=/src/vanilla-JS.html)

<br>

### 11. What is React?<a id="11"></a>

<br>

### 12. Setting Up Our Development Environment<a id="12"></a>

VS code extension

- ESLint by microsoft
- prettier
- one monokai theme
- materal icon theme by phillipp kief

---

- copy snippets code from 00-setup/snippets.json
- In Vs-code setting-> User Snippets-> New Gloabl Snippets file...-> PASTE HERE

<br>

### 13. Pure React<a id="13"></a>

- In 01-pure-react/final/index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Hello React!</title>
  </head>
  <body>
    <div id="root"></div>

    <!-- React core library hooks: useState, useEffect, useContext etc -->
    <script
      src="https://unpkg.com/react@18/umd/react.development.js"
      crossorigin
    ></script>

    <!-- Rendering/Updating/Manuplating DOM -->
    <script
      src="https://unpkg.com/react-dom@18/umd/react-dom.development.js"
      crossorigin
    ></script>

    <script>
      function App() {
        // const time = new Date().toLocaleTimeString();
        const [time, setTime] = React.useState(new Date().toLocaleTimeString());

        React.useEffect(function () {
          setInterval(function () {
            setTime(new Date().toLocaleTimeString());
          }, 1000);
        }, []);

        return React.createElement("header", null, `Hello React! It's ${time}`);
      }

      const root = ReactDOM.createRoot(document.getElementById("root"));
      root.render(React.createElement(App));
    </script>
  </body>
</html>
```

<br>

### 14. A Quick Look at React's Official Documentation<a id="14"></a>

- Ref. [Escape Hatches](https://react.dev/learn/escape-hatches)
- Ref. [Hooks](https://react.dev/reference/react)

<br>

### 15. Setting Up a New React Project: The Options<a id="15"></a>

<br>

### 16. Setting Up a Project With Create-React-App<a id="16"></a>

- Ref. [Create react app cmd](https://create-react-app.dev/docs/getting-started)

```sh
npx create-react-app my-app
cd my-app
npm start
```

<br>
