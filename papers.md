---
logo: light
hero: hero-work.html

---

<section>
  <h3>DTI Publications</h3>

  <div >
    <p>As we explore portability related themes and collaborate with our partners and others, we have published a number of paper/articles listed below.</p>
    {% for paper in site.data.papers %}
    <br/>

  <article class="post">
    <div class="post-image">
    <img class="list-icon" src="/images/icons/book-icon.svg" alt="" style="width: 130px">
    </div>
    <div class="post-text-stuff">
      <h2 class="post-title">
        <a href="{{ paper.url | relative_url }}">
          {{ paper.name | escape }}
        </a>
      </h2>
        <h4> Author: {{paper.author}}</h4>
              <div class="post-meta">
                <time class="post-date" datetime="{{ paper.date }}">{{ paper.date | date: "%b %-d, %Y" }}</time>
                {%- if paper.tags.size > 0 -%}
                  <ul class="post-tags">
                    {%- for tag in paper.tags -%}
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

</section>
<p class="home-learn-more"> 
  <span>
		Learn more about DTI and our work!
	</span>
	<a class="button" href="/about">About DTI</a>
</p>
