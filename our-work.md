---
logo: light
hero: hero-work.html

accordion:
- title: <img class="header-icon" src="/images/icons/block-icon.svg" alt="" height="40" /><b>Building on Existing APIs</b>
  content: The Data Transfer Project (DTP) is an open source project that uses services’ existing APIs and authorization mechanisms to access data. It then uses service specific adapters to transfer that data into a common format, and then back into the new service’s API. DTP continues to be developed and grow today.
- title:  <img class="header-icon" src="/images/icons/block-icon.svg" alt="" height="40" /> <b>History</b>
  content: The Data Transfer Project was created in 2018 as an industry collaboration with a mission of enabling users to complete simple, fast, and secure data transfers directly between services. Since its creation, the project has built an open source technology framework that powers direct data transfer features within Google Takeout, Facebook’s Transfer your Information, and Apple’s Data and Privacy page, as well as software libraries that connect to over a dozen additional services..
-  title: <img class="header-icon" src="/images/icons/block-icon.svg" alt="" height="40" /><b> How it Works</b>
   content: DTP runs as a server in a data exporter’s platform. From there, it makes it easier for the data exporter to offer destinations for porting, exporting or backing up data, even in large volume. In turn this allows people to switch services or try new and innovative products. Without DTP, transferring a copy of data from one service to another can be a time consuming process, requiring a user to download a copy of their data to a local device and re-upload it to a new service. This can be particularly challenging for mobile-only users, those with limited bandwidth, and in markets where people pay-as-they-go for data usage. Direct service-to-service portability removes the need for local device storage and transfer -– enabling users to move their data directly between services.

---
<div class="columns">
  <div class="column-links" >
<br/>
    <a class="column-links-a" href="#policy-work">Policy Work</a><br/><br/><br/>
    <a class="column-links-a" href="#events">Events</a><br/><br/><br/>
    <a class="column-links-a" href="#open-source">Open Source</a><br/><br/><br/>
    <a class="column-links-a" href="#trust-model">Trust Model</a><br/><br/><br/>
    <!-- more links... -->
  </div>
  <div class="column-content">

<section>

<h3 id="policy-work">Policy Work</h3>

  <div class="our-work-intro-container">
    <ul class="our-work-intro">
      <li style="font-size: 16px">
        Our work on portability policy means that we talk to many policy-makers, directly or via
        publications and articles.
      </li>
      <li style="font-size: 16px">Much of our focus right now is on trust frameworks.  This <a href="/blog/2023/11/07/framework-trust">blog post</a> is a good introduction.
      </li>
    </ul>
   <nav class="our-work-nav">
      <h3>Most recent publications</h3>
    {% for paper in site.data.papers limit:4 %}
        <p><img class="list-icon" src="/images/icons/book-icon.svg" alt="" style="width: 30px">
            <a target="_blank" href="{{ paper.url | relative_url }}">
              {{ paper.name | escape }}
            </a>   </p>
    {% endfor %}
    <a target="_blank" href="/papers">All papers and articles</a></nav>
  </div>
</section>
<section class="slanted-background ourwork-container" style="--slanted-bg-color: var(--light-green)">
  <h2 id="events">Events</h2>
  <h4>Current Events</h4>

  <div style="width:100%">
    <h4>
      Portability in Practice: Google
    </h4>
<p>
	On February 11, 2025, DTI will host Google for a one hour virtual discussion of cutting-edge portability implementations, joined by civil society and other stakeholders. This experiment in engaging broader audiences is meant both to inform and to provide opportunities for feedback to portability tool developers. The event will be held under Chatham House rules for greater transparency; it will not be recorded, although DTI reserves the option to use modern transcription and summary services.
</p>
	  <p>
		  Details:
		  <ul>
<li>Tuesday, February 11 · 8:00 – 9:00am</li>
<li>Time zone: America/Los_Angeles</li>
<li>Google Meet joining info</li>
<li>Video call link: https://meet.google.com/kjw-asou-iqx</li>
<li>Or dial: ‪(US) +1 920-395-6055‬ PIN: ‪716 616 392‬#</li>
<li>More phone numbers: https://tel.meet/kjw-asou-iqx?pin=4186183993150</li>
		  </ul>
	  </p>
  </div>

 <div style=" display: block !important;">
