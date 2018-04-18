Haskell, the language of pretty lambda syntax. What are the fruits of this forest? Here, I will make some propaganda about it.

There are not that many things written in Haskell. You could probably count the ones people use on your hand.
<ul>
	<li>Xmonad (Window Manager)</li>
	<li>Pandoc (Convert between textual document formats)</li>
	<li>Git Annex (Syncing)</li>
        <li>Gitit</li>
</ul>
Darcs used to be bigger but most haskellers have moved to GIt already. It may seem unfair to include GHC, but given how complex a compiler it is, It says a lot about Haskell. Pugs used to be big around decade ago but now how slipped out of attention. 

There are a few compilers, most noteably haskell ones such as GHC, which are written in Haskell among some languages which have features that are not present in haskell these are
<ul>
	<li>GHC</li>
        <li>Agda</li>
	<li>Idris</li>
        <li>Elm</li>
</ul>

Then there are Haskell libraries. Some of these libraries are quite exceptional. Again there are not many popular ones, but here is a list.
<ul>
	<li>Diagrams (For rendering vector images)</li>
	<li>Parsec (For parsing text)</li>
</ul>
Then there are git libraries that on there own, don't do anything, but can make your code much more fancy. A good example of these are
<ul>
	<li>Monad (Type class to compose functions with simple do keyword and arrows &lt;- which you can customize the behavior of per type constructor (Term sourced from on category theory!))</li>
	<li>Lens (unite getters and setter into a single object)</li>
	<li>Pipes or Conduit (Compute over streams of data without creating temporary data structures which cause your application to run out of memory).</li>
	<li>Arrows (like monad, but for constructors with an arity of 2)</li>
	<li>Comonad (Monad, in reverse)</li>
	<li>Functor,Applicative,Foldable,Traversable (more typeclasses to generalize functions)</li>
	<li>Free Monad.</li>
</ul>
There are a couple of things I might like to try out. These are apparently good.
<ul>
	<li>Shake (make alternative)</li>
	<li>music-suite (render music notation)</li>
</ul>
There is also some pretty good libraries for dealing with parallelisms. This is also apparently good.
<ul>
	<li>STM (Atomic variables)</li>
	<li>Parallel strategies (There is a book on these).</li>
</ul>
Then there are a few more apps written in haskell to help people code haskell
<ul>
	<li>Ghci</li>
	<li>Pointfree (compress haskell code into smaller haskell code)</li>
	<li>Yi (Text editor)</li>
	<li>Leksah</li>
	<li>djinn (Generate Code from type signatures)</li>
	<li>cabal</li>
	<li>hackage</li>
	<li>hoogle</li>
	<li>haddock</li>
	<li>Template Haskell (useful with Lens library)</li>
	<li>Generics</li>
	<li>GHC API</li>
</ul>
Haskell has a interesting collection of data structures. Here I will mention a couple.
<ul>
	<li>ByteString (Serialized, strict or non strict)</li>
	<li>Sequence (another lIst type, this time based on trees)</li>
</ul>
Everything listed is open source and there are some non open source ones, but I haven't mentioned them.
