# ojt-monitoring-system-api-installation-guide
a guide of running the ojt-monitoring-system via windows linux subsystem
# Reminder Just Keep Entering Y on dependecies installation!!!!

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
and paste the .deb
# Install the mongodb
enter 
<pre>ls</pre>
and the .deb file name will show copy the name and enter
<pre>sudo dpkg -i ./thefilename.deb </pre>
and wait for it to install!!!
# mongosh installation
enter
<pre> curl -fsSL https://www.mongodb.org/static/pgp/server-8.0.asc \
  | sudo gpg -o /usr/share/keyrings/mongodb-server-8.0.gpg \
    --dearmor</pre>
and 
<pre> echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-8.0.gpg ] https://repo.mongodb.org/apt/ubuntu jammy/mongodb-org/8.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-8.0.list</pre>
then
<pre>sudo apt-get update
sudo apt-get install -y mongodb-mongosh</pre>
# now lets clone the ojt-monitoring-system-api
<pre>sudo apt install git
git clone https://github.com/ojtmonitoringsystemph/ojt-monitoring-system-api.git
cd ojt-monitoring-system-api.git</pre>
# Create the .env file
first
<pre>sudo apt install vim</pre>
then
<pre>vim .env</pre>
click i to the keyboard and paste this
<pre>PORT=5000
MONGODB_URI=mongodb://localhost:27017/ojt-monitoring-system
NODE_ENV=development
JWT_SECRET=your-secret-key
CLOUDINARY_CLOUD_NAME=your-cloudinary-name
CLOUDINARY_API_KEY=your-api-key
CLOUDINARY_API_SECRET=your-api-secret
</pre>
then save by clicking esc and enter 
<pre>:wq</pre>
to save and quit 
then register register your pc ip address on Kuya Dariel's given acc on (cloud.mongodb.com) navigate to the left side and find network and all your pc IP address
# after that go back to the wsl and enter
<pre>npm install</pre>
just follow what i requested remember to always use "sudo" (sometimes it will ask you to force it but linux will provide the command line just copy it to force it)
then
<pre>npm run dev</pre>
then if it says server running or connected go to your browser and enter
<pre>localhost:5000/api/docs/#/</pre>

