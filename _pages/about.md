---
layout: about
title: Sjors Verhaak
description: "Sjors Verhaak is a political theorist who recently received his PhD from Cornell University. His research explores ecological crisis, Earth metaphors, and democratic theory."
permalink: /
subtitle:

profile:
  align: right
  image: headshot.jpg
  image_circular: true
  image_style: "margin-top: -60px; margin-bottom: 20px; box-shadow: 0 6px 24px rgba(27,67,50,0.12); border: 3px solid #52b788; outline: 6px solid #d0e8dc; outline-offset: -3px;"
  more_info: >
    <div style="text-align: center; margin-top: 0.75em; position: relative; z-index: 10;">
      <a href="/assets/pdf/Verhaak%20CV.pdf" title="Download Curriculum Vitae"
        style="display: inline-block; padding: 0.4em 1.2em; font-family: 'Cormorant Garamond', Georgia, serif; font-size: 0.88em; letter-spacing: 0.12em; text-transform: uppercase; text-decoration: none; color: #2d6a4f; border: 1.5px solid #2d6a4f; border-radius: 2px; position: relative; z-index: 10;"
        onmouseover="this.style.background='#2d6a4f'; this.style.color='#fff';"
        onmouseout="this.style.background='transparent'; this.style.color='#2d6a4f';">
        Curriculum Vitae ↓
      </a>
    </div>

selected_papers: false
social: false

announcements:
  enabled: false
  scrollable: false
  limit: 5

latest_posts:
  enabled: true
  scrollable: true
  limit: 1
---

