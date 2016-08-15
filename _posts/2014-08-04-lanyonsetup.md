---
layout: post
title: Using Jekyll, Poole and Lanyon to setup my github user page
categories: []
tags: [code]
description:
comments: true
---

[Github pages](https://pages.github.com/) is where I learnt github repositories could be used to host a website using [jekyll](http://jekyllrb.com/). This website was created using the theme [lanyon](https://github.com/poole/lanyon), which derives from [poole](https://github.com/poole/poole). Jekyll, Poole and Lanyon are all characters from [_The Strange Case of Dr. Jekyll and Mr. Hyde_](http://en.wikipedia.org/wiki/Strange_Case_of_Dr_Jekyll_and_Mr_Hyde).

### General custimizations
* Added Disqus comments using [Joshua Lande's guide](http://joshualande.com/jekyll-github-pages-poole/)
* Added Google analytics using [the same guide](http://joshualande.com/jekyll-github-pages-poole/) 
* Added SEO streamlining from [here](http://jethrokuan.github.io/2013/12/20/SEO-with-Jekyll.html)
* Added CNAME from [here](https://help.github.com/articles/tips-for-configuring-a-cname-record-with-your-dns-provider)
* Added a favicon (mouse brain with the cerebellum coloured - posterior-lateral view)
* Added tags page
* Added archive page

### CSS and head.html modifcations
* Added the font-awesome css in head.html and then used its icons to display my social media presence in the sidebar. 
[Future resource for help with font-awesome](http://fortawesome.github.io/Font-Awesome/examples/)

### Sidebar modifications
* Added my gravatar to the sidebar
* Added social links with _config.yml settings I set-up and font-awesome icons

My repository can be found at [https://github.com/psteadman/psteadman.github.io](https://github.com/psteadman/psteadman.github.io)

### Things I'd like to explore
* Medium and their website - [https://medium.com]()
* [Pandoc](http://johnmacfarlane.net/pandoc/) with [github](https://github.com/jgm/pandoc)
* HTML and CSS
* [Bootstrap](http://getbootstrap.com/) - from Mark Otto

### Ideas
* Code a bar below current header with most popular tags (count beside) and serve as link to view all posts with that tag
