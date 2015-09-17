---
layout: post
title:  "Instruction of Theme Installation"
author: "panforest.net"
date:   2015-08-25 07:55:57
meta: "Instruction based on steps how install green freedom default theme trough OpenCart extensions installer and(or) manual installation"
weight: 1
package: "less-theme"
categories: Installation
submenu:
  - { hook: "install-theme-through-opencart-the-extension-installer--brrecommended",       title: "Install theme through OpenCart the extension installer  " }
  - { hook: "theme-manual-installation", title: "Theme Manual installation" }
  - { hook: "if-you-have-fresh-installation-of-opencart", title: "Setup your installation similar to the demo (For fresh installation of OpenCart)" }
  - { hook: "if-you-have-installation-of-opencart-with-own-data", title: "Setup your installation similar to the demo (For installation of OpenCart with custom data)" }
  
---

### Install theme through OpenCart the extension installer  <br>(recommended)


In the OpenCart admin backend, do the following steps:

    Step 1) Go to Extensions > Extension Installer
   
<br>

    Step 2) Upload the {{ page.package }}.ocmod.zip

*If your OpenCart settings of FTP aren't correct or FTP is disabled by your host, during upload file you may will get error “FTP needs to be enabled in the settings” or similar
. In this case you have to install
[QuickFix extension ](http://www.opencart.com/index.php?route=extension/extension/info&extension_id=18892)
 first, then upload the theme ocmod.zip file again*  

    Step 3) Go to System » Settings from the navigation menu.
    
<br>
    
    Step 3) Click the "Store" tab.
    
<br>

    Step 4) Choose the template you uploaded from the "Template" drop-down box.
    
<br>

    Step 4) Click the "Save" button in the upper right corner of the page.

<br>

**That's it. You have successfully activated your new OpenCart template.**


## Theme Manual installation 

    Step 1) Find {{ page.package }}.ocmod.zip  in downloaded package.
      
<br>
    
    Step 2) Extract food_theme.ocmod.zip on local computer
    
<br>
     
     
     Step 3) Upload {{ page.package }} folder (and all folders and files inside) via FTP Client( FileZila or similar) to server. 
     
*Folder patch should looks like **upload/catalog/view/theme/{{ page.package }}/***

    Step 4) Go to System » Settings on OpenCart admin panel 
    
<br>
    
    Step 5) Click the "Store" tab
    
<br>

    Step 6) Choose the template you uploaded from the "Template" drop-down box and 
    Click the "Save" button in the upper right corner of the page.

**That's it. You have successfully activated your new OpenCart template.**

# Setup your installation similar to the demo

--------------------------------------


### If you have fresh installation of OpenCart

----------------------------------

This is quickly way to install our demo site on your server . 
This is recommended for shop owners who have fresh installation of Opencart. 

___Important Note__: Of course , you can use this method if you have store with custom data but keep in mind that data will be replaced_
 
    1) Install green freedom default theme
    
You can  Install theme through [OpenCart the extension installer (recommended)](#install-theme-through-opencart-the-extension-installer--brrecommended) or [manually](#theme-manual-installation)   


<br>

    2) Install helper extension "Bonus Extension - Slideshow Full Width". 

You can find the installation instructions in `full_width_sideshow.zip` file      

<br>
 
    3) Install helper  extension "Bonus Extension - Full Image Manager". 

You can find the installation instructions in `raim2.zip` file

<br>

    4) Copy the all sample images to your server. Path of images should be same as in sample package
     
There are `sample-images-banners.zip` , `sample-images-manufacturer.zip` and `sample-images- products.zip` package of the sample images. Copy all of them to your server.
You can install them  through OpenCart the extension installer or manually. if you want install manually, keep path of images same as in the sample packages .

<br>

    5) Open Home -> Backup & Restore in your admin panel and choose "demo-sample.sql" file from package. Then click on  "Restore" button ( right corner of page )
    
It will set  demo data in your database. It will also set new admin login details ( username: demo, password: demo ), so if you want change it open Home -> Users and edit data for demo user    
 
__That is all.__ 


--------------------------------
 
 
### If you have installation of OpenCart with own data 

----------------------------------

This is recommended for shop owners who do not want to lose already entered data

---------------------------------


#### Full width slideshow on homepage

From downloaded packages find and install "Bonus Extension - Slideshow Full Width". 

_Note for installation : Just unzip `full_width_sideshow.zip` and follow installation instruction in `install_extension_instruction.txt`_

    1) Open Settings->Design->Banners and create new banner 
      ( Recommended width of images are 1348px)
      
<br>
 
    2) Open Modules create Slideshow Full Width.
    Recommended settings : 
                Width : 1348 , 
                Height : 560, 
                Show slider defined style: On // it will append `.full-width-slide` css class to wrapped div so you can add 
    custom css rules for that class
    
<br>

    3) Open Settings->Design-Layout->Homepage and add modules Slideshow full with > your slideshow full name, position : content top, sort order: 1
    


#### Recommended settings of images on store level

    Open Admin panel -> Stores -> Settings and click on edit button 

<br>
    
    Open Image tab and enter values below : 



|--- 
|
| Name  | Width | Height  
|-:|:-:|:-:|:-:
|--- 
|  ------------------------------ | --------------- |----------------------
| Category Image Size | 80 | 80  
|--- 
| 
| Product Image Thumb Size | 380 | 380
|--- 
|   
| Product Image Popup Size | 500 | 500
|--- 
|   
| Product Image List Size | 380 | 380
|--- 
|   
| Additional Product Image Size | 74 | 74 
|--- 
|   
| Related Product Image Size | 380 | 380 
|--- 
|   
| Compare Image Size | 90 | 90 
|--- 
|   
| Wish List Image Size | 47 | 47 
|--- 
|   
| Cart Image Size | 47 | 47
|--- 
|   
| Store Image Size | 268 | 50 
