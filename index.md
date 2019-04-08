---
layout: default
---
<div class="blurb">
	<h1>Hallo!!</h1>
	<p>Thank's for visiting my website. Sometimes I write technical IT stuff, random blog, or my diary :D <br>
    If you wanna know about me, visit <a href="/about">this</a></p>

    <h2>Latest posts:</h2>
    <hr>
    {% for post in site.posts limit: 5 %}
        <div class="post-preview">
            <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
            <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
            <p>{{ post.excerpt | remove: '<p>' | remove: '</p>' }}<a href="{{ post.url }}" >read more..</a></p>
        </div>
        {% if post != site.posts.last %}
            <hr>
        {% endif %}
   {% endfor %}
</div><!-- /.blurb -->
