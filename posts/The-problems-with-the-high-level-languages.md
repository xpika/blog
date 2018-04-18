This article I'm going to try and claim why the clunky old lower levels like Java and to a greater extent C are still popular.

I think the biggest problem, which I know is a real stick in the mud for higher level programmers, is speed.

"But my application doesn't require speed","I find it's IO bound" you say.

While your application does not require speed now, it may in future scenarios. An algorithm written in a low language can be used in much more demanding tasks. Calculating a winning poker hand may be small work to compute, calculating the chances of which particular moves to win are a much heavier computation.

You might want to run software on a machine which is running less powerful hardware than your own. There also seems to be a trend in porting a more sophisticated software to devices with less powerful machines. Smart phones are an example of this.

"I will just scale the hardware" you say, if you have the money that sounds like a great solution, but what happens when the money runs out as economics will ensure. Some algorithms, even with the most powerful hardware available may not run fast enough for your needs.

"I will adapt my software when necessary". There are a few techniques to this. Advanced features of a language could be substituted with more the more primitive operations that the language provides. One could refactor out the slow parts of the code and write them in a lower level language via remote procedure call or foreign function interface. A more sophisticated algorithm could be employed which uses of a special data structure or calculation technique.

All of these sound like a good idea, but whereas you had one problem before, you know have two, thus proving the point I was trying to make. Sometimes you can get away in lower level languages just with brute force algorithms. See some project Euler solutions for an example of this.

Last post I said that high level languages were more portable. While this is true in the case of the source code this is not always so true of the application more generally.

Both the developers and users still often have the task of installing the latest flash or JVM or Dot net framework or particular browser for example the higher level general purpose language. Generally, the more high level  the language is the more esoteric it is will be and the less likely the dependencies will already be installed.

Building software, that is the packing and distribution of software is in my opinion, highly underrated, and it's for this reason along with others that a program written using the win32 api or libc or java have been so lucrative. The better job it does at being easier to move the application to another machine, often the worse the software will perform. Programming languages that utilise virtual machines are a good example of this. The more high level constructs the language supports usually means the language will be slower. Ruby, although known really flexible, is also known for being particularly slow.

Code written in low level languages is generally less esoteric and commonly used. There is another benefit to this. A more common language means more development resources.  I guess a counter to this might be CPAN which currently has over 130,000 modules, but I wonder as to what portion of those packages are quality given how many people are using them today.

If you go up one step further to something like Java, you get massive of very high quality jars such as SAX and swing and JDBC available to you.

The more esoteric higher level languages are usually more radical in there software support as well. If you want to install a python library there are now many variants for different versions you might want. If you do a search for a python for example in your package manager of choice, you may be confronted with question of which version? 2.4, 2.5, 2.6, 2.7, 2.8 ,3 etc. lower level languages have these sorts of problems too but my point is that they are often very comparable to there higher level counterparts.

I find high level languages like php and python usually do well, until the language fragments.

This creates a very interesting what I will call "honey moon" phase of a programming language. The feeling the programmer gets when they are using a language that has just come out and think it will never change.

So there is my article on why high level languages are not as practical as they might seem at first. Many of the things I've mentioned have just been circumstantial and not really to do with the languages fundamentally. Still, this has been a bit of rude awakening for me which I wanted to share. The whole idea summarizes itself in what I will call "The rule of high level code".

> "Any sufficiently practical application written in high level will be rewritten in low level."
