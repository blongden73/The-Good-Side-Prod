---
layout: default
---

<div class="blog-wrapper-title">
    <div class="gs-container-centered">
        <h1>The Good Side Zine</h1>
    </div>
</div>
<div class="blog-wrapper">
    <div class="gs-container-centered">
    <div class="flex space-between">
    {% assign zines = page.Zines %}
        {% for zine in zines %}
        <a class="zine-post" href="{{zine.url}}">
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

{% include tg-footer.html %}
{% include tg-footer-base.html %}