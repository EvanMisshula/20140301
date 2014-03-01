# Files
## base.html
<https://github.com/sebg/20140301/blob/master/base.html>
<br />
## d3_divs.html
<https://github.com/sebg/20140301/blob/master/d3_divs.html>
<br />
## aquarium.json
<https://github.com/sebg/20140301/blob/master/aquarium.json>
<br />
<br />
<br />
# Exercises
## Slide 53: Chrome
<https://www.google.com/chrome>
<br />
## Slide 56: D3.js Setup
<pre>
<code>d3.version;
</code></pre>
<br />
## Slide 61: D3.js Selections
<pre>
<code>d3.select("body");

d3.select("div");

d3.selectAll("div");

d3.select("#d_tre");

d3.select(".d_small");

d3.selectAll(".d_medium ");

d3.select("#d_tre").select("#d_for");

d3.select("#d_tre").select("#d_one");

d3.select("#d_tre").select("#d_fiv");

d3.select("#d_tre").selectAll("div");
</code></pre>
<br />
## Slide 64: D3.js Data Operator
<pre>
<code>d3.select("body").data(["Saturday"]);

d3.select("body").data();

d3.select("body").data(["March"]);

d3.select("body").data();

d3.selectAll("div").data([1,2,3,4,5]);

d3.selectAll("div").data();

d3.selectAll("div").data([11,12,13,14,15]);

d3.selectAll("div").data();
</code></pre>
<br />
## Slide 66: D3.js \_\_data\_\_ Property
<pre>
<code>d3.select("body").data(["one"]);

d3.select("body").data([2]);

d3.select("body").data([{"x":3, "y":4}]);

d3.select("body").data([[[5], [6]]]);
</code></pre>
<br />
## Slide 70: D3.js Enter Selection
<pre>
<code>d3.selectAll("unicorn").data([1,2,3]).enter();

// Reset Browser

d3.selectAll("div").data([4,5,6]).enter();
</code></pre>
<br />
## Slide 72: D3.js Append
<pre>
<code>d3.select("body").selectAll("span").data([4,5,6,7,8]).enter().append("span");

d3.selectAll(“span”);

// Reset Browser

d3.select("body").selectAll("unicorn").data([1,2,3]).enter().append("unicorn");

d3.selectAll(“unicorn”).data();
</code></pre>
<br />
## Slide 75: D3.js Attr
<pre>
<code>d3.select("div").attr("abc", "123");

// Reset Browser

d3.selectAll("div").attr("mos", "def");

d3.select("div").attr("mos");

// Reset Browser

d3.selectAll("div").attr("holiday", function() { return "inn"; });
</code></pre>
<br />
## Slide 77: Using Data Bound To Dom Elements
<pre>
<code>d3.selectAll("span").data([4,5,6,7,8]).enter().append("span");

d3.selectAll("span").attr("d_element", function(d) { return d; });

// Reset Browser

d3.selectAll("unicorn").data([1,2,3]).enter().append("unicorn");

d3.selectAll("unicorn").attr("unicorn_i", function(d, i) { return i; });
</code></pre>
<br />
## Slide 79: Style Attr Shortcut
<pre>
<code>d3.select("div").style("font-size", "24px");

// Reset Browser

d3.selectAll("div").style("font-size", function(d, i) { return (i+1)*25 + "px "; });
</code></pre>
<br />
## Slide 81: D3.js Remove
<pre>
<code>d3.select("body").selectAll("span").data([4,5,6,7,8]).enter().append("span");
             
d3.select("body").selectAll("span").attr("span_d", function(d) { return d; });

d3.select("body").selectAll("span").remove();

// Reset Browser

d3.select("body").selectAll("unicorn").data([1,2,3]).enter().append("unicorn");

d3.select("body").selectAll("unicorn").attr("unicorn_d", function(d) { return d; });

d3.select("body").selectAll("unicorn").remove();
</code></pre>
<br />
## Slide 87: SVG Basic Shapes
<pre>
<code>d3.select("body").append("svg").attr("height",200).attr("width",200);

d3.select("svg").append("circle").attr("cx", 35).attr("cy", 35).attr("r", 25);

// Reset Browser

d3.select("body").append("svg").attr("height",200).attr("width",200);

