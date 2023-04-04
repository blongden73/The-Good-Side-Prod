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
    {% assign commitments = page.['Our Commitment'] %}
    {% for commitment in commitments %}
        <div class="gs-impact-container-inner">
        <div class="gs-impact-table">
            <div class="flex space-between">
                <div class="left-logo"><img src="{{commitment.Logo}}"></div><div class="right-descripotion"><p class="commitment-description">{{commitment.Description}}</p></div>
            </div>
        </div>
        </div>
    {% endfor %}
</div>

{% include tg-footer.html %}
{% include tg-footer-base.html %}