---
layout: post
title:  "Workplace of Framework"
author: "natasa"
date:   2015-08-25 20:55:57
meta: "Developers area. Guide about workplace of framework. It will help you to understand how the framework works. Also, it will help you to modify default theme of the framework or create your theme"
weight: 4
categories: workplace
submenu:
  - { hook: "folders-and-files-structure", title: "Green Freedom Framework -  folders and files structure" }
  - { hook: "less-to-css---customise-default-theme-of-framework", title: "Less to css - Customise default theme of framework" }
  - { hook: "html---customise-default-theme-of-framework", title: "HTML - Customise default theme of framework" }
  - { hook: "settings-of-the-framework-for-new-theme", title: "Settings of the framework for new theme" }

---

After installing <a class="page-link" href="{{ '/installation/2015/08/25/framework-installation.html' | prepend: site.baseurl }}">green-freedom framework</a> ,the structure of folders and files should look like below:


{% include structure.html %}

### Less to css - Customise default theme of framework 

We have written  `less` for default framework theme based on <a href="http://bootflat.github.io/" target="_blank"> BOOTFLAT Flat UI KIT </a>.  All `less` files are placed:


    upload/catalog/view/assets/greenfreedom/less/

Main less file in this folder is `theme-variables.less` file. 
It contains definition of theme variables such as colors, font size, background-color for elements … etc.   
Here, you can change value of variables or create new variable  if you needed. Also, this file inherits  
<a href="https://github.com/twbs/bootstrap/blob/master/less/variables.less" target="_banko">default twitter bootstrap less variables</a>
 ( <a href="http://getbootstrap.com/customize/#less-variables" target="_blanko" > see here also</a> )
 so you can overwrite them in this file.
 
 Other `less` files, such as `typography.less`, `breadcrumb.less`, `buttons.less` ..itd , contain css selector and  implementation of theme variables.

Example .

File 'upload/catalog/view/assets/greenfreedom/less/typography.less` looks like:

        //
        // Typography
        // --------------------------------------------------
        h1, h2, h3, h4, h5, h6 {
          color: @darkgray-dark;
        }
        
        /* default font size */
        .fa {
          font-size: floor((@font-size-base * 1.2));
        }
        
        /* Override the bootstrap defaults */
        h1 {
          font-size:@font-size-h1;
        }
        h2 {
          font-size: @font-size-h2;
        }
        h3 {
          font-size: @font-size-h3;
        }
        h4 {
          font-size: @font-size-h4;
        }
        h5 {
          font-size: @font-size-h5;
        }
        h6 {
          font-size: @font-size-h6;
        }


In this file we use variables `@darkgray-dark`, `@font-size-base`, `@font-size-h1` ( and @font-size-h2,h3,h4) to define  header sizes and color. 

These variables are defined in `upload/catalog/view/assets/greenfreedom/less/theme-variables.less` file

Try it. Just run [grunt serve](grunt/2015/08/25/work-with-base-grunt-task.html) task and change variables value or/and their implementation


### HTML - Customise default theme of framework
Path to view is
 
        upload/catalog/view/theme/less-theme/
        
We have kept the default tpl files and css attributes. Here, you can change it

------------------------------

__Note :__ 
 <a href="{{ '/grunt/2015/08/25/work-with-base-grunt-task.html' | prepend: site.baseurl }}">Grunt server</a> task provides detection of every changes on the less, js and tpl files . 
 Your browser will be synchronized automatically when you change those files. 


### Settings of the framework for new theme

You have to have <a href="{{ '/installation/2015/08/25/framework-installation.html' | prepend: site.baseurl }}" target="_blanko">installed framework</a>

In root of your project you will find `package.json` file . At the end of file you will find grunt settings :
 
        ...
                    
        "boostrapPath": "bower_components/bootstrap/",
        "frameworkPath": "upload/catalog/view/assets/greenfreedom/",
        "themeFolder": "less-theme",
        "themeImgFolder": "less",
        "browserSyncProxy": "http://localhost/ocTest/upload/index.php"
          
<br>

__boostrapPath__

_path of boostrap. Keep it same as is it_

__frameworkPath__

_path to less,html-template and js files of frameworks. - You will change it when you want create new theme ( [see example](#exampl-of-new-setup))_

__themeFolder__

_Name of your theme folder. You will change it when you want create new theme ( [see example](#exampl-of-new-setup))_

__themeImgFolder__

_Name of images folder ( Good practice is to keep all images of a theme in one folder) -You will change it when you want create new theme ( [see example](#exampl-of-new-setup))_

<hr>

####Exampl of new setup

For example , we want create new theme for books shop .

__Step 1__ 

Create folder `books` ( you can call it how want) in `upload/catalog/view/theme/`

__Step 2__
 
Copy all folders and files from `upload/catalog/view/theme/less-theme/` to your new folder `upload/catalog/view/theme/books`

<hr>
_Now you have  necessary html ( .tpl ) files_
<hr>  
  
__Step 3__

Create folder `books-framework` ( you can call it how want) in `upload/catalog/view/assets/`

__Step 4__
 
Copy all folders and files from `upload/catalog/view/assets/greenfreedom/` to your new folder `upload/catalog/view/assets/books-framework/`

<hr>
_Now you have  necessary frameworks  files_
<hr>  
  
    



 

