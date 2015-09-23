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

---

After installing <a class="page-link" href="{{ '/installation/2015/08/25/framework-installation.html' | prepend: site.baseurl }}">green-freedom framework</a> ,the structure of folders and files should look like below:


{% include structure.html %}

### Less to css - Customise default theme of framework 

We have written  `less` for default framework theme.  All `less` files are placed





### HTML - Customise default theme of framework


### Create new theme

You ’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve --watch`, which launches a web server and auto-regenerates your site when a file is updated.

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
