---
layout: post
title: Setting up a blog
comments: true 
published: true
---

## Hello World
With this post, i've sucessfully found out how to setup a blog hosted by [Github pages](http://pages.github.com/)
using [Jekyll](http://jekyllrb.com) and [poole](https://github.com/poole/poole).

## Blog setup wrapup
The procedure is documented very good at [joshualandes blog](http://joshualande.com/jekyll-github-pages-poole/)
I've done only minimal 'additions':

- added a navigation bar at the top of each post to quickly navigate through the posts
- removed the related posts section, because it seems to only show the posts which are nearest by date
- show only the first 50 words on the front page
- show more blog posts on the front page

### Navigation bar on top
Just copy&paste
{% highlight md %}
<div class="pagination">
  {% if paginator.next_page %}
    <a class="pagination-item older" href="{{ site.baseurl }}page{{paginator.next_page}}">Older</a>
  {% else %}
    <span class="pagination-item older">Older</span>
  {% endif %}
  {% if paginator.previous_page %}
    {% if paginator.page == 2 %}
      <a class="pagination-item newer" href="{{ site.baseurl }}">Newer</a>
    {% else %}
      <a class="pagination-item newer" href="{{ site.baseurl }}page{{paginator.previous_page}}">Newer</a>
    {% endif %}
  {% else %}
    <span class="pagination-item newer">Newer</span>
  {% endif %}
</div>
{% endhighlight %}
to the position where you want it in index.html
