## Website Performance Optimization portfolio project

~~Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).~~

~~To get started, check out the repository and inspect the code.~~

Challenge Accepted! See below...way below for optimizations made.

### Getting started

#### Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to the top-level of your project directory to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

#### Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js.

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimizations made Part 1:

Index.html now gets a speed score of 93/100 for mobile & 95/100 for Desktop.
You can further optimize by leveraging browser cache.

Techniques used to optimize:
- Inline style.css (also minified)
- `async` google fonts
- `async` and `media="print"` for print.css
- move js to bottom of file
- `async` scripts
- optimize images
- make remote images local and optimized

The hosted solution for you to run your own insight test is [https://gmawji.github.io/optimized-portfolio/index.html](here).

### Optimizations made Part 2:

Inline styles on pizza.html & compressed images.

Techniques used to optimize main.js:
- `resizePizzas()` - replaced `querySelector` with `getElementByID`
- `changePizzaSizes()` - replaced `querySelector` with `getElementByClass`
- `var randomPizza` - replaced `querySelector` with `getElementByClass`
- removed `determineDx()` - replaced with `switch(size)` this was modified from `resizePizzas`
- `updatePositions()` - replaced `querySelector` with `getElementByClass`

Other optimizations are also noted in main.js

The hosted solution is [https://gmawji.github.io/optimized-portfolio/views/pizza.html](here).