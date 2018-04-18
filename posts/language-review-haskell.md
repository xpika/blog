I'm going to go through the features of Haskell and state which ones i like and don't and why.

Tuples
Haskell provides special syntax for these which i don't mind. These things are good. they make it so you don't have to define datatypes everywhere. I wish they would also provide syntax for homogeneous tuples too.

List Comprehensions
I thought these were good until I discovered the list monad can do all of this. I think list comprehensions are just used to make examples show with less characters. I don't like them.

Pattern Guards
Since Haskell provides the case syntax i think this one is pretty lame. conditionals are rarely very arbitrary. For that reason i believe i don't use them.

Mutliple declaration pattern matching
I use this because it's convenient but maybe i shouldn't. Haskell's indentation rules can be tricky so sometimes i avoid that confusion by defining functions multiple times with different pattern matching. if i was more confident with case expressions i would always use them instead, so for this i don't like it.

if syntax
Haskell baked this thing into the language which has ultimately low precedents so you can always avoid brackets when using them. brackets seem to be a fact of life so i would prefer if everyone just used an if function. maybe if the if notation could be specified via infix operaters i would be happier.

infix operators.
these things are a god send. they set haskell apart from those lisp languages where you have to keep cranking out the parens (which gives me rsi). they can be hard to master but the more you learn them the more you like them.

type inference
not sure if i would even use Haskell if it didn't have this. gives you the benefits of typing without without typing(on your keyboard). any language that requires more type annoations than Haskell looks like a suspiciously bad language, I'm looking at you Scala.

purity
great feature that i don't know why all languages can't employ. in a world where we are so overwhelmed by data, this kind of meta data is almost essential in my book.

laziness
this thing has its pros and con's. its definitely mind blowing the first time you see it being used and it's very often handy. my current thinking is it often effects performance reasoning badly. When I do get a bug caused by laziness. It's often hard for me to hunt and fix.

type classes
i think of these as overloading. they also work for overloading return types as well. they are very good but i worry about the runtime overhead sometimes.

constructor syntax and record syntax
the fusion haskell creates between enums and record types is amazing. very nifty feature. record syntax is ok but it can pollute the namespace very quickly. i think ghc are fixing that soon.

list sytax.
Daunting at first because there are so many ways to specify a list but useful none the less. I approve.

number model
Haskell has a really great model on numbers. supporting both hardware ints and integers seemlessly. i think most of the reason i use int instead of integer is int takes less time to write. learn to use the functions fromIntegral and round and you will rock the number model quickly.

partial function application
i like this a lot because it allows you to compose functions really quickly. Â this is a gem feature which i would sorely miss if removed.

do notation.
i used to like this alot. that was until i realised that only the second line requires extra indention inHskell. what's wrong with main = getLine >>= \x -> putStrLn x?

Type parameters
Im grateful haskell has this as the type system would be very limited without it. this is  also where Haskell's type inference really shines.
