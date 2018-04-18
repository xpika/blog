Here is some propaganda for the Clojure language.

Let's benchmark the Java Clojure compiler against a Javascript interpreter based on v8(nodejs).

Write the two files as follows:

fib.clj
<pre>(defn fib [x] 
 (if 
  (&lt; 2 x) 
  (+ (fib (- x 1)) 
     (fib (- x 2)))
  1))

(println "fib: " 38)
(println (fib 38))</pre>
fib.js
<code></code>
<pre>function fib(x){
 if (x &lt;2) {
   return 1;
 } else {
   return fib(x -1) + fib(x-2);
 }
}

console.log("fib: "+38);
console.log(fib(38));</pre>
Now we try to benchmark them.
<pre>$ time clojure fib.clj
fib:  38
39088169

real	0m5.531s
user	0m5.305s
sys	0m0.220s

$ time node fib.js
fib: 38
63245986

real	0m1.677s
user	0m1.514s
sys	0m0.072s
</pre>
As you can see Clojure took a lot longer. But what if I had a long running app like a web server?
Maybe Clojure just takes longer to load?

In the spirit of presentation driven development PDD this is where a tool I have written comes in. It's called timeconsole. At the moment, you can get it by

<code>cabal install timeconsole</code>

Now we try to benchmark them again.
<pre>$ timeconsole clojure fib.clj
1:2.15314:fib:  38
1:2.011855:39088169

$ timeconsole node fib.js
1:2.15314:fib:  38
1:2.011855:39088169

</pre>
As you can see Clojure takes longer to load than node (approx. 2 seconds vs 0.2 seconds), but clojure is still slower even when start up time has been factored out. I entitled this article with the notion that clojure would be faster, so what to do here?

Type hints to the rescue!

If we limit ourselves to the long number type we can get the code to run faster.

fib2.clj
<code></code>
<pre>(defn fib ^long [^long x] 
 (if 
  (&lt; 2 x) 
  (+ (fib (- x 1)) 
     (fib (- x 2)))
  1))

(println "fib: " 38)
(println (fib 38))</pre>
<pre>$ timeconsole clojure fib2.clj

1:2.187285:fib:  38
1:0.494628:39088169
</pre>
And so it does. I could use something like ASM.js where I think it would beat clojure, but since I don't have it installed, I've left it there.

You can get the source for this article <a href="https://github.com/xpika/presentations/tree/master/blog/clojure_v_js">here</a>
