We live in the web age. For most people it's their most consuming technology. But what is the web? OrÂ more specifically, what counts as aÂ web technology?

One may be tempted to say anything that can make an HTTP Request. But this would make curl or wget web browsers, which would be too restrictive.

One May say it's something that conforms to w3c specfications? But not all browsers implement those specifications and it still begs the question: what is considered a reasonable thing to add to the specification?

I'm not so interested in the specification, but really the concept which lies beneath the browser phenomena. This can be contrasted with the pre-web world which consisted of apps where you ranÂ an application if your machine supported it. The key phrase: "if your computer supported it". Browsers are cross platform by design because they are not implemented directly for aÂ machine, rather a "process virtual machine".

Firstly to explain the difference between a process virtual machine and something like VMware. Process virtual machines don'tÂ virtualize the resourcesÂ that kernels provide such as communication with hardware and time sharing.

But all of this this might make Java or .Net Â web technologies?

The difference in status between virtual machines such as Java and the virtual machine that is the web is today, somewhat an accident of history.

One of the simple concepts that makes a browser work is its ability to load something from a simple location string. This forms a location service. In the old days people used to recite "double you double you double you dot". Nowadays people usually just google the company name.Â Another pivotal function is the ease at which someone can embed a link to another web site and then have that user navigate to it. This is where the whole "web" analogy works. An architecture constructed from one common material that can connect many disperse entities. This is all made easy usingÂ a web browser and cumbersome when using coding things yourself.Â The fact that all pages had to have separate location strings because there was no dynamic HTML at the time made this very easy. This also made the creation of search engines much more viable. Nowadays, one can submit a site map to search engines using there favorite CMS.

There is another reason to it. The base language for the web is HTML. HTML as a DSL and not a GPL like Java has the advantage that it has less features. People that don't know how to set variables don't need to learn to. They don't need to be taught to avoid infinite loops. In fact, the browser executed code in a way which worked even if there were errors in your code. The serial nature of HTML meant parts could be presented even before the whole page had downloaded. This meant a lot when browsers were slow. In theory a java program could include a library to do all this but this would bloat the install.

There is something more fundamental to this however. Computers don't have infinite resources and they are at the mercy of speed requirements. Java was meant to do many more things than HTML so to decrease the download size, much of the functionality is written inÂ  Java itself. In contrast, old web browsers required no direct communication with things such as file systems, 3D, audio adapters etc which meant they could focus making UI fast. With AWT(advanced windowing toolkit) in Java for instance, instead of asking the operating system to draw a button, a button is drawn using lower level primitivesÂ which then in turn communicate with the operating system.

This in turn meant browsers were more efficient. But wait, there's more! MicrosoftÂ didn't likeÂ Sun so much because they competed with them so they did not shipÂ updated java versions with Windows releases. Later on, Apple also barred it along with flash, from the iPhone killing off its last hope.

Lastly, much of the specification for the web is publicly made very available and is quite democratically decided upon through the efforts of the W3C. This can beÂ put in contrast withÂ another virtual machine, flash, which is closed source and can not only can change between vendors happen quickly, but they can be learned about ahead of time.

These days there is much less of a difference between running something like Java and running web technologies. Many websites run extensively on JavaScript which means your browser window can easily use way too much memory or run into an infinite loop.

Browsers support a huge range of capabilities such as web cam support,Â direct audio and even 3D. Java since added a library called swing which could render graphical components faster, in ways whichÂ had the native "look and feel" of the operating system.

I'm not claiming that Java and the web ever had the same goals, but there objectives overlapped a lot. Web technologies managed to jiffy there way into the dominateÂ seat of internet communication by specializing for presenting documents. They were in the right place at the right time and managed to deliver the goods.

Now that we realize web browsers are virtual machines, we can start to re-envisage it in theÂ broaderÂ perspectives of the pastÂ and future. We can see the inadequacies of JavaScript. Too abstractÂ to make a good VM, too primitive to use forÂ good programming language.

We see that the advantages of local storage can make for a really responsive feel that for high use apps are hard to beat with the limitation of small cookie sizes.

We see that there is not much bad about the idea of putting browser scripting language on the server side.

We see that browsers being permissive about broken HTML really shouldn't be so much these days asÂ many web content creators don't edit HTML directly any more.

We see that the complexity of CSS is venturing into areas which make it look stupid in the light of traditional GUIÂ programming technologies.

One novel differentiating factor between .Net,Â Java, Flash and the web is that the web is not managed by one person. It's a community effort. This makes it invincible so long as the publicÂ still want it. This has greatly spurred its interest.

We see that the web is really the most popular virtual machine due to its ubiquity and longevity. Efforts should keep being made to provide that it can execute code in the most efficient way possible, even if it means changing the general target instructionÂ code JavaScript.

To summarize:
<table>
<thead>
<tr class="header">
<th align="left">ProcessVM</th>
<th align="left">Access restricted</th>
<th align="left">Open Source</th>
<th align="left">Community Driven</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">Web</td>
<td align="left">*</td>
<td align="left">*</td>
<td align="left">*</td>
</tr>
<tr class="even">
<td align="left">Flash</td>
<td align="left">*</td>
<td align="left"></td>
<td align="left"></td>
</tr>
<tr class="odd">
<td align="left">Java</td>
<td align="left"></td>
<td align="left">*</td>
<td align="left"></td>
</tr>
</tbody>
</table>
