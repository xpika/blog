In the old days. like around the time of Euclid, it was popular to do maths geometrically and not so much using algebra. There is much to say about the intuition that can be easily obtained using graphical aids. As time progressed this fell out of favor to algebraic which is a more code based solution.

Some things are just harder to express graphically. Geometry involving 2 dimensions is not so bad, but as you start adding more dimensions it quickly becomes a mess.

Likewise programming languages could be given more graphically oriented aids. For example consider a language that looks like this

<img class="alignnone size-medium wp-image-593" src="http://codekinder.com/wordpress/wp-content/uploads/2016/03/lang2-300x207.png" alt="lang2" width="300" height="207" />

If calling functions within the file follows the line method then misspelling a function is impossible. (In this example multiply is assumed to be  primitive)

The problem is that there are other non-graphical solutions to achieve similar results. Static analyzers can check if variables are in scope for you and print line numbers where code is defined. The non graphical solution scales better as well. Imagine a program with a lot of variables. Keeping track of where each value is coming from would become like trying to follow a poorly laid out switch cabinet.

Also, consider a really big number like 12345. I could draw a whole heap of lines with crosses but that wouldn't get you very far quickly. The shortest way to summarize it with something close to its binary representation.

Graphical programming has to not just overcome the convenience of text based coding, but it also has to overcome any amendments that might substitute for the same techniques.

As an analogy, consider a piano. It might be easier for players if a crank was installed to perform a key change. This however might make the piano much more expensive to manufacture and repair. Cars too could be fitted with pedestrian light sensors but they may not work very well in the all cases like in a snowstorm or when the words walk are replaced with a picture of a green man.

In the same vein. it may be easier in the short term to change the minds of developers than recreate the text interfaces which are used to code.
