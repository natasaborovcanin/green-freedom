---
layout: post
title:  "Framework Installation Instruction"
author: "natasa"
date:   2015-08-25 07:55:57
meta: "Developers area. Guide about install framework. It will help you to set up workplace for customised or create new the theme"
weight: 2
categories: installation
submenu:
  - { hook: "requirement",       title: "Requirement" }
  - { hook: "green-freedom-framework-installation-instruction", title: "Green Freedom Framework Installation instruction" }
  - { hook: "folders-and-files-structure", title: "Folders and files structure after installation" }
  
---

### Requirement:

To work with green freedom framework you have to have installed :

* [Node.js/npm](https://docs.npmjs.com/getting-started/installing-node){:target="_blanko"}
 
* [bower](http://bower.io/#install-bower){:target="_blanko"}

* [grunt/grunt-cli](http://gruntjs.com/getting-started){:target="_blanko"}

### Green Freedom Framework Installation instruction

    In downloaded package find `framework.zip` and unzip it


<br>

    Copy `package.json` , `Gruntfile.js` and `bower.json` files and `grunt` folder to root of your Opencart Installation
     
<br>

Run command below

    bower install
    
This command will create `bower_components` folder and put into it  all dependencies defined in  `bower.json` file

<br>

Run command below

     npm install

This command will create `node_modules` folder and put into it  all dependencies defined in  `package.json` file

<hr>


After those actions your structure of  folders and files  should look like:

{% include structure.html %}

More information about folder and files of the framework you can find 
<a class="page-link" href="{{ '/workplace/2015/08/25/workplace-of-framework.html' | prepend: site.baseurl }}">here</a>

