# ros-agriculture.github.io
Website for rosagriculture.org.

![Hugo](https://github.com/ros-agriculture/ros-agriculture.github.io/workflows/Hugo/badge.svg)

This branch (hugo) contains the Hugo source files. The content of the website is deployed to the master branch. Manual modifications to the master branch will be overwritten if the source files are modified. In order to debug the changes, you can make and test the website locally on your computer.

## Make the website locally on Ubuntu

* Install node js and npm: ```sudo apt install nodejs npm```
* Install postcss-cli globally: ```sudo npm install -g postcss-cli```
* Install autoprefixer globally: ```sudo npm install -g autoprefixer```
* Install Hugo with: ```sudo snap install hugo --channel=extended```
* Clone the repository: ```git clone https://github.com/ros-agriculture/ros-agriculture.github.io.git```
* Go inside the folder: ```cd ros-agriculture.github.io```
* Install required node packages: ```npm install```
* Run hugo and serve the website locally: ```hugo serve```

## Resources

- [Hugo](http://gohugo.io)
- [Docsy theme for Hugo](https://www.docsy.dev/)
- [Host Hugo on GitHub Pages](https://gohugo.io/hosting-and-deployment/hosting-on-github/)
