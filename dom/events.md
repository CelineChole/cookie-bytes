# Events

## How to handle an event that changes class such as "toggle the button on and off on each click"?

To toggle a button, you can add a className as 'active' and if you click on the button you remove 'active'.

```js
const button = document.getElementsByTagName("button");

button[0].addEventListener("click", (event) => {
  if (event.target.className === "active") {
    event.target.className = "";
  } else {
    event.target.className = "active";
  }
});
```

## Event listeners - extra resources

https://gist.github.com/CelineChole/f76ef7b77071d7958f68ad37ebfa1afb
