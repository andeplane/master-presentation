master-presentation
===================

Prerequisites:
	- Node.js (http://nodejs.org/) 
	- Grunt (http://gruntjs.com/getting-started#installing-the-cli)

Installation of prerequisities:
	Ubuntu:
 		sudo apt-get install nodejs npm; sudo npm install -g grunt-cli; 
 	Mac:
 		Install Homebrew
 			ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"; brew update;
 		Install Node.js and Grunt
 			brew install node; npm install -g grunt-cli

Instructions (assuming you are in this directory):
	- Clone reveal.js in parent directiry
		cd ..; git clone https://github.com/hakimel/reveal.js.git; cd reveal.js
	- This presentation was made with commit 131c00689a4c7a18e5c991fc8102347e4594b5d4, so if it doesn't work, checkout this commit
		git checkout 131c00689a4c7a18e5c991fc8102347e4594b5d4 .
	- Copy the content of reveal.js into master-presentation-folder, but don't replace this readme
		rsync -av --exclude=".*" --exclude="README.md" --exclude="index.html" * ../master-presentation
	- Change to master-presentation directory
		cd ../master-presentation
	- Install dependencies (sudo might be required)
		sudo npm install
	- Start the webserver
		grunt serve
	- Open in browser
		http://127.0.0.1:8000/index.html

Instructions (one-liner):
	cd ..; git clone https://github.com/hakimel/reveal.js.git; cd reveal.js; rsync -av --exclude=".*" --exclude="README.md" --exclude="index.html" * ../master-presentation; cd ../master-presentation; sudo npm install; grunt serve