<style>
  /* Hide default theme h1 title — replaced by hero below */
  .post-header h1.post-title { display: none; }

  /* CV button */
  .cv-dl-btn {
    display: inline-block;
    padding: 0.4em 1.2em;
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.88em;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    text-decoration: none;
    color: #2d6a4f;
    border: 1.5px solid #2d6a4f;
    border-radius: 2px;
    position: relative;
    overflow: hidden;
    transition: color 0.3s ease;
    z-index: 0;
  }
  .cv-dl-btn::before {
    content: '';
    position: absolute;
    inset: 0;
    background: #2d6a4f;
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    z-index: -1;
  }
  .cv-dl-btn:hover { color: #fff; border-color: #2d6a4f; text-decoration: none; }
  .cv-dl-btn:hover::before { transform: scaleX(1); }

  /* Fade-in on load */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(12px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .about-fade {
    opacity: 0;
    animation: fadeUp 0.65s ease forwards;
  }
  .about-fade:nth-child(1) { animation-delay: 0.05s; }
  .about-fade:nth-child(2) { animation-delay: 0.2s; }
  .about-fade:nth-child(3) { animation-delay: 0.35s; }
  .about-fade:nth-child(4) { animation-delay: 0.5s; }
  .about-fade:nth-child(5) { animation-delay: 0.62s; }
  .about-fade:nth-child(6) { animation-delay: 0.72s; }
  .about-fade:nth-child(7) { animation-delay: 0.82s; }
  .about-fade:nth-child(8) { animation-delay: 0.92s; }

  /* Confluence line under name: two streams draw in and merge */
  .confluence-line {
    display: block;
    width: 100%;
    max-width: 300px;
    height: auto;
    margin: 0.1em 0 0.5em;
    overflow: visible;
  }
  .confluence-line path {
    fill: none;
    stroke-linecap: round;
    stroke-dasharray: 1;
    stroke-dashoffset: 1;
    animation: drawStream 1.6s cubic-bezier(0.45, 0, 0.2, 1) forwards;
  }
  .confluence-line .stream { stroke: #52b788; stroke-width: 1.3; animation-delay: 0.35s; }
  .confluence-line .stream-b { animation-delay: 0.5s; }
  .confluence-line .river { stroke: #2d6a4f; stroke-width: 2; animation-duration: 1.4s; animation-delay: 1.5s; }
  @keyframes drawStream { to { stroke-dashoffset: 0; } }

  /* Cycling tagline */
  .about-tagline { min-height: 3em; }
  .about-tagline-text { transition: opacity 0.45s ease; }
  .about-tagline-text.is-fading { opacity: 0; }

  /* Key-term definitions */
  .term {
    position: relative;
    border-bottom: 1px dotted #52b788;
    cursor: help;
    outline: none;
  }
  .term::after {
    content: attr(data-def);
    position: absolute;
    left: 50%;
    bottom: calc(100% + 10px);
    transform: translate(-50%, 4px);
    width: max-content;
    max-width: min(18rem, 70vw);
    padding: 0.6em 0.85em;
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.92rem;
    font-style: italic;
    line-height: 1.45;
    color: #1b4332;
    background: #fbfdfb;
    border: 1px solid #d0e8dc;
    border-left: 3px solid #52b788;
    border-radius: 2px;
    box-shadow: 0 6px 20px rgba(27, 67, 50, 0.1);
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.25s ease, transform 0.25s ease;
    z-index: 20;
  }
  .term:hover::after,
  .term:focus::after {
    opacity: 1;
    transform: translate(-50%, 0);
  }
  .term:hover, .term:focus { color: #2d6a4f; }

  /* Recently defended card */
  .defended-card {
    display: block;
    margin: 2em 0 0.5em;
    padding: 1.1em 1.3em;
    border: 1px solid #d0e8dc;
    border-left: 3px solid #52b788;
    border-radius: 3px;
    text-decoration: none !important;
    background: linear-gradient(to right, rgba(82, 183, 136, 0.06), transparent);
    transition: box-shadow 0.3s ease, transform 0.3s ease;
  }
  .defended-card:hover {
    box-shadow: 0 6px 22px rgba(27, 67, 50, 0.1);
    transform: translateY(-2px);
  }
  .defended-badge {
    display: inline-block;
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.72em;
    font-weight: 600;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #fff;
    background: #52b788;
    border-radius: 2px;
    padding: 0.1em 0.6em;
    margin-bottom: 0.5em;
  }
  .defended-title {
    display: block;
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 1.45rem;
    font-style: italic;
    color: #1b4332;
    line-height: 1.2;
  }
  .defended-meta {
    display: block;
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.8em;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: #52b788;
    margin: 0.3em 0 0.6em;
  }
  .defended-link {
    font-family: 'EB Garamond', Georgia, serif;
    color: #2d6a4f;
    border-bottom: 1px solid #52b788;
  }
  .defended-card:hover .defended-link { color: #1b4332; }

  /* Globe divider */
  .about-globe { display: block; width: 34px; height: 34px; }
  .about-globe * { fill: none; stroke: #52b788; stroke-width: 1; }
  .about-globe .globe-rim { stroke: #2d6a4f; stroke-width: 1.3; }

  /* Headshot glow on hover */
  .profile img { transition: transform 0.4s ease; }
  .profile img:hover { animation: ringGlow 2.4s ease-in-out infinite; }
  @keyframes ringGlow {
    0%, 100% { box-shadow: 0 6px 24px rgba(27, 67, 50, 0.12); }
    50%      { box-shadow: 0 6px 24px rgba(27, 67, 50, 0.12), 0 0 0 8px rgba(82, 183, 136, 0.18), 0 0 30px 6px rgba(82, 183, 136, 0.28); }
  }

  /* Scroll reveal (only when JS is running) */
  .js-reveal .reveal {
    opacity: 0;
    transform: translateY(16px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .js-reveal .reveal.is-visible {
    opacity: 1;
    transform: none;
  }

  @media (prefers-reduced-motion: reduce) {
    .about-fade, .confluence-line path, .profile img:hover { animation: none; opacity: 1; stroke-dashoffset: 0; }
    .js-reveal .reveal { opacity: 1; transform: none; transition: none; }
    .term::after, .defended-card { transition: none; }
  }

  /* Drop cap on first bio paragraph */
  .about-bio-first::first-letter {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 3.8em;
    font-weight: 400;
    color: #2d6a4f;
    float: left;
    line-height: 0.75;
    margin: 0.05em 0.08em 0 0;
    padding: 0;
  }

  /* Hero name treatment */
  .about-hero-name {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 3rem;
    font-weight: 300;
    color: #1b4332;
    letter-spacing: 0.06em;
    line-height: 1.1;
    margin: 0 0 0.1em 0;
  }
  .about-hero-name span {
    font-weight: 600;
    color: #2d6a4f;
  }
  .about-hero-sub {
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 0.95em;
    color: #5a5a5a;
    letter-spacing: 0.04em;
    margin-bottom: 1.6em;
  }
  .about-divider {
    display: flex;
    align-items: center;
    gap: 0.75em;
    margin: 1.8em 0 1.4em;
  }
  .about-divider::before,
  .about-divider::after {
    content: '';
    flex: 1;
    height: 1px;
  }
  .about-divider::before { background: linear-gradient(to right, transparent, #52b788); }
  .about-divider::after  { background: linear-gradient(to left,  transparent, #52b788); }
  .about-divider-glyph {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 1em;
    color: #52b788;
    letter-spacing: 0.2em;
    user-select: none;
  }

  /* Latest posts section */
  .post article h2 a[href*="blog"] {
    font-family: 'Cormorant Garamond', Georgia, serif !important;
    font-size: 0.78em;
    font-weight: 600;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #52b788 !important;
    text-decoration: none;
    display: flex;
    align-items: center;
    gap: 0.75em;
    margin-bottom: 1rem;
  }
  .post article h2 {
    margin-top: 2.5rem;
  }
  .post article h2 a[href*="blog"]::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, #d0e8dc, transparent);
  }
  /* Style the post rows in latest posts */
  .post article table {
    border: none;
    width: 100%;
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 1.05em;
    margin-top: 0.5rem;
  }
  .post article table td {
    border: none;
    padding: 0.5rem 0;
    color: #2a2218;
    vertical-align: top;
  }
  .post article table td:first-child {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.8em;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: #52b788;
    white-space: nowrap;
    padding-right: 1.5rem;
    padding-top: 0.6rem;
  }
  .post article table td a {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 1.25em;
    color: #1b4332;
    text-decoration: none;
    border-bottom: 1px solid transparent;
    transition: border-color 0.2s ease, color 0.2s ease;
  }
  .post article table td a:hover {
    color: #2d6a4f;
    border-bottom-color: #52b788;
  }
</style>


<div class="about-fade">
<p class="about-hero-name"><span>Sjors</span> Verhaak</p>
<svg class="confluence-line" viewBox="0 0 300 36" aria-hidden="true">
  <path class="stream" pathLength="1" d="M2,4 C50,4 80,18 135,18" />
  <path class="stream stream-b" pathLength="1" d="M2,32 C50,32 80,18 135,18" />
  <path class="river" pathLength="1" d="M135,18 C175,18 195,13 230,15 S280,20 298,18" />
</svg>
<p class="about-hero-sub">PhD in Political Theory &nbsp;·&nbsp; Cornell University</p>
</div>

<div class="about-fade">
<span style="display: block; font-family: 'Cormorant Garamond', Georgia, serif; font-size: 0.78em; font-weight: 600; letter-spacing: 0.18em; text-transform: uppercase; color: #52b788; margin-bottom: 0.75em;">About</span>
</div>

<div class="about-fade">
<p class="about-tagline" style="font-family: 'Cormorant Garamond', Georgia, serif; font-size: 1.28em; font-weight: 400; font-style: italic; color: #2d6a4f; border-left: 3px solid #52b788; padding-left: 0.85em; line-height: 1.5; margin-bottom: 1.6em;"><span class="about-tagline-text" id="about-tagline">Researcher specializing in environmental political theory and democratic thought.</span></p>
</div>

<div class="about-fade" style="font-family: 'EB Garamond', Georgia, serif; font-size: 1.08em; line-height: 1.85; color: #2a2218;">
  <p class="about-bio-first reveal">I am a political theorist whose research examines the ecological crisis from the standpoint of political theory. I received my PhD from Cornell University in 2026. My dissertation, <em>Imaginaries of Earth</em>, investigates the relationship of humans to their planet through the framework of <span class="term" tabindex="0" data-def="Earth imaginaries: the implicit, shared background understandings of Earth, carried in images, metaphors, and stories.">Earth imaginaries</span>, which make sense of practices such as Earth photography, climate science and engineering, and the extension of rights to nature.</p>

  <p class="reveal" style="margin-top: 1em;">It traces the encounter between two opposing imaginaries: a dominant planetary imaginary of human exceptionalism, mastery, and stewardship, premised on the disavowal of <span class="term" tabindex="0" data-def="Terrestriality: the constitutive earthliness of human being.">terrestriality</span>; and the Earth community imaginary sustained by the transnational Rights of Nature movement, which avows terrestriality through declaration. Their philosophical encounter is investigated through the problem space of <span class="term" tabindex="0" data-def="Gaia: a problem space in which ontological reflection about planetary being is displaced by systems understandings of the planet.">Gaia</span>.</p>

  <p class="reveal" style="margin-top: 1em;">Rather than adjudicating between these imaginaries, I attend to their meeting at sites of confluence, where <span class="term" tabindex="0" data-def="Confluential politics: politics that emerges where the disavowal of terrestriality meets its avowal, generating more-than-human collective political subjects.">confluential politics</span> can generate more-than-human collective political subjects whose emplaced practices refigure the human-planet relation. In doing so, I aim to cultivate a distinctive multi-species and post-anthropocentric approach to contemporary democratic theorizing, while reorienting political theory to the imaginaries that both sustain—and are sustained by—politics. My next project, <em>Democracy at Earth's Edge</em>, extends this research by examining how Earth imaginaries are negotiated between global frameworks of climate governance and local democratic practices.</p>
</div>

<div class="about-fade">
  <a class="defended-card reveal" href="{{ '/research/' | relative_url }}">
    <span class="defended-badge">Recently defended</span>
    <span class="defended-title">Imaginaries of Earth</span>
    <span class="defended-meta">Cornell University &nbsp;·&nbsp; July 2026</span>
    <span class="defended-link">Read the abstract →</span>
  </a>
</div>

<div class="about-fade about-divider">
  <svg class="about-globe" id="about-globe" viewBox="-20 -20 40 40" aria-hidden="true">
    <circle class="globe-rim" r="18" />
    <line x1="-18" y1="0" x2="18" y2="0" />
    <line x1="-15.6" y1="-9" x2="15.6" y2="-9" />
    <line x1="-15.6" y1="9" x2="15.6" y2="9" />
    <ellipse rx="18" ry="18"><animate attributeName="rx" values="18;0;18" keyTimes="0;0.5;1" calcMode="spline" keySplines="0.5 0 1 1;0 0 0.5 1" dur="12s" repeatCount="indefinite" /></ellipse>
    <ellipse rx="18" ry="18"><animate attributeName="rx" values="18;0;18" keyTimes="0;0.5;1" calcMode="spline" keySplines="0.5 0 1 1;0 0 0.5 1" dur="12s" begin="-4s" repeatCount="indefinite" /></ellipse>
    <ellipse rx="18" ry="18"><animate attributeName="rx" values="18;0;18" keyTimes="0;0.5;1" calcMode="spline" keySplines="0.5 0 1 1;0 0 0.5 1" dur="12s" begin="-8s" repeatCount="indefinite" /></ellipse>
  </svg>
</div>

<div class="about-fade" style="font-family: 'EB Garamond', Georgia, serif; font-size: 1em; color: #2a2218; text-align: center;">
  For more information please visit my <a href="https://government.cornell.edu/sjors-verhaak" style="color: #2d6a4f; border-bottom: 1px solid #52b788; text-decoration: none;">Cornell University profile</a>.
</div>

<div class="about-fade" style="margin-top: 2rem; font-family: 'Cormorant Garamond', Georgia, serif; font-size: 0.78em; font-weight: 600; letter-spacing: 0.14em; text-transform: uppercase; color: #aac9b8; text-align: center;">
  Last updated: September 2026
</div>

<script>
(function () {
  var reduceMotion = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  // Globe: hold still for reduced-motion visitors
  var globe = document.getElementById('about-globe');
  if (reduceMotion && globe && globe.pauseAnimations) { globe.pauseAnimations(); }

  // Cycling tagline, settling on the full tagline
  var tagline = document.getElementById('about-tagline');
  if (tagline && !reduceMotion) {
    var finalText = tagline.textContent;
    var phrases = ['Thinking Earth.', 'Planetary imaginaries.', 'The Earth community.', 'Gaia.', 'Confluence.', finalText];
    var i = 0;
    tagline.textContent = phrases[0];
    var timer = setInterval(function () {
      i += 1;
      tagline.classList.add('is-fading');
      setTimeout(function () {
        tagline.textContent = phrases[i];
        tagline.classList.remove('is-fading');
      }, 450);
      if (i === phrases.length - 1) { clearInterval(timer); }
    }, 1700);
  }

  // Scroll reveal
  if (!reduceMotion && 'IntersectionObserver' in window) {
    document.documentElement.classList.add('js-reveal');
    var observer = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add('is-visible');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.15 });
    document.querySelectorAll('.reveal').forEach(function (el) { observer.observe(el); });
  }
})();
</script>
