---
description: Javascript fundamentals
---

# Javascript

## Prepare to launch

Install Node.js - a version of JavaScript that doesn't need a browser. Example for installation on MacOS:

```text
curl "https://nodejs.org/dist/latest/node-${VERSION:-$(wget -qO- https://nodejs.org/dist/latest/ | sed -nE 's|.*>node-(.*)\.pkg</a>.*|\1|p')}.pkg" > "$HOME/Downloads/node-latest.pkg" && sudo installer -store -pkg "$HOME/Downloads/node-latest.pkg" -target "/"
```

### Check version

```text
$ node -v
v8.16.0
```

## Hello World Javascript

Use:

* node REPL
* Javascript File

## Check Documentation and Tutorials

MDN: [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

What is MDN: [https://en.wikipedia.org/wiki/MDN\_Web\_Docs](https://en.wikipedia.org/wiki/MDN_Web_Docs)

W3Schools: [https://www.w3schools.com/js/default.asp](https://www.w3schools.com/js/default.asp)

Intro book: [https://launchschool.com/books/javascript](https://launchschool.com/books/javascript)

> You make prototype objects, and then … make new instances. Objects are mutable in JavaScript, so we can augment the new instances, giving them new fields and methods. These can then act as prototypes for even newer objects. We don't need classes to make lots of similar objects… Objects inherit from objects. What could be more object oriented than that?

> dot notation \(`obj.x = 10`\) and bracket notation \(`obj['x'] = 10`\)



