---
layout: page
title: All posts
permalink: /posts/
---
<ul>
    <span>
        {{paginator.total_posts}}
    </span>

    {% for post in site.posts %}
    
        <li class="post"
            data-post-language="{{post.language}}">
            <a href="{{ post.url }}">{{ post.title }}</a>
        </li>
    {% endfor %}
</ul>
