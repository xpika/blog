In the old days. Most services did not use HTTP. FTP. IRC, SMTP specify there own language for communication. Nowadays, many more things are brought via Http. Social media apps. RSS. Git over http. Email APis over http. This site for example.

I can think of some examples why this is the case.
<ol>
	<li>HTTP performs slow so restricted networks would be more likely to allow it as they are less likely to connect to things like file sharing networks.</li>
	<li>HTTP is connection-less (or conventionally so (see long polling) which reduces memory consumption .</li>
	<li>HTTP can be tested in a web browser which is slightly easier than using telnet.</li>
	<li>HTTP supports compression and encryption headers.</li>
	<li>HTTP has a standard for submitting the domain name allowing for Virtual Hosts</li>
	<li>HTTP supports basic auth.</li>
	<li>Probably other stuff.</li>
</ol>
Sockets does not provide this stuff out of the box and you would have to roll your own. Web sockets are the connectionful version of HTTP.

HTTP of course adds it's own overhead with the HTTP method names like GET but if you can get past that, it can be pretty lucrative.
