Say you have this docker container, but you want to expose a port that is not already open. One good way is to save the image and restart. This however, will cause some downtime. You also may not want any process to stop because you have not added all the daemons to your startup script. This may lead to "sad times".

One cool way to expose this port is to is by using a reverse SSH tunnel. Reverse tunnels require specific SSH daemon settings and you also may not wantÂ to be bothered ensuring that it's set right. Instead, a docker container can be run specifically to run SSH for this purpose. The command to do this, image provided by docker user tifayuki,Â is as follows.
<pre class="lang:default decode:true  ">docker run -d -e ROOT_PASS=mypass -p 23:22 -p 81:81 tifayuki/reverse-ssh-tunnel
</pre>
Set mypass to the ssh password you want to use toÂ for the reverse tunnel.

<span style="line-height: 1.71429; font-size: 1rem;">This command will expose port 81 on your container. port 23 is chosen as the ssh server that will be used for reverse tunneling.</span>

Then run this for the container you want a port exposed on. your.domain.name being your external domain or IP address.
<pre class="lang:default decode:true">docker exec -it YOUR_CONTAINER_IDÂ ssh -p 23 -R 81:localhost:81 your.domain.name
</pre>
