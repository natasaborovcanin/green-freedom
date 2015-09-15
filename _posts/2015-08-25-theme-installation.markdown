---
layout: post
title:  "Instruction of Theme Installation"
author: "panforest.net"
date:   2015-08-25 07:55:57
meta: "Instruction based on steps how install green freedom default theme trough OpenCart extensions installer and(or) manual installation"
weight: 1
package: "less-theme"
categories: Installation
---

### Install theme with OpenCart the extension installer  <br>(recommended)


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


## Manual installation 

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

## Setup your installation similar to the demo
If you want to have site like our demo site do following

### Full width slideshow on homepage

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
    
 Property name | Width | Height    
 ------------- | ----- | ------    
Category Image Size | 80 | 80 

Product Image Thumb Size

380

380
Product Image Popup Size

500

500
Product Image List Size

380

380
Additional Product Image Size

74

74
Related Product Image Size

380

380
Compare Image Size

90

90
Wish List Image Size

47

47
Cart Image Size

47

47
Store Image Size

268


-------------------------------
    
1) Create slideshow images and banner images in settings/banners
    ( For slideshow full with behind header use images with width 1348px.
    For banner images on homepage use images with width 1140px ,or download images from demo store)
    
2)Install Slideshow Full Width
    You will get message that will be overwritten file "catalog/view/theme/food/template/module/slideShowFullWidth.tpl"
    	Click on continue button
    ( In modules/Slideshow Full Width chose banner which you created for slideshow,
     we put width 1348px and height you need.
    select *Show slider defined style / ON*
    (This is option which puts slideshow behind header in this theme. Slideshow Full Width always have first position in page layout.
    It's been used on home page.If you chose option /OF it will be displayed default Slideshow Full Width below header)
    Enable it and save it
3)Install two banners from modules/banner, put them related banner to display
    (In demo store with of banners is 1140) Enable it and save it
4)Install latest and featured module from module, add product to display
  ( use limit:4, wdth:390, height:390, if you using demo product images)Enable it and save it
5)Go to settings/design/layout/homepage
    add modules
    Slideshow full with>your name, position: content top, sort order: 1
    Banner>your name, position: content top, sort order: 2
    Latest>your name, position: content top, sort order: 3
    Banner>your name, position: content top, sort order: 4
    Featured>your name, position: content top, sort order: 5
    Carousel>carousel-home page, position: content top, sort order: 6
    save it.
    That's it!








You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve --watch`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