d3.select("svg").append("rect").attr("x", 10).attr("y", 10).attr("height", 50).attr("width", 50);
</code></pre>
<br />
## Slide 91: D3.js Linear Scales
<pre>
<code>var scaleOne =d3.scale.linear().domain([0, 1000]).range([0, 200]);

var scaleTwo =d3.scale.linear().domain([1000, 0]).range([0, 200]);

scaleOne(0);

scaleOne(1000);

scaleOne(500);

scaleOne(2000);

scaleTwo(0);

scaleTwo(1000);

scaleTwo(500);

scaleTwo(2000);
</code></pre>
<br />
## Slide 96: D3.js Axes
<pre>
<code>d3.select("body").append("svg").attr("height", 200).attr("width", 200);

var axisScale =d3.scale.linear().domain([0, 10]).range([0, 200]);

var xAxis = d3.svg.axis().scale(axisScale);

var xAxisGroup = d3.select("svg").call(xAxis);
</code></pre>
<br />
## Slide 101: D3.js Axes Text & Tick Labels
<pre>
<code>var inner = d3.select("body").append("svg")
    .attr("height", 200)
    .attr("width", 200)
  .append("g")
    .attr("transform", "translate(10, 20)");

var axisScale =d3.scale.linear().domain([0, 10]).range([0, 180]);

var xAxis = d3.svg.axis().scale(axisScale).orient("xxxxx");

var xAxisGroup = inner.call(xAxis);
</code></pre>
<br />
## Slide 103: D3.js Axis Placement
<pre>
<code>var inner = d3.select("body").append("svg")
    .attr("height", 200).attr("width", 200)     
  .append("g")
    .attr("transform", "translate(10, 20)");

var axisScale =d3.scale.linear().domain([0, 100]).range([0, 170]);

var xAxis = d3.svg.axis().scale(axisScale).orient("bottom");

var xAxisGroup = inner.append("g")
    .attr("transform", "translate(0,140)")
    .call(xAxis);
</code></pre>
<br />
## Slide 121: D3.js & AJAX
<pre>
<code>d3.json("aquarium.json", function(error, data) {
  console.log(data);
});
</code></pre>
<br />
## Slide 122: D3.js & AJAX -> In The Wild
<pre>
<code>var tempData;

d3.tsv("data.tsv", function(error, data) {
        tempData = data;
});

tempData;
</code></pre>
<br />
## Slide 134: Add “click” Event To Paragraphs
<pre>
<code>var paras = d3.select("body").selectAll("p")
    .data([10, 11, 12, 13, 14])
  .enter().append("p")
    .text(function(d, i) { return d; });

paras.on("click", function() { alert("clicked"); });

paras.on("click", function(d, i) { alert(i); });

paras.on("click", function(d, i) { alert(d); });

paras.on("click", function(d, i) { alert(i); d3.select(this).remove() });    
</code></pre>
<br />
## Slide 135: Add “click” With Named Function
<pre>
<code>var paras = d3.select("body").selectAll("p")
    .data([10, 11, 12, 13, 14])
  .enter().append("p")
    .text(function(d, i) { return d; });

function clickFunction () { alert("clicked"); }

paras.on("click", clickFunction);

function clickFunction () { alert("bye!"); d3.select(this).remove(); }

paras.on("click", clickFunction);
</code></pre>
<br />
## Slide 136: Two Event Listeners
<pre>
<code>var paras = d3.select("body").selectAll("p")
    .data([10, 11, 12, 13, 14])
  .enter().append("p")
    .text(function(d, i) { return d; });

function colorBlack() { d3.select(this).style("color", "black"); }

function colorRed() { d3.select(this).style("color", "red"); }

paras
    .on("mouseover", colorRed)
    .on("mouseout", colorBlack);
</code></pre>
<br />
## Slide 137: Remove Scatterplot Dots
<pre>
<code>function mouseOver () { d3.select(this).remove(); }

d3.selectAll(".dot").on("mouseover", mouseOver);
</code></pre>
<br />
## Slide 142: Give Scatterplot Tool Tips
<pre>
<code>var div = d3.select("body").append("div")   
    .style("position", "absolute")
    .style("text-align", "center")
    .style("width", "240px")
    .style("height", "2.5em")
    .style("font", "1.5em sans-serif")
    .style("color", "yellow")
    .style("pointer-events", "none")
    .style("background", "black")
    .style("border-radius", "8px")
    .style("border", "solid 1px green")
    .style("opacity", 0);

