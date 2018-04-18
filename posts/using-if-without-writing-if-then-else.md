Haskell has a keyword <code>if</code> which allows you to branch your execution based on some predicate. 

<code>if</code> is not a regular function. It might be more useful if it was.

Say i want to replace all occurrences of a character in a string. similar to the unix too sed.

this could be written like this
<code>

> let replace x y xs = map (\z->if z==x then y else z) xs

> replace '.' '!' "Yes. I agree."
"Yes! I agree!" 

</code>

However, what if I want to write it using less points? Because <code>if</code> is not a regular function I can't use it on its own. 

The function <code>if'</code> can easily be written as follows.
<code>
> let if' p a b = if p then a else b
</code>

Now replace can be re-written as
<code>
> let replace x y xs = map (if'.(x==)>>=($y)) xs
</code>

much better.
