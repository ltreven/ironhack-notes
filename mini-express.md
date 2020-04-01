---
description: How to create a minimum express server using Node and connect to MongoDB
---

# Express Intro

## Creating Express Server

{% embed url="https://blog.vanila.io/setup-basic-server-with-express-framework-37b2ec749a6d" %}

## Express Generator

```text
npm install express-generator -g
express myapp
```

## HandleBars

#### Prepare

First we should uninstall Jade if it came with Express Generator

```text
npm uninstall jade --save
```

Next step: open `app.js` and remove `jade` references like this one:

```text
app.set('view engine', 'jade'); // REMOVE IT
```

Also delete all the jade files under views folder.

Then let's install an enhanced version of handlebars, very well adapted to Express Server

```text
npm install express-handlebars --save
```

#### Tell Express what you want to use to render views

In `app.js` import \(require\) express-handlebars library

```text
const hbs = require('express-handlebars');
```

Then setup the view engine.

```text
// view engine setup
app.engine('hbs', hbs({extname: 'hbs', defaultLayout: 'layout', layoutsDir: __dirname + '/views'}));
app.set('views', path.join(__dirname, 'views'));
app.set('view engine', 'hbs');
```

#### Create Layout Templates for HTML pages

Create a file called `layout.hbs` in the views folder with the content like this:

```text
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="/public/stylesheets/style.css">
    <title>{{ title }}</title>
</head>
<body>
    {{{ body }}}
</body>
</html>
```

Create also a `index.hbs` file with the following content:

```text
<h1>{{ title }}</h1>
<p>Welcome to {{ title }}</p>
```

And it is also a good idea to have a default error page. Create the `error.hbs` file:

```text
<h1>ERROR</h1>
<p>Error: {{ message }}</p>
```

And that's it. Run using the following command on terminal

```text
npm start
```

And open you browser on the following location: `http://localhost:3000/`

\`\`

