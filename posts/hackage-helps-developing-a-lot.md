If you write a haskell application and want to transfer it somewhere else you could do so by uploading it to github. That way, each client can grab a copy with a simple:

<code>git pull &lt;repo-url&gt;</code>

If however, you upload it to <a href="http://hackage.haskell.org">hackage</a>, both the downloading and installation can be done in a simple:

<code>cabal install &lt;package-name&gt;</code>

This is coupled by the fact that all dependencies will also be downloaded if also available makes cabal very convenient.

If you put a package on hackage and then need to reference it as a dependency in another project its as simple adding 

<code>build-depends: &lt;other-package-name&gt;</code>

to your .cabal file.

Uploading to hackage will also automatically generate your haddock documenation for you.

Then there is the advantage that hackage also makes it easier for others to to find, download and install your package. This is why hackage exsists. Hayoo and Hoogle also index the functions found in the libraries on hackage.

While hackage is a centralised system. It's still a very convenient option for haskell software distribution.
