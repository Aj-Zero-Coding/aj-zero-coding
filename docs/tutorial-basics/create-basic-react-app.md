---
sidebar_position: 2
---

# Create React Js app

## React.Js

React.Js is one of the maximum popular front-stop frameworks these days, which masses of human beings find useful to study. Building your first React.Js application.
In this article, I’m going to create an easy React.Js application with step by step.
To create this software, it'd be a plus to have fundamentals of React.Js, Javascript, HTML, and CSS. 

**Prerequisites: The pre-requisites for this project are:**

- React
- Functional Components
- JavaScript ES6 / Prettier (extension) for code formatting
- HTML & CSS

**Simple Intro of react:**

**Step-1:** Required some libraries for react project.

**React**

``https://unpkg.com/react@17/umd/react.development.js``

**React-DOM**

``https://unpkg.com/react-dom@17/umd/react-dom.development.js``

**Step-2:** Create ``index.html`` file and write some code.

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
    <title>React ⚛️</title>
</head>

<body>
    <h1>Getting Started React With <span style="color: green;">Aj Zero Coding</span></h1>
</body>

</html>
```

**Output:**

![image](https://user-images.githubusercontent.com/99037494/212524043-b14db73d-4f28-49ce-9faf-a2a56fdc0915.png)

**Step-3:** Edit `index.html` file and add code.

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
    <title>React ⚛️</title>
</head>

<body>
    <h1>Getting Started With <span style="color: green;">Aj Zero Coding</span></h1>

<div id="root"></div>

<script type="text/javascript">
    ReactDOM.render(
        React.createElement("h1", null, "Getting Started!"),
        document.getElementById("root")
    );
</script>
</body>
</html>
```

**Output:**

![image](https://user-images.githubusercontent.com/99037494/212524133-ec498c28-538a-4e05-b74d-dc3b4d24f399.png)

**Step-4:** add style in `index.html`.

```html
<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8" />
    <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>
    <title>React ⚛️</title>
</head>

<body>
    <h1>Getting Started With <span style="color: green;">Aj Zero Coding</span></h1>

<div id="root"></div>

<script type="text/javascript">
    let heading = React.createElement(
        "h1", {
            style: {
                color: "blue"
            }
        },
        "Hey Everyone!"
    );

    ReactDOM.render(
        heading,
        document.getElementById("root")
    );
</script>
  
</body>
  
</html>
```

**Output:**

![image](https://user-images.githubusercontent.com/99037494/212524238-6ab35d87-131d-4439-b4a2-961d451f4633.png)
