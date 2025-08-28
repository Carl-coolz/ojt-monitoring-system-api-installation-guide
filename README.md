# ojt-monitoring-system-api-installation-guide
a guide of running the ojt-monitoring-system via windows linux subsystem

# First step is to install WSL(Windows Subsystem Linux)
<pre> wsl --install </pre>

# After Installation
restart your laptop/pc and after that, open your cmd and input
<pre> wsl </pre>
wait for it to load and enter your username and password you will set and later on you will see this 
# example@DESKTOP-123456:/mnt/c/Users/Example$
you need to enter
<pre> cd </pre>
first before proceeding, then go update your linux system enter
<pre> sudo apt update </pre>
then install nodejs npm and mongodb 
Download mongodb here! (https://www.mongodb.com/try/download/community)
on platform select debian and download the .deb file!

# to install nodejs and npm, go to the wsl and enter
<pre>sudo apt install nodejs npm</pre>
after that copy the .deb file you download on linux directory, open file explorer and navigate to the left side until you find the penguin(linux) icon
and open it and go to the 
<pre>Ubuntu\home\YourUserName</pre>

