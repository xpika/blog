<strong>1. Command Line options</strong>

In unix, commands have parameters, but this is not standardized. Sometimes a parameter will be expressed as:
<code>
command -osomething
command -o something
command --o=something
command --opt something
command o something
</code>

There is no consistency. This should be standardized. CGI is a better alternative to this.

<strong>2. Command Line output</strong>

In unix, commands have outputs in columns, however, some columns contain spaces. since columns are seperated by spaces and not tabs, you have to count more spaces until you can extract the data you want. An example of an alternative to this is Windows powershell where commands output XML.

<strong>3. Filesystem Organisation</strong>

In unix. Files are divided by type not by application. This means executables are in /bin and config files in /etc etc (no pun intended).
This makes uninstallation and moving apps between servers almost impossible. Mac does this better as apps are contained in a single directory.
 
