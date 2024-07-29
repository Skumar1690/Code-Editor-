# My Code Editor

My Code Editor is a simple, interactive, in-browser code editor that allows you to write and run HTML, CSS, and JavaScript code in real-time. It provides a convenient way to practice and test code snippets without needing any external tools.

## Features

- **HTML Editor**: Write HTML code in the provided text area.
- **CSS Editor**: Write CSS code to style your HTML.
- **JavaScript Editor**: Add interactivity and functionality with JavaScript.
- **Real-time Output**: See the results of your code immediately in the output area.

## Getting Started

To use the code editor, simply open the `index.html` file in your web browser. You will see three text areas for HTML, CSS, and JavaScript, and an output area that renders the result of your code.

### Usage

1. **HTML**: Write your HTML code in the HTML text area.
2. **CSS**: Write your CSS code in the CSS text area.
3. **JavaScript**: Write your JavaScript code in the JavaScript text area.
4. The output will be displayed in the `Output` section on the right side of the screen.

## How It Works

The code editor uses JavaScript to capture the content of the HTML, CSS, and JavaScript text areas. When you type in any of the text areas, the `run` function is triggered, updating the content of an iframe that displays the output.

```javascript
function run() {
  let htmlcode = document.getElementById("Html-code").value;
  let csscode = document.getElementById("css-code").value;
  let jscode = document.getElementById("Js-code").value;
  let output = document.getElementById("output");

  output.contentDocument.body.innerHTML =
    htmlcode + "<style>" + csscode + "</style>";
  output.contentWindow.eval(jscode);
}
```