<h4>Past Events</h4>
	 <h4>
		 Smart Data Forum in London
	 </h4>
	 <p>
		 DTI sponsored the <a href="https://www.smartdataforum.org/">Smart Data Forum</a>, organized by <a href="https://www.ctrl-shift.co.uk/">Ctrl-Shift</a>, in London to bring together business leaders, government officials, and civil society on issues related to data transfers.
	 </p>
    <h4>
      Spring Policy Event in DC &mdash; Empowerment through Portability
    </h4>
    <p>
      The <a target="_blank " href="/docs/feb29summit.html">Data Transfer Summit &mdash; Empowerment through Portability event</a> convenes academics, regulators and industry in DC to discuss difficult policy questions and the future of data portability policy.  <a href="/docs/feb29summitagenda">Agenda</a>, <a href="/docs/feb29summitspeakers">Speaker bios</a> and <a href="">livestream link</a> available now!
    </p>
    <a target="_blank " href="/assets/DTI-Data-Portability-Compendium.pdf">
      Check out the Data Portability Compendium Papers. 
    </a>
    <h4>
      The Federated Data Transfer Miniconference
    </h4>
    <p>
      On September 27th and 28th &mdash; (08:00 Pacific, 11:00 Eastern, 15:00 UTC) &mdash; the Data Transfer Initiative hosted our first online conference for social software developers, the Federated Data Transfer Miniconference.</p>
    <a target="_blank " href="/docs/dtp-federated-miniconference-report">
      The full Federated Data Transfer Miniconference Event Report
    </a> is now available. 

</div>

</section>



<section>
  <h3 id ="open-source" class="our-work-h3">
    Data Transfer Project - Open Source</h3>
{% include accordion.html %}



  <div class="our-work-intro-container">
       <nav class="our-work-nav">
        <ul class="work-nav-list">
         <li>
            <img class="list-icon" src="/images/icons/github-solid.svg" alt=""  style="width: 30px">
          <a style="font-size: 16px" href="https://github.com/dtinit" rel="noopener nofollow" target="_blank">DTP Github Repository</a>
          <img class="list-icon" src="/images/icons/book-icon.svg" alt="" style="width: 30px">
          <a  style="font-size: 16px" href="/docs/dtp-what-is-it">DTP &mdash; What is it?</a>
          <img class="list-icon" src="/images/icons/book-icon.svg" alt="" style="width: 30px">
          <a  style="font-size: 16px" href="/docs/dtp-intro-for-contributors">Intro for Potential Participants</a>
          <img class="list-icon" src="/images/icons/book-icon.svg" alt="" style="width: 30px">
          <a  style="font-size: 16px" href="/assets/dtp-overview.pdf">DTP Fundamentals and Overview (PDF)</a>
         </li>
      </ul>
    </nav>
  </div>

</section>


<section class="slanted-background">

 <h3 style="font-size: 1.45rem" id="trust-model"> A third-party trust model for direct personal data transfers</h3>


  <p>
    Data portability is a powerful tool to allow individuals to exercise more agency over personal data. While its origins lie in data protection and fundamental rights contexts, and that context remains salient, portability’s nexus to competition gives it new relevance. Portability helps consumers have more choices of services, and it helps businesses both to compete over similar service offerings and to innovate new features and functions. To take full advantage of these benefits, portability is evolving from a tool principally exercised by individual users requesting and receiving their data from a service provider via download, to implementation through direct transfers, where a user requests a data host to transfer personal data directly to a third party.
  </p>

  <p>
     The question that arises as a consequence of this shift is, how to build trust in these direct transfers. Exchanges of personal data are not without risk. DTI counts privacy and security among its core principles: “Platforms should not be required to substantially threaten the privacy and security of individual users or the platforms. Platforms may require baseline privacy and security standards, including shared certification or accreditation processes, as a condition of enabling data transfer.” This report is an exercise in coordinating the development of such standards.
    </p>
  <p> <a  style="font-size: 16px" href="/trust">Read More </a></p>



</section>

<section >
  <figure class="video-wrapper">
    <iframe class="video-embed" width="1100" height="622" src="https://www.youtube-nocookie.com/embed/_mVhmDnhrWo?si=BYbCUhmeT34HCHwQ" title="YouTube video player that plays a video describing the Data Transfer Project" allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  </figure>
  <figcaption class="video-description">
    This video serves as a good introduction to the Data Transfer Project's goals and participants. The DTP is a project within the DTI, which continues to grow and be developed today.
  </figcaption>
</section>


<hr/>

<p class="home-learn-more"> 
  <span>
		Learn more about DTI and our work!
	</span>
	<a class="button" href="/about">About DTI</a>
</p>

  </div>
</div>
