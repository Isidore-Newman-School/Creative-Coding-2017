# Writing Code with Atom

**Objective** We want to be able to write code with [Atom](https://atom.io/)- a more robust text editor than the p5 editor- but in order to run all project files in the browser, we need a local server. p5 automatically spawned localhost for us. Now that we're using Atom, we need to start the server ourselves.

## node.js server
1. [Download and install node.js](https://nodejs.org/en/download/)
2. Windows:
  Open the node.js command prompt and type:

  ```bash
  npm install -g http-server
  ```
  On Linux / Mac OS, open a terminal window and type:

  ```bash
  sudo npm install -g http-server
  ```

3. Let's have the server look for files in your local GitHub repository (i.e. where your homework and projects are currently stored). In my case:

  ```bash
  cd C:\Users\jennadeboisblanc\Documents\jennadeboisblanc
  ```

  And now let's get the server running in this location:

  ```bash
  http-server
  ```
4. Done! Go to [http://localhost:8080/](http://localhost:8080/) to see your files.

## Writing Code with Atom
Writing code with Atom is just like writing code with p5. The difference, in this case, is that Atom doesn't automatically create all of the files you need when you begin a project. You need:

index.html ()
sketch.js (where your write JavaScript)

1. Open p5 (hopefully for the last time) and save an empty project in location where you're currently serving files (your GitHub coding folder).

OR

2. Use Atom to create the following files and

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>YOUR PAGE TITLE HERE</title>

    <!-- libraries go here -->
    <script src="libraries/p5.js" type="text/javascript"></script>

    <!-- script files go here -->
    <script src="sketch.js" type="text/javascript"></script>

    <!-- if you have css ... -->
    <style> body {padding: 0; margin: 0;} canvas {vertical-align: top;} </style>

  </head>
  <body>
  </body>
</html>
```
