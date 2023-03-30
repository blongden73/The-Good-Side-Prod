---
layout: default
---

<div class="blog-wrapper-title">
    <div class="gs-container-centered">
        <h1>The Good Side Blog</h1>
    </div>
</div>
<div class="blog-wrapper">
    <div class="gs-container-centered">
    <div class="flex space-between">
    {% assign blogs = site.blog %}
        {% for blog in blogs %}
        <a class="blog-post" href="{{blog.url}}">
            <div>
                <div class="blog-image">
                    <img src="{{blog.['Main Image']}}">
                </div>
                <h3>{{blog.title}}</h3>
            </div>
        </a>
        {% endfor %}
    </div>
    </div>
</div>