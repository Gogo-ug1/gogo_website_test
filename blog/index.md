---
title: Blog
logo: dark
---

<div class="main-blog">
<h1 style="float: left; width:58%">Blog </h1>
<h3 style="float: left;margin-right: 10px">
Subscribe To DTI's Blog via </h3>
<h3>
    <div id="mc_embed_shell">
      <div id="mc_embed_signup">
         <form action="https://dtinit.us21.list-manage.com/subscribe/post?u=3ba10a090b97c2dc608fd780e&amp;id=1bb7a69318&amp;f_id=0012d8e1f0" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_self" novalidate="" style="float: left">
          <div id="mc_embed_signup_scroll">
            <div class="mc-field-group-subscribe">
              <input aria-label="Email address" type="email" name="EMAIL" class="text-input-subscribe required email" id="mce-EMAIL" required="" value="" placeholder="Enter your email" />
            </div>
            <div aria-hidden="true" style="position: absolute; left: -5000px;">
               <input type="text" name="b_3ba10a090b97c2dc608fd780e_1bb7a69318" tabindex="-1" value="" />
            </div>
            <input type="submit" name="subscribe" id="mc-embedded-subscribe" class="button-subscribe" value="Send" />
          </div>
        </form>
      </div>
    </div>

 </h3>
<a class="socialIcon" href="/feed.xml" style="float: left; margin-right: 10px; margin-top: 6px"> 
            <img height="24px" src="/images/rss_feed.png" alt="RSS Feed"/> RSS 
          </a>
 

<br>

</div>

<div class="blog-index-content">
{% for post in site.posts %}
  <article class="post">
    <div class="post-image">
      <img src="{{ post.thumbnail }}"/>
    </div>
    <div class="post-text-stuff">
      <h2 class="post-title">
        <a href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h2>
      <div class="post-meta">
        <time class="post-date" datetime="{{ post.date }}">{{ post.date | date: "%b %-d, %Y" }}</time>
        {%- if post.tags.size > 0 -%}
          <ul class="post-tags">
            {%- for tag in post.tags -%}
              <li>
                <a href="tags#{{tag}}">{{ tag }}</a>
              </li>
            {%- endfor -%}
          </ul>
        {%- endif -%}
      </div>
      <p>
        {{ post.excerpt }}
      </p>
    </div>
  </article>
<div class="blog-seperator"></div>
{% endfor %}
</div>
