Docker implements containers. Operating system containers used to be more commonly refereed to chroot jails. A "Jail" highlighting the security aspect, however Docker containers have many other uses.
<ul>
	<li>Configuration Management. You can think of a docker file as like a build script.</li>
	<li>Distrubution: Pushing to docker hub is a great way to share environments</li>
	<li>Containers isolate processes making debugging easier. Consider how fewer processes there are when typing ps aux.</li>
	<li>Containers can use different distros to the host operating system and are specifyable to the tagged version simply with a one-liner on top of the docker file</li>
	<li>Docker adds an extra layer of security making it harder for hackers to jump from one set of processes to another such as the underlying operating system. If they hack the container, you can just rebuild it and the host operating system should be pretty unscathed.</li>
	<li>Docker can caches operating system builds meaning adjusting the configuration of your servers can be faster.</li>
	<li>Docker shares common build assets reducing disk space and build time.</li>
	<li>Docker implements a network abstraction layer meaning programs running on the same port are not an issue.</li>
	<li>Containers are isolated environments so the installation of one thing won't conflict with another.</li>
</ul>
