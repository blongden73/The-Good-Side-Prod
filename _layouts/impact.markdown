---
layout: default
---

<div class="gs-impact-header">
    <div class="gs-container-centered">
        <h1 class="impact-title">{{page.title}}</h1>
    </div>
    <div class="big-circle"></div>
</div>
<div class="gs-impact-header">
    <div class="gs-container-centered">
        <div class="impact-content">
            <div class="gs-impact-container-inner">
             {{page.content | markdownify}}
            </div>
        </div>
    </div>
</div>
<div class="gs-impact-badges">
    
</div>

{% include tg-footer.html %}
{% include tg-footer-base.html %}