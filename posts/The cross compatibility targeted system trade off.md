Why do some people use android and other ios?

Why do some people like windows and other MacOS?

Why do some people like to write apps in Java while others dot net.

Why do some people like web apps while others like native apps?

You will find that apps made for one system that just aren't available in the same way on the others systems and one reason for this is because some environments are more cross compatible than others. This compatibility however, comes at a price.

Often cross platform code is slower because it has to run through an interpreter. The java script with web applications is one example. Even Java byte code has to run through extra interpretation before being run.

Often the abstraction layers do not provide the complete functionality of all the systems they target and just provide a subset. Someone developing for Windows using dot net might be able to add context menus to File Explorer but someone using Java may not do that because they are trying to create a consistent experience across systems where adding custom context menus is not possible. Also, web apps do not currently allow for as much data to be stored locally as native apps. A Cross Platform developer might have to support a wider array of hardware such as monitors with different resolutions so they might settle for a simpler UI for speed of development.

The more targeted developer can make more assumptions about Ram availability. While developers in the past have tried to put "Recommended Hardware Requirements" on the box, it can be hard to expect users to check it. Even for the experienced software buyer it can greatly complicate the software availability landscape to the end user.

In summary.
<ul>
	<li>If each individual who uses your app will use it a lot of the time, use native as the experience can be better custom fit.</li>
	<li>If you want your app to be fast use native</li>
	<li>otherwise, provided the first two conditions are not met, if you want to target a large audience use an environment which is more cross platform.</li>
</ul>
&nbsp;
