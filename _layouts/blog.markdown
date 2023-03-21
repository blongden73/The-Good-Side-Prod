---
layout: default
---

<div class="blog-wrapper-title">
    <div class="gs-container-centered">
        <h1>Blog page title</h1>
    </div>
</div>
<div class="blog-wrapper">
    <div class="gs-container-centered">
    <div class="flex">
    {% assign blogs = site.blog %}
        {% for blog in blogs %}
        <div class="blog-post">
            <img src="{{blog.['Main Image']}}">
            {{blog.title}}
            {{blog.content}}
        </div>
        {% endfor %}
    </div>
    </div>
</div>