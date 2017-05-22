# swiftClosures
Closures in swift 3 <br>
by Sh.Nanosem

<h3><b> Introduction </b></h3>

<h4> What is closures in swift? </h4>

  Closures are self-contained blocks of functionality that can be passed around and used in your code.

<b> How to declare a Closure in Swift? </b> http://fuckingclosuresyntax.com/
  <div>
    <h2>As a <strong>variable</strong>:</h2>
    <code>
      <span class='return'>var</span> closureName: (<span class='parameter-types'>ParameterTypes</span>) -&gt; <span class='return'>ReturnType</span>
    </code>
  </div>
  
  <div>
    <h2>As an <strong>optional variable</strong>:</h2>
    <code>
      <span class='return'>var</span> closureName: ((<span class='parameter-types'>ParameterTypes</span>) -&gt; <span class='return'>ReturnType</span>)?
    </code>
  </div>

  <div>
    <h2>As a <strong>type alias</strong>:</h2>
    <code>
        <span class='return'>typealias</span> <span class='closure-type'>ClosureType</span> = (<span class='parameter-types'>ParameterTypes</span>) -&gt; <span class='return'>ReturnType</span>
    </code>
  </div>
  
  <div>
    <h2>As a <strong>constant</strong>:</h2>
    <code>
      <span class='return'>let</span> closureName: <span class='closure-type'>ClosureType</span> = { ... }
    </code>
  </div>

  <div>
    <h2>As an <strong>argument to a function call</strong>:</h2>
    <code>
      <span class='name'>funcName</span>({ (<span class='parameter-types'>ParameterTypes</span> <span class='return'>ReturnType</span> in statements })
    </code>
  </div>

  <div>
    <h2>As a <strong>function parameter</strong>:</h2>
    <code>
      <span class='name'>array</span>.<span class='func'>sorted</span>(<span class='func'>by:</span> { (item1: <span class='func'>Int</span>, item2: <span class='func'>Int</span>) -&gt; Bool <span class='return'>in return</span> item1 &lt; item2 })
    </code>
  </div>
  
  <div>
    <h2>As a <strong>function parameter with implied types</strong>:</h2>
    <code>
      <span class='name'>array</span>.<span class='func'>sorted</span>(<span class='func'>by:</span> { (item1, item2) -&gt; Bool <span class='return'>in return</span> item1 &lt; item2 })
    </code>
  </div>
  
  <div>
    <h2>As a <strong>function parameter with implied return type</strong>:</h2>
    <code>
      <span class='name'>array</span>.<span class='func'>sorted</span>(<span class='func'>by:</span> { (item1, item2) <span class='return'>in return</span> item1 &lt; item2 })
    </code>
  </div>
  
  <div>
    <h2>As the <strong>last function parameter</strong>:</h2>
    <code>
      <span class='name'>array</span>.<span class='func'>sorted</span> { (item1, item2) <span class='return'>in return</span> item1 &lt; item2 }
    </code>
  </div>
  
  <div>
    <h2>As the last parameter, <strong>using shorthand argument names</strong>:</h2>
    <code>
      <span class='name'>array</span>.<span class='func'>sorted</span> { <span class='return'>return</span> $0 &lt; $1 }
    </code>
  </div>
  
  <div>
    <h2>As the last parameter, <strong>with an implied return value</strong>:</h2>
    <code>
      <span class='name'>array</span>.<span class='func'>sorted</span> { $0 &lt; $1 }
    </code>
  </div>
  
  <div>
    <h2>As the last parameter, <strong>as a reference to an existing function</strong>:</h2>
    <code>
      <span class='name'>array</span>.<span class='func'>sorted</span>(<span class='func'>by:</span> &lt;)
    </code>
  </div>
  
  <div>
    <h2>As a function parameter <strong>with explicit capture semantics</strong>:</h2>
    <code>
      <span class='name'>array</span>.<span class='func'>sorted</span>(<span class='func'>by:</span> { [unowned self] (item1: <span class='func'>Int</span>, item2: <span class='func'>Int</span>) -&gt; Bool <span class='return'>in return</span> item1 &lt; item2 })
    </code>
  </div>
  
  <div>
    <h2>As a function parameter <strong>with explicit capture semantics and inferred parameters / return type</strong>:</h2>
    <code>
      <span class='name'>array</span>.<span class='func'>sorted</span>(<span class='func'>by:</span> { [unowned self] <span class='return'>in return</span> $0 &lt; $1 })
    </code>
  </div>
