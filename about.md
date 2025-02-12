---
logo: light
hero: hero-about.html
---

<section class="slanted-background">
  <h2>Who We Are</h2>
  <p>
    The Data Transfer Initiative (DTI) is a U.S. 501(c)(4) nonprofit organization dedicated to empowering individuals by enabling simpler, faster, and more secure data transfers through data portability at scale. Born out of the Data Transfer Project (DTP), a collaborative open-source effort initiated in 2018 by a consortium of technology companies, DTI advances its mission through the design and implementation of open source data transfer tools and other innovations and investments to foster a healthy portability ecosystem. DTI also serves as an expert resource to regulators around the world, helping translate principle to practice and catalyzing greater user agency and empowerment.
</p>
</section>

<section>
  <h2>The Team</h2>
  <p class="heading-subtitle">
    Driven by a shared passion for technology and positive change, our staff brings diverse expertise to our mission.
  </p>

  <div class="team-container">
    {% for person in site.data.staff %}
      <image class='team-avatar' src='/images/staff/{{ person.headshot }}'/>
      <div>
        <h3>{{ person.name }}</h3>
        <span class="team-subtitle">{{ person.position }}</span>
        <p>{{ person.bio }}</p>
        {% if person.linkedin %}
          <a class="social-icon" href="{{person.linkedin}}" target="_blank" rel="noopener nofollow">
            <img height="40" src="/images/icons/linkedIn.svg" alt="{{person.name}} on LinkedIn"/>
          </a>
        {% endif %}
        {% if person.mastodon %}
          <a class="social-icon" href="{{person.mastodon}}" target="_blank" rel="noopener nofollow">
            <img height="40" src="/images/icons/mastodon.svg" alt="{{person.name}} on Mastodon"/>
          </a>
        {% endif %}
      </div>
    {% endfor %}
  </div>
</section>

<section class="slanted-background subscribe-container">
  <div>
    <h2>Keep up with DTI</h2>
    <p>
      The scope of data portability is as broad and diverse as user data itself. We welcome you to join us in our efforts. To follow along with DTI’s work via our newsletter, please sign up below.
    </p>
    <div id="mc_embed_shell">
      <div id="mc_embed_signup">
        <form action="https://dtinit.us21.list-manage.com/subscribe/post?u=3ba10a090b97c2dc608fd780e&amp;id=1bb7a69318&amp;f_id=0012d8e1f0" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_self" novalidate="">
          <div id="mc_embed_signup_scroll">
            <div class="mc-field-group">
              <input aria-label="Email address" type="email" name="EMAIL" class="text-input required email" id="mce-EMAIL" required="" value="" placeholder="Enter your email" />
            </div>
            <div aria-hidden="true" style="position: absolute; left: -5000px;">
              <input type="text" name="b_3ba10a090b97c2dc608fd780e_1bb7a69318" tabindex="-1" value="" />
            </div>
            <input type="submit" name="subscribe" id="mc-embedded-subscribe" class="button" value="Subscribe" />
          </div>
        </form>
      </div>
    </div>
  </div>
  <img src="/images/dtinit_logo_lg.svg" alt="" />
</section>

<section>
  <h2>FAQs</h2>
  <p>
    We are committed to providing users with the information they need to make informed decisions about their data.
  </p>

  <details>
    <summary>What are some examples of data portability?</summary>
    <p>
      There are many use cases for users porting data directly between services, some we know about today, and some we have yet to discover. A couple of examples of ones we know users want today are...
    </p>
    <ul>
      <li>Moving one's private photos and photo albums to a different online hosting service permanently</li>
      <li>Moving social media post history to a new location without having to start from scratch at a new URL</li>
      <li>Trying out a new service with data from a service you already use, even if you don't decide to make the move</li>
      <li>Importing content into a new short-form video social service and continuing to use it in parallel with the old service</li>
    </ul>
  </details>
  <details>
    <summary>What is DTP?</summary>
    <p>
      One of the projects that DTI (Data Transfer Initiative) helps support is DTP (Data Transfer Project). The project was started much earlier than DTI was founded, and is an open source project with contributions from several companies. DTP is hosted by companies and connected to their data services in order to provide portability services that work with the other platforms participating in DTP.
    </p>
  </details>
  <details>
    <summary>What kinds of data can be transferred through DTP?</summary>
    <p>
      DTP can be used to transfer photos, videos and posts or documents, depending on what kind of data the source can send and the destination can accept.  Platforms that use DTP will offer available choices on their data management Web sites.
    </p>
  </details>
  <details>
    <summary>Who is responsible for protecting data?</summary>
    <p>
      Each organization is responsible for securing and protecting the data it receives, whether received via data portability or another way.  Organizations must also ensure that data is protected in transit when participating in data transfer.
    </p>
  </details>
  <details>
    <summary>When data is transferred via DTP, who gets a copy?</summary>
    <p>
      Only the source and destination ever get access to data transfered via the DTP.
    </p>
  </details>

  <h3>Still have a question?</h3>
  <p>
    If you have any questions that are not answered in our FAQ, please feel free to contact us.
  </p>

  <a class="button button-primary" href="https://dtinit.org/contact-us">
    Contact
  </a>
</section>
