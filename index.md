---
layout: default
title: About
---

<section class="home-hero">
  <div class="hero-copy">
    <h1>Kevin Jun</h1>
    <p class="home-intro">Software engineer in Chicago's trading industry, with a background in consulting and analytics. I like tech, music, reading and cooking.</p>
    <div class="hero-actions">
      <a class="button button-primary" href="{{ site.baseurl }}/experience/">Explore my work <span aria-hidden="true">↗</span></a>
      <a class="button button-quiet" href="https://www.linkedin.com/in/kevjun">Connect on LinkedIn</a>
    </div>
  </div>
  <div class="hero-visual" aria-hidden="true">
    <svg class="signal-art" viewBox="0 0 620 560" fill="none" xmlns="http://www.w3.org/2000/svg">
      <defs>
        <linearGradient id="ray-blue" x1="86" y1="54" x2="532" y2="448" gradientUnits="userSpaceOnUse"><stop stop-color="#A7E5FF" stop-opacity="0"/><stop offset=".46" stop-color="#A7E5FF"/><stop offset="1" stop-color="#A7E5FF" stop-opacity="0"/></linearGradient>
        <linearGradient id="ray-lime" x1="456" y1="42" x2="176" y2="525" gradientUnits="userSpaceOnUse"><stop stop-color="#D5FF63" stop-opacity="0"/><stop offset=".48" stop-color="#D5FF63"/><stop offset="1" stop-color="#D5FF63" stop-opacity="0"/></linearGradient>
        <filter id="glow"><feGaussianBlur stdDeviation="5" result="blur"/><feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
      </defs>
      <g class="signal-grid" opacity=".2"><path d="M0 112H620M0 224H620M0 336H620M0 448H620M124 0V560M248 0V560M372 0V560M496 0V560" stroke="white"/></g>
      <path class="signal-ray ray-blue" d="M-14 102L606 470" stroke="url(#ray-blue)" stroke-width="3" filter="url(#glow)"/>
      <path class="signal-ray ray-lime" d="M548 18L142 552" stroke="url(#ray-lime)" stroke-width="2" filter="url(#glow)"/>
      <path class="signal-route route-one" d="M31 413H176L245 343H356L427 250H588" stroke="#A7E5FF" stroke-width="2"/>
      <path class="signal-route route-two" d="M56 188H166L230 255H344L408 197H559" stroke="#D5FF63" stroke-width="2"/>
      <path class="signal-route route-three" d="M127 497V375L197 305V119" stroke="#fff" stroke-opacity=".5" stroke-width="1"/>
      <g class="signal-nodes" filter="url(#glow)"><circle cx="176" cy="413" r="6" fill="#A7E5FF"/><circle cx="356" cy="343" r="6" fill="#A7E5FF"/><circle cx="427" cy="250" r="7" fill="#D5FF63"/><circle cx="230" cy="255" r="5" fill="#D5FF63"/><circle cx="197" cy="305" r="5" fill="white"/></g>
      <g class="signal-bars" opacity=".75"><rect x="448" y="335" width="95" height="6" rx="3" fill="#A7E5FF"/><rect x="469" y="351" width="75" height="6" rx="3" fill="#D5FF63"/><rect x="427" y="367" width="116" height="6" rx="3" fill="white"/><rect x="457" y="383" width="86" height="6" rx="3" fill="#A7E5FF"/></g>
    </svg>
  </div>
</section>

<section class="portrait-panel">
  <figure class="portrait-main"><img src="{{ site.baseurl }}/images/profile-photo.jpg" alt="Kevin Jun" width="960" height="720" fetchpriority="high"></figure>
  <figure class="portrait-secondary"><img src="{{ site.baseurl }}/images/leah-and-daisy.jpg" alt="Kevin's dog Leah and rabbit Daisy" width="1008" height="756" loading="lazy"></figure>
</section>

<section class="now-section">
  <div><h2>What I'm interested in now:</h2></div>
  <ul class="interest-list">
    <li><strong>LLMs</strong><span>Claude has been helping out a lot around the house.</span></li>
    <li><strong>Cooking</strong><span>It's soup season in Chicago, and I've been thinking about getting into sourdough.</span></li>
    <li><strong>Parenting</strong><span>I'm a human dad and dog dad.</span></li>
  </ul>
</section>
