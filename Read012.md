# JavaScript Graphics
Chart.js
Chart.js comes with the following built-in chart types:

- Scatter
- Line
- Bar
- Radar
- Pie and Doughnut
- Polar Area
- Bubble
### Chart.js is an open source JavaScript library. Using Chart.js, add animated, interactive graphs on your website.

# What is HTML Canvas?
The HTML canvas element is used to draw graphics, on the fly, via scripting (usually JavaScript).
The canvas element is only a container for graphics. You must use a script to actually draw the graphics.
Canvas has several methods for drawing paths, boxes, circles, text, and adding images.
  
## HTML Canvas Can Draw Text
Canvas can draw colorful text, with or without animation.
  
## HTML Canvas Can Draw Graphics
Canvas has great features for graphical data presentation with an imagery of graphs and charts.
  
## HTML Canvas Can be Animated
Canvas objects can move. Everything is possible: from simple bouncing balls to complex animations.
  
## HTML Canvas Can be Interactive
Canvas can respond to JavaScript events.

Canvas can respond to any user action (key clicks, mouse clicks, button clicks, finger movement).
  
## HTML Canvas Can be Used in Games
Canvas' methods for animations, offer a lot of possibilities for HTML gaming applications.

Canvas Example
In HTML, a canvas element looks like this:

canvas id="myCanvas" width="200" height="100"/canvas
The canvas element must have an id attribute so it can be referred to by JavaScript.

The width and height attribute is necessary to define the size of the canvas.

## Example
<!DOCTYPE html>
<html>
<head>
<script
<script src="https://cdn.jsdelivr.net/npm/chart.js@2.8.0"></script>
</script>
</head>
<body>
<canvas id="myChart" width="500" height="300"></canvas>
<script type="text/javascript">
   var ctx = document.getElementById("myChart");
   var myChart = new Chart(ctx, {
      type: 'bar',
         data: {
            labels: ["2005", "2007" , "2009" , "2012", "2014"],
            datasets: [
               { label: 'HouseHold income',
               data: [5000,8000,10000,1200,15000],
               backgroundColor :['rgba(255, 129, 102, 1)',
               'rgba(234, 162, 235, 1)',
               'rgba(255, 206, 36, 1)',
               'rgba(75, 192, 192, 1)',
               'rgba(153, 102, 255, 1)',
            ],
         }
      ]
   },
   options: {
      scales: {
         yAxes: [{
            ticks: {
               beginAtZero:true
            }
         }]
      }
   }
});
</script>
</body>
</html>


