<!DOCTYPE HTML>
<html lang="en">

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" type="text/css" href="../tools.css" />
    <link rel="stylesheet" type="text/css" href="collatz-harriss.css" />
    <script src="https://cdn.jsdelivr.net/npm/p5@1.0.0/lib/p5.js"></script>
    <title>The Collatz Conjecture and Edmund Harriss's visualisation</title>
</head>

<body>
    <div class="center">
        <h1 id="title">The Collatz Conjecture and Edmund Harriss's visualisation</h1>
        <div id="switch_to"><a onclick="switch_language();">Lees in het Nederlands 🇳🇱</a></div>
        <div id="explainer">
            <p>The Collatz Conjecture is an unsolved problem in mathematics. This JavaScript applet is an accompaniment to our post <a href='https://opencurve.info/the-collatz-conjecture/'>The Collatz Conjecture</a>, where you can read more about the Conjecture. This applet calculates a series of Collatz sequences. If you enter, for example, 10000, it will calculate the Collatz values starting at 10000 (until it reaches the value of 1). It will then calculate the Collatz values starting at 9999. And then 9998, and so on. Lastly, it will plot all the sequences at once down below using <a href='https://opencurve.info/the-collatz-conjecture/#edmundharriss'>Edmund Harriss's visualisation rules</a>. Mind you, if you click OK, it might take a while!</p>
            <p>Enter a positive integer (a positive whole number, max 20000), a line thickness (0.1 to 20), and a color:</p>
        </div>
        <form onsubmit="return CollatzHarriss();" novalidate>
            <input id="start" type="number" min="4" max="20000" step="1" placeholder="Integer">
            <input id="stroke_thickness" type="number" min="0.1" max="20" step="0.1" placeholder="Line width"><br />
            <button id="fg" class="jscolor {valueElement:'fgcolor'}">Pick a colour</button>
            <button id="bg"class="jscolor {valueElement:'bgcolor'}">Background</button>
            <input id="fgcolor" type="hidden" value="ffffff">
            <input id="bgcolor" type="hidden" value="000000">
            <input id="submit_button" type="submit" value="OK"><div id="output"></div>
        </form>
        <div id="graph"></div>
        <p>This is just a side project for the author to teach himself some JavaScript programming. Do have a look at our <a href="https://opencurve.info/">main website</a> for some more maths and physics.</p>
        <p>(C) 2020 <a href="https://twitter.com/kjrunia">KJ Runia</a></p>
        <a href="index.html">Back</a>
    </div>
    <script defer src="collatz-harriss.js"></script>
    <script defer src="jscolor.js"></script>
</body>

</html>
