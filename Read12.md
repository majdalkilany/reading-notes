# Chrt
we can use  a JavaScript plugin that uses HTML5’s canvas element to 
draw the graph onto the page. It’s a well documented plugin that makes
 using all kinds of bar charts, line charts

## Setting up

we need to download chart.js and set it up

## Drawing a line chart

To draw a line chart  the first thing we need to do is
 create a canvas element in our HTML in which Chart.js can draw our chart
**then we need to write a script that will retrieve the context of the canvas, so add this to the foot of your body element**
*Inside the same script tags we need to create our data,
 in this instance it’s an object that contains labels for
  the base of our chart and datasets to describe the values 
  on the chart. Add this immediately above the line that begins ‘var buyers=’:*

### Drawing a pie chart

first thing we need the canvans elemant
*then we need to get the context and to instantiate the chart*
Next we need to create the data. This data is a little 
different to the line chart because the pie chart is simple
after the pie data we will add options these optione will do to
 things remove the stroke from the segments, and then they animate the scale 
 of the pie so that it zooms out from nothing
 ## Drawing a bar chart
Finally, we add  a bar chart to our page. 
Next, we retrieve the element and create the graph And finally, we add in the bar chart’s data:










