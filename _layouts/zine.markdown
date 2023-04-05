---
layout: default
---

<div class="exit-intent-cirlce exit zine-email">
  <h1 class="h1">Get the Good Zine</h1>
  <div id="mc_embed_signup">
  <form action="https://thisisthegoodside.us19.list-manage.com/subscribe/post?u=a747a9891de6f7294a56d05ab&amp;id=4bda985eab" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate mc-form" target="_blank" novalidate>
      <div id="mc_embed_signup_scroll">
  <div class="mc-field-group">
    <input type="email" value="" placeholder="Email address" name="EMAIL" class="required email" id="mce-EMAIL">
  </div>
    <div id="mce-responses" class="clear">
      <div class="response" id="mce-error-response" style="display:none"></div>
      <div class="response" id="mce-success-response" style="display:none"></div>
    </div>    <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
      <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_a747a9891de6f7294a56d05ab_4bda985eab" tabindex="-1" value=""></div>
      <div class="clear"><button type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button">Subscribe</button></div>
      </div>
  </form>
  </div>
</div>

<div class="page-blocker">

</div>

<div class="blog-wrapper-title">
    <div class="gs-container-centered">
        <h1>The Good Side Zine</h1>
    </div>
</div>
<div class="blog-wrapper">
    <div class="zine-container-centered">
    <div class="zine-container">
    {% assign zines = page.Zines %}
        {% for zine in zines %}
        <a class="zine-post" href="{{zine.url}}">
            <div>
                <div class="zine-image">
                    <h3>The Good Side Zine Issue {{zine.['Zine Number']}}</h3>
                    <img src="{{zine.['Zine Image']}}">
                </div>
            </div>
        </a>
        {% endfor %}
    </div>
    </div>
</div>

{% include tg-footer.html %}
{% include tg-footer-base.html %}