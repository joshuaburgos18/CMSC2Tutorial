## Working with Numbers

Your file for this exercise should be saved in the public folder and should be accessed using this link: **"/javascript-exercises/working-with-numbers.html"**. Include all the scripts using an **external file** that should be accessed using this link: **"/script/working-with-numbers.js"**.  

* * *

#### Functions

A **function** is a group of reusable code which can be called anywhere in your program. It is executed when "something" invokes it (calls it).   

A JavaScript function is defined with the `function` keyword, followed by a `name`, followed by `parentheses`. The parentheses may include 0 or more parameter names separated by commas: (parameter1, parameter2, ...). The code to be executed by the function is placed inside curly brackets. Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).

<div class="card-panel grey lighten-3">

<h5> Function Definition Syntax </h5>
```
	function name(parameter1, parameter2, parameter3) {
		code to be executed
	}
```
</div>

<br>
In our discussion about functions, there are some terms that you need to learn:

*   Function **parameters** are the names listed in the function definition.
*   Function **arguments** are the real values received by the function when it is invoked (called).
*   **Local** variables are variable inside the function.

<br>

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>
<script>
	//Creates a popup box with text Hello World!
	function sayHello() {
		alert("Hello World!");
}
</script>
```
<script>
	//Creates a popup box with text Hello World!
	function sayHello() {
		alert("Hello World!");
    }
</script>

```

</div>

As discussed, the example above will not be executed if it is not yet invoked (called).

The code inside a function will execute when an event occurs (when a user clicks a button), when it is invoked (called) from JavaScript code, or automatically (self invoked). To invoke (call) a function, you simply need to write the name of that function as shown in the following code.

Let's try to add a button to invoke the JavaScript function:

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div>

Click the button to call the function

<form><input type="button" onclick="sayHello()" value="Say Hello"></form>

</div>

```
<p>Click the button to call the function</p>
<form>
	 <input type="button" onclick="sayHello()" value="Click Me!">
</form>
```

</div>

<br>

Images and styles can also be manipulated using functions.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function changeImage() { document.getElementById('lbulb').src = "/images/pic_bulbon.gif"; var par = document.getElementById('sample1'); par.style.color = "yellow"; par.style.fontWeight = "bold"; }</script>

<p>Image and Style</p>

