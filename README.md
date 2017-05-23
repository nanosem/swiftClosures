# swiftClosures
Closures in swift 3 </br>

<h3><b> Introduction </b></h3></br>
https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/Closures.html

<h4> What is closures in swift? </h4>

  Closures are self-contained blocks of functionality that can be passed around and used in your code.
<h2><b> How to declare a Closure in Swift? </b></h2>
http://fuckingclosuresyntax.com/

<code>
{ (parameters) -> ReturnType in
  //Closure body goes here...
}
</code>

<h1><b> Existing types of closures: </b></h1>

<h3> @escaping </h3>

<p> A closure is said to escape a function when the closure is passed as an argument to the function, but is called after the     function returns. When you declare a function that takes a closure as one of its parameters, you can write <b>@escaping</b>   before   the parameter’s type to indicate that the closure is allowed to escape.

One way that a closure can escape is by being stored in a variable that is defined outside the function. As an example, many   functions that start an asynchronous operation take a closure argument as a completion handler. The function returns after     it starts the operation, but the closure isn’t called until the operation is completed—the closure needs to escape, to be .   called later. For example: </p>
https://pastebin.com/FhjeYQyX

<p> My example of using escaping closure: </p>
https://pastebin.com/68rVvLFU </br>

<b> Marking a closure with @escaping means you have to refer to self explicitly within the closure. </b>

<h3> @noescape </h3>

<code lang="swift">
  func someFunctionWithNonescapingClosure(closure: () -> Void) {
    closure()
  }
</code>

<h3><b> And now - @autoclosure</b></h3>

<p>
An autoclosure is a closure that is automatically created to wrap an expression that’s being passed as an argument to a function. It doesn’t take any arguments, and when it’s called, it returns the value of the expression that’s wrapped inside of it. This syntactic convenience lets you omit braces around a function’s parameter by writing a normal expression instead of an explicit closure.
</p>

<p>
It’s common to call functions that take autoclosures, but it’s not common to implement that kind of function. For example, the assert(condition:message:file:line:) function takes an autoclosure for its condition and message parameters; its condition parameter is evaluated only in debug builds and its message parameter is evaluated only if condition is false.
</p>

Example:
http://ericasadun.com/2015/04/30/swift-a-little-autoclosure-hacking/
