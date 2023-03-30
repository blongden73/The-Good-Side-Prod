---
layout: default
---

<div class="gs-wrapper-article">
    <div class="gs-wrapper-blog-inner">
        <div class="gs-container-centered">
        <h2>{{page.title}}</h2>
        <small class="article-date">{{page.date | date_to_string}}</small>
        <img src="{{page.['Main Image']}}">
        <div class="gs-blog-container-inner">
            {{page.content}}
        </div>
    </div>
    </div>
</div>

{% include tg-footer.html %}
{% include tg-footer-base.html %}