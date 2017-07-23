##How to open
For the index.hmtl in source, go to: https://konekote.github.io/src/index.html

For the index.html in production, go to:
https://konekote.github.io/dist/index.html

For the pizza.html in source, go to:
https://konekote.github.io/src/views/pizza.html

For the pizza.html in production, go to:
https://konekote.github.io/dist/views/pizza.html


I tried to improve the 2 pages by eliminating any FSL, improving loading speed as well as scroll speed, minifying CSS and JS and optimizing images. The implemented optimizations are in order:
- I first optimized the images and the Javascript,as well as minified the CSS in Index.html with the help of PageSpeed Insights
- I then moved the CSS and Javascript to the end of the body tag and added a print media query to improve the loading speed. I also removed the unnecessary font style and deferred the loading of non-essential CSS
- I then reverted back to normal CSS loading as I could not see a difference in the score or speed of the page and added async tags to analytics.js.
- I ended my trials by trying CSS deferring once again using examples here: 
https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery
- Tried adding an image style to make images even smaller, however did not like the general aspect of it so removed it.
- Added one requestAnimationFrame to updatePositions per scroll, per frame. 
- Crated the src and dist directories and continued working in both. Documented a few changed in the ReadMe file. 
- I then replaced all query selectors with getElementById and getElementByClass and extracted all element selecotrs out of the for loops.
- Made variables for length for items and randomPizzas to prevent redundant calls.
- Implemented a dyanmic mechanism for number of pizzas in background to keep the page scroll at 60 fps.
- I then declared the elem var in the loop declaration and finished by documenting all other changes in the Readme file.
- As a last change, I added the pizzeria photos in original size, with compressed version and small version. Added them to pizza.html with original size, responsive, and to index.html with 100x75px. 


## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository and inspect the code.

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

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>
