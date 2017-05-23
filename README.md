# swiftClosures
<h3><b> Introduction </b></h3>
</hr>

<h4> What is closures in swift? </h4>
<p> Closures are self-contained blocks of functionality that can be passed around and used in your code. </p>

<h4><b> How to declare a Closure in Swift? </b></h4>

<code>
{ (parameters) -> ReturnType in
  //Closure body goes here...
}
</code>

</hr>

<h3> Existing types of closures: </h3>
<h4> @escaping </h4>

<img src="https://swiftunboxed.com/images/closure-escape.png" width="500" height="300"> </br>

<p> 
A closure is said to escape a function when the closure is passed as an argument to the function, but is called after the    function returns. When you declare a function that takes a closure as one of its parameters, you can write @escaping   before   the parameter’s type to indicate that the closure is allowed to escape. 
<p>

<p>
One way that a closure can escape is by being stored in a variable that is defined outside the function. As an example, many  functions that start an asynchronous operation take a closure argument as a completion handler. The function returns after it starts the operation, but the closure isn’t called until the operation is completed—the closure needs to escape, to be called later. For example: https://pastebin.com/FhjeYQyX
</p>

<p> 
Another example of using escaping closure: https://pastebin.com/mwVScJDV
</p>

<p>
Marking a closure with @escaping means you have to refer to self explicitly within the closure.
Goto: "Swift Capture List in Closures"

</p>

<h3> @noescape (default closure type in swift 3+)</h3>

<img src="https://swiftunboxed.com/images/closure-noescape.png" width="500" height="300"> </br>


<p> Simple example of usage: https://pastebin.com/JsS74P4L 

The lifecycle of a non-escaping closure is simple:

Pass a closure into a function
The function runs the closure (or not)
The function returns
</p>

<h4>@autoclosure</h4>

<p>
An autoclosure is a closure that is automatically created to wrap an expression that’s being passed as an argument to a function. It doesn’t take any arguments, and when it’s called, it returns the value of the expression that’s wrapped inside of it. This syntactic convenience lets you omit braces around a function’s parameter by writing a normal expression instead of an explicit closure.
</p>

<p>
It’s common to call functions that take autoclosures, but it’s not common to implement that kind of function. For example, the assert(condition:message:file:line:) function takes an autoclosure for its condition and message parameters; its condition parameter is evaluated only in debug builds and its message parameter is evaluated only if condition is false.
</p>

<p>
Simple example of usage:
https://pastebin.com/JG4fqrnY

And one more:
https://pastebin.com/AEKchATh
</p>
</hr>

<div>
<h3> Swift Capture List in Closures </h3>

Simple example of using capture list:
https://pastebin.com/2Pr5wwyE

Some examples of usage:
https://pastebin.com/M1gn7MFi

When to use unowned and weak self?
https://pastebin.com/dVCkFEbB

</div>
</hr>

<div>
  <h5> Referances: <h5>
  <p> Official documentation </p>
  https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html </br>
  <p> Declarations of closure blocs </p>
  http://goshdarnclosuresyntax.com </br>
  <p> Capture list (Rus) <p>
  http://swiftbook.ru/doc/automatic-reference-counting/resolving-strong-reference-cycles-for-closures </br>
</div>
