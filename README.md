# swiftClosures
Closures in swift 3 <br>

<h3><b> Introduction </b></h3>

<h4> What is closures in swift? </h4>

  Closures are self-contained blocks of functionality that can be passed around and used in your code.

<h2><b> How to declare a Closure in Swift? </b></h2>
http://fuckingclosuresyntax.com/

<h1><b> Existing types of closures: </b></h1>

<div>
  <h3> @escaping </h3>
  Escaping closure

  A closure is said to escape a function when the closure is passed as an argument to the function, but is called after the     function returns. When you declare a function that takes a closure as one of its parameters, you can write <b>@escaping</b>   before   the parameter’s type to indicate that the closure is allowed to escape.

  One way that a closure can escape is by being stored in a variable that is defined outside the function. As an example, many   functions that start an asynchronous operation take a closure argument as a completion handler. The function returns after     it starts the operation, but the closure isn’t called until the operation is completed—the closure needs to escape, to be .   called later. For example:

<span>  <code lang="swift">
    var completionHandlers: [() -> Void] = []
    func someFunctionWithEscapingClosure(completionHandler: @escaping () -> Void) {
      completionHandlers.append(completionHandler)
    }
  </code> 
</span>
  
  
  <h3> @noescape <h3>
</div>