![Lightbulb](http://www.w3schools.com/js/pic_bulboff.gif)

<p id="sample1">Click the light bulb to turn it on!</p>

</div>

```
<script>
	function changeImage() {
		document.getElementById("lbulb").src = "http://www.w3schools.com/js/pic_bulbon.gif";
		var par = document.getElementById("sample1");
		par.style.color = "yellow";
		par.style.fontWeight = "bold";
	}
</script>

<p>Image and Style</p>
<img src="/images/pic_bulboff.gif" onclick="changeImage()" alt="Lightbulb" id="lbulb" />
<p id="sample1">Click the light bulb to turn it on!</p>

```

</div>

<br>

Now, let's try to create a function with parameters. Values can be passed to parameters while calling a function. These passed values will be captured inside the function and any manipulation can be done over those parameters.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script type="text/javascript">//Writes in the page the name and age values function outputDetails(name, age){ document.write (name + " is " + age + " years old."); }</script>

<p>Example with Parameters</p>

<form><input type="button" onclick="outputDetails('Senyora', 18)" value="View Senyora Details"></form>

</div>

```
<script>
	 function outputDetails(name, age){
		document.write (name + " is " + age + " years old.");
	 }
</script>

<p>Example with Parameters</p>
<p>Click the button to call the function</p>
<form>
	<input type="button" onclick="outputDetails('Senyora', 18)" value="View Senyora Details">
</form>

```

</div>

<br>

If the function was invoked from a statement, JavaScript will **return** to execute the code after the invoking statement. Functions often compute a return value. The return value is "returned" back to the "caller" using the `return` statement. This statement should be the **last** statement in a function.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script type="text/javascript">function concatenate(first, last) { var full; full = first + " " + last; return full; } function outputName(first, last) { document.write ("First name: " + first + ".<br>"); document.write ("Last name: " + last + ".<br>"); var result = concatenate(first, last) document.write ("Put it together: " + result + "!"); }</script>

<p>Example with Return Value</p>

<form><input type="button" onclick="outputName('Anna', 'Manalastas')" value="Concatenate!"></form>

</div>

```
<script>
	//Concatenates the first and last name
	function concatenate(first, last) {
		var full;
		full = first + " " + last;
		return full;
	}

	//Writes in the page the first and last name values
	function outputName(first, last) {
		document.write ("First name: " + first + ".<br>");
		document.write ("Last name: " + last + ".<br>");
		var result = concatenate(first, last)
		document.write ("Put it together: " + result + "!");
	}
</script>

<p>Example with Return Value</p>
<p>Click the button to call the function</p>
<form>
	<input type="button" onclick="outputName('Anna', 'Manalastas')" value="Concatenate!">
</form>

```

</div>

<br>

Another example using JavaScript function is converting the temperature from fahrenheit to celsius.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function getCelsius() { var fahr = document.getElementById("fahrenheit").value;     document.getElementById("celsius").value = (5/9) * (fahr-32); }</script>

<p>Convert Fahr to Cel</p>

<form><label>Fahrenheit</label> <input type="text" name="fahrenheit" id="fahrenheit"><label>Celsius</label><input type="text" name="celsius" id="celsius"><input type="button" onclick="getCelsius()" value="Convert"></form>

</div>

```
<script>
	function getCelsius() {
		var fahr = document.getElementById("fahrenheit").value;
		document.getElementById("celsius").value = (5/9) * (fahr-32);
	} 
</script>

<p>Convert Fahr to Cel</p>
<form>
	<label>Fahrenheit</label>
	<input type="text" name="fahrenheit" id="fahrenheit">
	<label>Celsius</label>
	<input type="text" name="celsius" id="celsius">
	<input type="button" onclick="getCelsius()" value="Convert">
</form>

```

</div>

* * *

#### Numbers

Numbers in JavaScript can be written with, or without, decimals.

<div class="card-panel grey lighten-3">

<h5>Example</h5>

```
<script>
	var x = 34.00;	// A number with decimals
	var y = 34;	// A number without decimals
</script>
```

</div>

<br>

Numbers with scientific (exponent) notation can also be written.

<div class="card-panel grey lighten-3">

<h5>Example</h5>

```
<script>
	var x = 123e5	// 12300000
	var y = 123e-5;	// 0.00123
</script>

```

</div>

Integers (numbers without a period or exponent notation) are considered accurate up to 15 digits. As for the floating point numbers, the maximum number of decimals is 17.

JavaScript interprets numeric constants as hexadecimal if they are preceded by 0x.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function convertToHex() { document.getElementById("sample2").innerHTML = "0xFF = " + 0xFF; }</script>

<p>Hexadecimal Values</p>

<input type="button" onclick="convertToHex()" value="Convert"></div>

```
<script>
	function convertToHex() {
		document.getElementById("sample2").innerHTML = "0xFF = " + 0xFF;
	}
</script>

<p>Hexadecimal Values</p>
<input type="button" onclick="convertToHex()" value="Convert"/>
<p id="sample2"></p>

```

</div>

<br>

**Infinity (or -Infinity)** is the value JavaScript will return if you calculate a number outside the largest possible number. It is of number type.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function computeInf() { var x = 2/0; var y = -2/0; document.getElementById("sample3").innerHTML = "To " + x + " or " + y + " and Beyond!"; }</script>

<p>Infinity Example</p>

<input type="button" onclick="computeInf()" value="Compute"></div>

```
<script>
	function computeInf() {
		var x = 2/0;
		var y = -2/0;
		document.getElementById("sample3").innerHTML = "To " + x + " or " + y + " and Beyond!";
	}
</script>

<p>Infinity Example</p>
<input type="button" onclick="computeInf()" value="Compute" />
<p id="sample3"></p>

```

</div>

<br>

**Nan** (Not a Number) is a JavaScript reserved word indicating that a value is not a number. Trying to do arithmetic with a non-numeric string will result in NaN. It is also of number type.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function computeNaN() { document.getElementById("sample4").innerHTML = 100 / "Hello World!"; }</script>

<p>NaN Example<p>

<input type="button" onclick="computeNaN()" value="Compute"></div>

```
<script>
	function computeNaN() {
		document.getElementById("sample4").innerHTML = 100 / "Hello World!";
	}
</script>

<p>NaN Example</p>
<input type="button" onclick="computeNaN()" value="Compute" />
<p id="sample4"></p>

```

</div>

* * *

#### Numbers and Strings

JavaScript strings are used for storing and manipulating text. A string can be any text inside single or double quotes while numbers can be integers or floating-point numbers that does not require the use of quotes. In JavaScript, numbers can be converted to string, vice versa.   

Numbers can be converted to string using the `toString()` method.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function numToStr(num1, num2) { var x = num1+ num2; var y = num1.toString() + num2.toString(); document.getElementById("sample5").innerHTML = "The sum of " + num1 + " and " + num2 + " is " + x + ". <br/> Put it together: " + y + "! <3"; }</script>

<p>Num to Str</p>

<input type="button" onclick="numToStr(14,3)" value="Convert Number"></div>

```
<script>
	function numToStr(num1, num2) {
		var x = num1+ num2;
		var x = num1.toString() + num2.toString();
		document.getElementById("sample5").innerHTML = "The sum of " + num1 + " and " + num2 + " is " + x + ". <br/> Put it together: " + y + "! <3";
	}
</script>

<p>Num to Str</p>
<input type="button" onclick="numToStr(14, 3)" value="Convert Number" />
<p id="sample5"></p>

```

</div>

<br>

Strings can also be converted to Numbers using the `parseInt()` and `parseFloat()` method.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function strToNum(str1, str2) { var w = parseInt(str1); var x = parseInt(str2); var y = parseFloat(str2); document.getElementById("sample6").innerHTML = w + "<br/>" + x + "<br/>" + y; }</script>

<p>Str to Num</p>

<input type="button" onclick="strToNum('15','10.333')" value="Convert"></div>

```
<script>
	function strToNum(str1, str2) {
		var w = parseInt(str1);
		var x = parseInt(str2);
		var y = parseFloat(str2);
		var z;	//try to convert str1 to float
		document.getElementById("sample6").innerHTML = w + "<br/>" + x + "<br/>" + y;
	}
</script>

<p>Str to Num</p>
<input type="button" onclick="strToNum('15','10.333')" value="Convert" />
<p id="sample6"></p>

```

</div>

* * *

#### Math Object

The Math object allows you to perform mathematical tasks on numbers.

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function outputCons() { document.getElementById("sample7").innerHTML = "E = " + Math.E + "<br>" + "PI = " + Math.PI + "<br>" + "Square root of 2 = " + Math.SQRT2 + "<br>"; }</script>

<p>Here are some Math constants. </p>

<input type="button" onclick="outputCons()" value="Print Constants"></div>

```
<script>
	function outputCons() {
		document.getElementById("sample7").innerHTML = "E = " + Math.E + "<br>" + "PI = " + Math.PI + "<br>" + "Square root of 2 = " + Math.SQRT2 + "<br>";
	}
</script>

<p>Here are some Math constants.</p>
<input type="button" onclick="outputCons()" value="Print Constants"/>
<p id="sample7"></p>

```

</div>

<br>

These are other Math object properties that you can use:

<table class="striped responsive-table">

<tbody>

<tr>

<th style="width:20%">Property</th>

<th>Description</th>

</tr>

<tr>

<td>E</td>

<td>Returns Euler's number (approx. 2.718)</td>

</tr>

<tr>

<td>LN2</td>

<td>Returns the natural logarithm of 2 (approx. 0.693)</td>

</tr>

<tr>

<td>LN10</td>

<td>Returns the natural logarithm of 10 (approx. 2.302)</td>

</tr>

<tr>

<td>LOG2E</td>

<td>Returns the base-2 logarithm of E (approx. 1.442)</td>

</tr>

<tr>

<td>LOG10E</td>

<td>Returns the base-10 logarithm of E (approx. 0.434)</td>

</tr>

<tr>

<td>PI</td>

<td>Returns PI (approx. 3.14)</td>

</tr>

<tr>

<td>SQRT1_2</td>

<td>Returns the square root of 1/2 (approx. 0.707)</td>

</tr>

<tr>

<td>SQRT2</td>

<td>Returns the square root of 2 (approx. 1.414)</td>

</tr>

</tbody>

</table>

<br>

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function getMax() { document.getElementById("sample8").innerHTML = Math.max(0, 150, 30, 20, -8); }</script>

<p>String Method Example</p>

<input type="button" onclick="getMax()" value="Find Max"></div>

```
<script>
	function getMax() {
		document.getElementById("sample8").innerHTML = Math.max(0, 150, 30, 20, -8);
	}
</script>

<p>String Method Example</p>
<input type="button" onclick="getMax()" value="Find Max"/>
<p id="sample8"></p>

```

</div>

<br>

These are other Math object methods that you can use:

<table class="striped responsive-table">

<tbody>

<tr>

<th style="width:20%">Method</th>

<th>Description</th>

</tr>

<tr>

<td>abs(x)</td>

<td>Returns the absolute value of x</td>

</tr>

<tr>

<td>acos(x)</td>

<td>Returns the arccosine of x, in radians</td>

</tr>

<tr>

<td>asin(x)</td>

<td>Returns the arcsine of x, in radians</td>

</tr>

<tr>

<td>atan(x)</td>

<td>Returns the arctangent of x as a numeric value between -PI/2 and PI/2 radians</td>

</tr>

<tr>

<td>atan2(y,x)</td>

<td>Returns the arctangent of the quotient of its arguments</td>

</tr>

<tr>

<td>ceil(x)</td>

<td>Returns x, rounded upwards to the nearest integer</td>

</tr>

<tr>

<td>cos(x)</td>

<td>Returns the cosine of x (x is in radians)</td>

</tr>

<tr>

<td>exp(x)</td>

<td>Returns the value of E<sup>x</sup></td>

</tr>

<tr>

<td>floor(x)</td>

<td>Returns x, rounded downwards to the nearest integer</td>

</tr>

<tr>

<td>log(x)</td>

<td>Returns the natural logarithm (base E) of x</td>

</tr>

<tr>

<td>max(x,y,z,...,n)</td>

<td>Returns the number with the highest value</td>

</tr>

<tr>

<td>min(x,y,z,...,n)</td>

<td>Returns the number with the lowest value</td>

</tr>

<tr>

<td>pow(x,y)</td>

<td>Returns the value of x to the power of y</td>

</tr>

<tr>

<td>random()</td>

<td>Returns a random number between 0 and 1</td>

</tr>

<tr>

<td>round(x)</td>

<td>Rounds x to the nearest integer</td>

</tr>

<tr>

<td>sin(x)</td>

<td>Returns the sine of x (x is in radians)</td>

</tr>

<tr>

<td>sqrt(x)</td>

<td>Returns the square root of x</td>

</tr>

<tr>

<td>tan(x)</td>

<td>Returns the tangent of an angle</td>

</tr>

</tbody>

</table>

<br>

<div class="card-panel grey lighten-3">

<h5>Try This Example!</h5>

<div><script>function getRand() { var x = Math.random(); //randomize var y = Math.floor((Math.random() * 50) + 1); //randomize between 1 to 50 document.getElementById("sample9").innerHTML = x + "<br/>" + y; document.getElementById("rand").value = "Click Me Baby One More Time!"; }</script>

<p>Randomize</p>

<input id="rand" type="button" onclick="getRand()" value="Click Me!"></div>

```
<script>
	function getRand() {
		var x = Math.random(); //randomize
		var y = Math.floor((Math.random() * 50) + 1); //randomize between 1 to 50
		document.getElementById("sample9").innerHTML = x + "<br/>" + y;
		document.getElementById("rand").value = "Click Me Baby One More Time!";
	}
</script>

<p>Randomize</p>
<input id="rand" type="button" onclick="getRand()" value="Click Me!"/>
<p id="sample9"></p>

```

</div>

The example above generates random numbers, one that is completely random, the other with a specified range. Click the button again to generate new random numbers.  

* * *

#### References

*   [W3Schools](http://www.w3schools.com/)
*   [JavaScript Functions](http://www.tutorialspoint.com/javascript/javascript_functions.htm)