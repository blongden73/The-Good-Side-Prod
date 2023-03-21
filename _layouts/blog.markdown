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
    <div class="flex space-between">
    {% assign blogs = site.blog %}
        {% for blog in blogs %}
        <a class="blog-post" href="{{blog.url}}">
            <div>
                <img src="{{blog.['Main Image']}}">
                <h3>{{blog.title}}</h3>
            </div>
        </a>
        {% endfor %}
    </div>
    </div>
</div>