function mouseover(d) {
    div.html("Sepal Width: " + d.sepalWidth + "&lt;br /&gt; Sepal Length: " + d.sepalLength)
        .style("left", (d3.event.pageX + 9) + "px")
        .style("top", (d3.event.pageY - 43) + "px")
        .style("opacity", 1);
}

function mouseout() {
    div.style("opacity", 1e-6);
}

d3.selectAll(".dot")
    .on("mouseover", mouseover)
    .on("mouseout",  mouseout);
</code></pre>
<br />
## Slide 147: Event Listener - Attr Change
<pre>
<code>var paras = d3.select("body").selectAll("p")
    .data([0,1,2,3,4])
  .enter().append("p")
    .text(function(d, i) { return d; })
    .style("font-size", "48px");

function colorBlack() { d3.select(this).style("color", "black"); }

function colorRed() { d3.select(this).style("color", "red"); }

paras
    .on("mouseover", colorRed)
    .on("mouseout", colorBlack);
</code></pre>
<br />
## Slide 148: Event Listener - Attr Transition
<pre>
<code>var paras = d3.select("body").selectAll("p")
    .data([0,1,2,3,4])
  .enter().append("p")
    .text(function(d, i) { return d; })
    .style("font-size", "48px");

function colorBlack() {
     d3.select(this).transition().duration(5000).style("color", "black");
}

function colorRed() { d3.select(this).style("color", "red"); }

paras
    .on("mouseover", colorRed)
    .on("mouseout", colorBlack);
</code></pre>
<br />
## Slide 157: Circle - Radius Attr Change
<pre>
<code>var circle = d3.select("body").append("svg").selectAll("circle")
    .data([1]).enter().append("circle")
    .attr("cx", "50").attr("cy", "50").attr("r", "25");

function rInc() { d3.select(this).attr("r", "50"); }
function rDec() { d3.select(this).attr("r", "25"); }

circle
    .on("mouseover", rInc)
    .on("mouseout" , rDec);
</code></pre>
<br />
## Slide 158: Circle - Radius Attr Transition
<pre>
<code>var circle = d3.select("body").append("svg").selectAll("circle")
    .data([1]).enter().append("circle")
    .attr("cx", "50").attr("cy", "50").attr("r", "25");

function rInc() { 
    d3.select(this)
        .transition()
            .ease("elastic")
            .delay(1000)
            .duration(2000)
            .attr("r", "50"); }

circle
    .on("mouseover", rInc)
    .on("mouseout" , function() { d3.select(this).attr("r", "25") }); </code></pre>
<br />
## Slide 163: Circle - Transition Chaining
<pre>
<code>var circle = d3.select("body").append("svg").selectAll("circle")
    .data([1]).enter().append("circle")
    .attr("cx", "50").attr("cy", "50").attr("r", "25");

function clickFun() { 
    d3.select(this)
        .transition().duration(2000).attr("cx", "200")
        .transition().duration(1000).attr("cy", "200")
        .transition().duration(2000).attr("cx", "50")
        .transition().duration(3000).attr("cy", "50");
}

circle
    .on("click", clickFun);</code></pre>
<br />
## Slide 164: Circle - Multi-Attr Transition Chain
<pre>
<code>var circle = d3.select("body").append("svg").selectAll("circle")
    .data([1]).enter().append("circle")
    .attr("cx", "50").attr("cy", "50").attr("r", "25");

function clickFun() { 
    d3.select(this)
        .transition().duration(2000).attr("cx", "200").style("fill", "red")
        .transition().duration(1000).attr("cy", "200").style("fill", "green")
        .transition().duration(2000).attr("cx", "50").style("fill", "blue")
        .transition().duration(3000).attr("cy", "50").style("fill", "black");
}

circle
    .on("click", clickFun);</code></pre>
<br />
## Slide 169: Circle - Data-Driven Transition
<pre>
<code>var circle = d3.select("body").append("svg").selectAll("circle")
    .data([1, 2]).enter().append("circle")
    .attr("cx", function(d, i) { return d * 50 + 25 * i; })
    .attr("cy", "50").attr("r", "25");

function clickFun() {
    d3.select(this)
        .transition()
            .duration(function(d,i) { return d * 2000; })
            .style("fill", "red")
        .transition().duration(1000).style("fill", "black")
}

circle.on("click", clickFun);</code></pre>