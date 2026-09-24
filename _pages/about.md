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

  /* Three imaginaries globe */
  .imaginaries { margin: 2.8em 0 0.5em; text-align: center; }
  .imaginaries-label {
    display: flex;
    align-items: center;
    gap: 0.75em;
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.78em;
    font-weight: 600;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #52b788;
  }
  .imaginaries-label::before,
  .imaginaries-label::after { content: ''; flex: 1; height: 1px; }
  .imaginaries-label::before { background: linear-gradient(to right, transparent, #d0e8dc); }
  .imaginaries-label::after  { background: linear-gradient(to left, transparent, #d0e8dc); }
  .imaginary-globe {
    display: block;
    width: 100%;
    max-width: 420px;
    aspect-ratio: 1;
    margin: 0 auto;
    cursor: grab;
    touch-action: pan-y;
    outline: none;
  }
  .imaginary-globe.is-dragging { cursor: grabbing; }
  .imaginary-globe:focus-visible { outline: 1px dashed #52b788; outline-offset: 4px; }
  .imaginaries-modes {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.5em;
  }
  .imaginary-btn {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.82em;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #2d6a4f;
    background: transparent;
    border: 1px solid #b7dcc8;
    border-radius: 2px;
    padding: 0.35em 0.95em;
    cursor: pointer;
    transition: background 0.25s ease, color 0.25s ease, border-color 0.25s ease;
  }
  .imaginary-btn:hover { border-color: #2d6a4f; }
  .imaginary-btn[aria-pressed="true"] { background: #2d6a4f; border-color: #2d6a4f; color: #fff; }
  .imaginaries-caption {
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 1.02em;
    line-height: 1.6;
    color: #2a2218;
    max-width: 32em;
    min-height: 4.8em;
    margin: 0.9em auto 0.2em;
  }
  .imaginaries-caption strong {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 1.1em;
    font-style: italic;
    font-weight: 600;
    color: #1b4332;
  }
  .imaginaries-hint {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.74em;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #aac9b8;
    margin: 0;
  }

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

<div class="about-fade imaginaries">
  <span class="imaginaries-label">Imaginaries of Earth</span>
  <canvas id="imaginary-globe" class="imaginary-globe" tabindex="0" role="img" aria-label="Interactive globe. Drag to turn it; click it or press Enter to switch between two imaginaries of Earth."></canvas>
  <div class="imaginaries-modes" role="group" aria-label="Choose an imaginary of Earth">
    <button type="button" class="imaginary-btn" data-mode="0" aria-pressed="true" data-caption="The planetary imaginary: Earth as a unified system to be modeled, measured, and managed, figuring human mastery and stewardship premised on the disavowal of terrestriality.">Earth System</button>
    <button type="button" class="imaginary-btn" data-mode="1" aria-pressed="false" data-caption="Earth as a community of beings, human and more-than-human, whose terrestriality is avowed through declaration by the transnational Rights of Nature movement.">Earth Community</button>
  </div>
  <p class="imaginaries-caption" id="imaginary-caption" aria-live="polite"><strong>Earth System.</strong> The planetary imaginary: Earth as a unified system to be modeled, measured, and managed, figuring human mastery and stewardship premised on the disavowal of terrestriality.</p>
  <p class="imaginaries-hint">Drag to turn &nbsp;·&nbsp; click the globe to change imaginary</p>
</div>

<div class="about-fade about-divider">
  <span class="about-divider-glyph">✦</span>
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

<script>
(function () {
  var canvas = document.getElementById('imaginary-globe');
  if (!canvas || !canvas.getContext) { return; }
  var ctx = canvas.getContext('2d');
  var reduceMotion = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  var DEG = Math.PI / 180;
  var buttons = document.querySelectorAll('.imaginary-btn');
  var caption = document.getElementById('imaginary-caption');

  var mode = 0;
  var alphas = [1, 0];
  var lambda = 20, phi = 18;
  var baseSpin = reduceMotion ? 0 : 0.006; // degrees per ms
  var spin = baseSpin;
  var t = 0;
  var W = 0, R = 0, cx = 0, cy = 0;
  var cosP = 1, sinP = 0;
  var p = { x: 0, y: 0, z: 0 };

  // ---- Geometry -----------------------------------------------------------
  function project(lon, lat, out) {
    var la = lat * DEG, lo = (lon + lambda) * DEG;
    var cl = Math.cos(la);
    var x = cl * Math.sin(lo), y0 = Math.sin(la), z0 = cl * Math.cos(lo);
    out.x = cx + R * x;
    out.y = cy - R * (y0 * cosP - z0 * sinP);
    out.z = y0 * sinP + z0 * cosP;
    return out;
  }

  // Adds the front (or back) portions of a lon/lat polyline to the current path
  function tracePolyline(coords, front) {
    var pen = false;
    for (var i = 0; i < coords.length; i++) {
      project(coords[i][0], coords[i][1], p);
      if (front ? p.z > 0 : p.z <= 0) {
        if (pen) { ctx.lineTo(p.x, p.y); } else { ctx.moveTo(p.x, p.y); pen = true; }
      } else {
        pen = false;
      }
    }
  }

  // Adds a polygon to the current path, pinning hidden points to the rim
  function tracePolygon(ring) {
    var visible = false, i;
    for (i = 0; i < ring.length; i++) {
      if (project(ring[i][0], ring[i][1], p).z > 0) { visible = true; break; }
    }
    if (!visible) { return; }
    for (i = 0; i < ring.length; i++) {
      project(ring[i][0], ring[i][1], p);
      var x = p.x, y = p.y;
      if (p.z <= 0) {
        var dx = x - cx, dy = y - cy, d = Math.sqrt(dx * dx + dy * dy) || 1;
        x = cx + dx / d * R; y = cy + dy / d * R;
      }
      if (i === 0) { ctx.moveTo(x, y); } else { ctx.lineTo(x, y); }
    }
    ctx.closePath();
  }

  var meridians = [], parallels = [], lon, lat;
  for (lon = -180; lon < 180; lon += 15) {
    var m = [];
    for (lat = -90; lat <= 90; lat += 3) { m.push([lon, lat]); }
    meridians.push(m);
  }
  for (lat = -75; lat <= 75; lat += 15) {
    var par = [];
    for (lon = -180; lon <= 180; lon += 3) { par.push([lon, lat]); }
    parallels.push(par);
  }
  var graticule = meridians.concat(parallels);

  // Coastlines from world-atlas (TopoJSON), decoded by hand
  var land = [];
  function decodeLand(topo) {
    var tf = topo.transform;
    var arcs = topo.arcs.map(function (arc) {
      var x = 0, y = 0;
      return arc.map(function (pt) {
        x += pt[0]; y += pt[1];
        return [x * tf.scale[0] + tf.translate[0], y * tf.scale[1] + tf.translate[1]];
      });
    });
    function ring(indices) {
      var out = [];
      indices.forEach(function (idx) {
        var arc = idx < 0 ? arcs[~idx].slice().reverse() : arcs[idx];
        arc.forEach(function (pt, k) { if (k > 0 || out.length === 0) { out.push(pt); } });
      });
      return out;
    }
    var obj = topo.objects.land;
    (obj.geometries || [obj]).forEach(function (g) {
      var polys = g.type === 'Polygon' ? [g.arcs] : g.type === 'MultiPolygon' ? g.arcs : [];
      polys.forEach(function (poly) { poly.forEach(function (r) { land.push(ring(r)); }); });
    });
  }
  if (window.fetch) {
    fetch('https://cdn.jsdelivr.net/npm/world-atlas@2/land-110m.json')
      .then(function (res) { return res.json(); })
      .then(decodeLand)
      .catch(function () {});
  }

  function traceLand() {
    ctx.beginPath();
    for (var i = 0; i < land.length; i++) { tracePolygon(land[i]); }
  }
  function traceLandOutline() {
    ctx.beginPath();
    for (var i = 0; i < land.length; i++) { tracePolyline(land[i], true); }
  }
  function disc() {
    ctx.beginPath();
    ctx.arc(cx, cy, R, 0, Math.PI * 2);
  }

  // ---- Mode 1: Earth System ---------------------------------------------
  function drawOrbit(front) {
    var rot = -0.32, u0 = front ? 0 : Math.PI, steps = 60;
    ctx.beginPath();
    for (var i = 0; i <= steps; i++) {
      var u = u0 + Math.PI * i / steps;
      var ex = 1.38 * R * Math.cos(u), ey = 0.34 * R * Math.sin(u);
      var x = cx + ex * Math.cos(rot) - ey * Math.sin(rot);
      var y = cy + ex * Math.sin(rot) + ey * Math.cos(rot);
      if (i === 0) { ctx.moveTo(x, y); } else { ctx.lineTo(x, y); }
    }
    ctx.setLineDash([3, 4]);
    ctx.strokeStyle = 'rgba(27,67,50,0.45)';
    ctx.lineWidth = 0.8;
    ctx.stroke();
    ctx.setLineDash([]);
    var su = (t * 0.5) % (Math.PI * 2);
    if ((Math.sin(su) > 0) === front) {
      var sx = 1.38 * R * Math.cos(su), sy = 0.34 * R * Math.sin(su);
      var px = cx + sx * Math.cos(rot) - sy * Math.sin(rot);
      var py = cy + sx * Math.sin(rot) + sy * Math.cos(rot);
      ctx.fillStyle = '#1b4332';
      ctx.fillRect(px - 3, py - 3, 6, 6);
      ctx.strokeStyle = '#52b788';
      ctx.beginPath(); ctx.moveTo(px - 9, py); ctx.lineTo(px + 9, py); ctx.stroke();
    }
  }

  function drawSystem() {
    drawOrbit(false);
    disc(); ctx.fillStyle = '#f3f7f5'; ctx.fill();

    ctx.beginPath();
    graticule.forEach(function (g) { tracePolyline(g, false); });
    ctx.strokeStyle = 'rgba(27,67,50,0.10)'; ctx.lineWidth = 0.6;
    ctx.setLineDash([2, 3]); ctx.stroke(); ctx.setLineDash([]);

    traceLand(); ctx.fillStyle = 'rgba(45,106,79,0.08)'; ctx.fill('evenodd');
    traceLandOutline(); ctx.strokeStyle = 'rgba(27,67,50,0.75)'; ctx.lineWidth = 0.8; ctx.stroke();

    ctx.beginPath();
    graticule.forEach(function (g) { tracePolyline(g, true); });
    ctx.strokeStyle = 'rgba(27,67,50,0.32)'; ctx.lineWidth = 0.6; ctx.stroke();

    // Measurement nodes at grid intersections
    for (var lo = -180; lo < 180; lo += 30) {
      for (var la = -60; la <= 60; la += 30) {
        project(lo, la, p);
        if (p.z > 0.1) {
          var pulse = 0.5 + 0.5 * Math.sin(t * 2 + lo * 0.1 + la * 0.2);
          ctx.fillStyle = 'rgba(82,183,136,' + (0.45 + 0.5 * pulse) + ')';
          ctx.fillRect(p.x - 1.8, p.y - 1.8, 3.6, 3.6);
        }
      }
    }

    // Rim with instrument ticks
    disc(); ctx.strokeStyle = '#1b4332'; ctx.lineWidth = 1.2; ctx.stroke();
    ctx.beginPath();
    for (var k = 0; k < 72; k++) {
      var a = k * 5 * DEG, len = k % 6 === 0 ? 7 : 3;
      ctx.moveTo(cx + Math.cos(a) * (R + 3), cy + Math.sin(a) * (R + 3));
      ctx.lineTo(cx + Math.cos(a) * (R + 3 + len), cy + Math.sin(a) * (R + 3 + len));
    }
    ctx.strokeStyle = 'rgba(27,67,50,0.45)'; ctx.lineWidth = 0.7; ctx.stroke();

    drawOrbit(true);

    // Readouts
    var viewLon = ((-lambda % 360) + 540) % 360 - 180;
    ctx.fillStyle = '#2d6a4f';
    ctx.font = '600 ' + Math.max(9, W * 0.024) + 'px ui-monospace, Menlo, Consolas, monospace';
    ctx.textAlign = 'left';
    ctx.fillText('EARTH SYSTEM MODEL', 10, 18);
    ctx.fillText('LON ' + viewLon.toFixed(1) + '°', 10, W - 26);
    ctx.fillText('LAT ' + phi.toFixed(1) + '°', 10, W - 12);
    ctx.textAlign = 'right';
    ctx.fillText('CO₂ 424 PPM', W - 10, 18);
    ctx.fillText('ΔT +1.5°C', W - 10, W - 12);
  }

  // ---- Mode 2: Earth Community ------------------------------------------
  var beings = [
    [-100, 60, 'bird'], [90, 48, 'bird'], [20, 68, 'bird'], [-65, -38, 'bird'], [140, -30, 'bird'],
    [-60, -8, 'tree'], [22, 0, 'tree'], [40, 58, 'tree'], [105, 62, 'tree'], [-120, 50, 'tree'],
    [-100, 40, 'human'], [15, 12, 'human'], [78, 24, 'human'], [135, -25, 'human'], [-70, -20, 'human'],
    [-30, 5, 'fish'], [-150, 20, 'fish'], [70, -40, 'fish'], [150, 30, 'fish'], [-120, -45, 'fish'], [0, -40, 'fish'],
    [-85, 15, 'butterfly'], [-50, -15, 'butterfly'], [30, -15, 'butterfly'], [115, 5, 'butterfly'],
    [-160, -15, 'turtle'], [60, -10, 'turtle'], [170, 10, 'turtle']
  ];
  var magpieRiver = [];
  for (var s = 0; s <= 12; s++) {
    magpieRiver.push([-64.6 + 0.35 * Math.sin(s * 1.3), 52.4 - s * 0.18]);
  }

  function drawBeing(type, i) {
    var flap = reduceMotion ? 0.8 : 0.6 + 0.4 * Math.sin(t * 5 + i);
    ctx.beginPath();
    if (type === 'bird') {
      ctx.moveTo(-1, 0); ctx.quadraticCurveTo(-0.5, -0.7 * flap, 0, 0);
      ctx.quadraticCurveTo(0.5, -0.7 * flap, 1, 0);
      ctx.stroke();
    } else if (type === 'fish') {
      ctx.moveTo(-0.8, 0); ctx.quadraticCurveTo(-0.2, -0.5, 0.4, 0);
      ctx.quadraticCurveTo(-0.2, 0.5, -0.8, 0);
      ctx.moveTo(0.4, 0); ctx.lineTo(0.9, -0.35); ctx.lineTo(0.9, 0.35); ctx.closePath();
      ctx.stroke();
    } else if (type === 'tree') {
      ctx.moveTo(0, 1); ctx.lineTo(0, 0.1);
      ctx.stroke();
      ctx.beginPath(); ctx.arc(0, -0.35, 0.55, 0, Math.PI * 2);
      ctx.fill(); ctx.stroke();
    } else if (type === 'human') {
      ctx.arc(0, -0.72, 0.22, 0, Math.PI * 2);
      ctx.moveTo(0, -0.48); ctx.lineTo(0, 0.3);
      ctx.moveTo(-0.45, -0.1); ctx.lineTo(0, -0.3); ctx.lineTo(0.45, -0.1);
      ctx.moveTo(0, 0.3); ctx.lineTo(-0.35, 0.95);
      ctx.moveTo(0, 0.3); ctx.lineTo(0.35, 0.95);
      ctx.stroke();
    } else if (type === 'butterfly') {
      ctx.save(); ctx.scale(flap, 1);
      ctx.ellipse(-0.42, -0.25, 0.4, 0.3, -0.5, 0, Math.PI * 2);
      ctx.moveTo(0.82, -0.25); ctx.ellipse(0.42, -0.25, 0.4, 0.3, 0.5, 0, Math.PI * 2);
      ctx.moveTo(-0.02, 0.3); ctx.ellipse(-0.3, 0.3, 0.28, 0.2, 0.4, 0, Math.PI * 2);
      ctx.moveTo(0.58, 0.3); ctx.ellipse(0.3, 0.3, 0.28, 0.2, -0.4, 0, Math.PI * 2);
      ctx.restore();
      ctx.fill(); ctx.stroke();
      ctx.beginPath(); ctx.moveTo(0, -0.5); ctx.lineTo(0, 0.6); ctx.stroke();
    } else if (type === 'turtle') {
      ctx.ellipse(0, 0, 0.7, 0.5, 0, 0, Math.PI * 2);
      ctx.moveTo(1.03, 0); ctx.arc(0.85, 0, 0.18, 0, Math.PI * 2);
      ctx.moveTo(-0.4, -0.4); ctx.lineTo(-0.6, -0.75);
      ctx.moveTo(0.4, -0.4); ctx.lineTo(0.6, -0.75);
      ctx.moveTo(-0.4, 0.4); ctx.lineTo(-0.6, 0.75);
      ctx.moveTo(0.4, 0.4); ctx.lineTo(0.6, 0.75);
      ctx.fill(); ctx.stroke();
    }
  }

  function drawCommunity(alpha) {
    var g = ctx.createRadialGradient(cx - R * 0.3, cy - R * 0.35, R * 0.1, cx, cy, R);
    g.addColorStop(0, '#f1f8f3'); g.addColorStop(1, '#d6ebdd');
    disc(); ctx.fillStyle = g; ctx.fill();

    traceLand(); ctx.fillStyle = 'rgba(82,183,136,0.32)'; ctx.fill('evenodd');
    traceLandOutline(); ctx.strokeStyle = 'rgba(45,106,79,0.45)'; ctx.lineWidth = 0.8; ctx.stroke();

    // Flowing wave lines in place of parallels
    ctx.beginPath();
    for (var la = -60; la <= 60; la += 15) {
      var wave = [];
      for (var lo = -180; lo <= 180; lo += 3) {
        wave.push([lo, la + 3 * Math.sin(lo * DEG * 4 + t * 0.8 + la)]);
      }
      tracePolyline(wave, true);
    }
    ctx.strokeStyle = 'rgba(45,106,79,0.35)'; ctx.lineWidth = 0.9; ctx.stroke();

    // Mutehekau Shipu / Magpie River
    ctx.beginPath(); tracePolyline(magpieRiver, true);
    ctx.strokeStyle = '#2d6a4f'; ctx.lineWidth = 1.8; ctx.stroke();
    project(-64.5, 51.4, p);
    if (p.z > 0.3) {
      ctx.globalAlpha = alpha * Math.min(1, (p.z - 0.3) * 4);
      ctx.fillStyle = '#1b4332';
      ctx.font = 'italic ' + Math.max(11, W * 0.03) + 'px "Cormorant Garamond", Georgia, serif';
      ctx.textAlign = 'left';
      ctx.fillText('Mutehekau Shipu', p.x + 6, p.y - 4);
      ctx.globalAlpha = alpha;
    }

    // Beings, foreshortened toward the limb
    ctx.lineCap = 'round'; ctx.lineJoin = 'round';
    ctx.strokeStyle = '#1b4332';
    ctx.fillStyle = 'rgba(82,183,136,0.45)';
    beings.forEach(function (b, i) {
      project(b[0], b[1], p);
      if (p.z < 0.05) { return; }
      var size = R * 0.07 * (0.5 + 0.5 * p.z);
      ctx.save();
      ctx.globalAlpha = alpha * Math.min(1, p.z * 4);
      ctx.translate(p.x, p.y);
      ctx.scale(size, size);
      ctx.lineWidth = 1.2 / size;
      drawBeing(b[2], i);
      ctx.restore();
    });

    disc(); ctx.strokeStyle = 'rgba(45,106,79,0.6)'; ctx.lineWidth = 1.2; ctx.stroke();
  }

  // ---- Loop and interaction ----------------------------------------------
  var painters = [drawSystem, drawCommunity];

  function render() {
    ctx.clearRect(0, 0, W, W);
    cosP = Math.cos(phi * DEG); sinP = Math.sin(phi * DEG);
    for (var k = 0; k < painters.length; k++) {
      if (alphas[k] < 0.01) { continue; }
      ctx.save();
      ctx.globalAlpha = alphas[k];
      painters[k](alphas[k]);
      ctx.restore();
    }
  }

  function resize() {
    var dpr = window.devicePixelRatio || 1;
    W = canvas.clientWidth || 360;
    canvas.width = Math.round(W * dpr);
    canvas.height = Math.round(W * dpr);
    ctx.setTransform(dpr, 0, 0, dpr, 0, 0);
    R = W * 0.34; cx = W / 2; cy = W / 2;
  }

  var dragging = false, last = 0, running = false, onScreen = true;
  function frame(now) {
    var dt = last ? Math.min(now - last, 50) : 16;
    last = now;
    if (!reduceMotion) { t += dt / 1000; }
    if (!dragging) {
      lambda += spin * dt;
      spin += (baseSpin - spin) * Math.min(1, dt / 1500);
    }
    lambda = ((lambda % 360) + 360) % 360;
    for (var k = 0; k < painters.length; k++) {
      alphas[k] += ((k === mode ? 1 : 0) - alphas[k]) * Math.min(1, dt / 220);
    }
    render();
    if (onScreen) { requestAnimationFrame(frame); } else { running = false; }
  }
  function start() {
    if (running) { return; }
    running = true; last = 0;
    requestAnimationFrame(frame);
  }

  function setMode(k) {
    mode = k;
    for (var i = 0; i < buttons.length; i++) {
      var on = Number(buttons[i].getAttribute('data-mode')) === k;
      buttons[i].setAttribute('aria-pressed', on ? 'true' : 'false');
      if (on && caption) {
        caption.innerHTML = '';
        var strong = document.createElement('strong');
        strong.textContent = buttons[i].textContent + '.';
        caption.appendChild(strong);
        caption.appendChild(document.createTextNode(' ' + buttons[i].getAttribute('data-caption')));
      }
    }
    start();
  }
  for (var b = 0; b < buttons.length; b++) {
    buttons[b].addEventListener('click', function () { setMode(Number(this.getAttribute('data-mode'))); });
  }

  var lastX = 0, lastY = 0, lastT = 0, moved = 0;
  canvas.addEventListener('pointerdown', function (e) {
    dragging = true; moved = 0;
    lastX = e.clientX; lastY = e.clientY; lastT = performance.now();
    if (canvas.setPointerCapture) { canvas.setPointerCapture(e.pointerId); }
    canvas.classList.add('is-dragging');
    start();
  });
  canvas.addEventListener('pointermove', function (e) {
    if (!dragging) { return; }
    var now = performance.now();
    var dx = e.clientX - lastX, dy = e.clientY - lastY;
    moved += Math.abs(dx) + Math.abs(dy);
    lambda += dx * 0.45;
    phi = Math.max(-60, Math.min(60, phi + dy * 0.45));
    spin = dx * 0.45 / Math.max(now - lastT, 8);
    lastX = e.clientX; lastY = e.clientY; lastT = now;
  });
  function endDrag(e, isClick) {
    if (!dragging) { return; }
    dragging = false;
    canvas.classList.remove('is-dragging');
    if (performance.now() - lastT > 80) { spin = baseSpin; }
    if (isClick && moved < 5) { setMode((mode + 1) % painters.length); }
  }
  canvas.addEventListener('pointerup', function (e) { endDrag(e, true); });
  canvas.addEventListener('pointercancel', function (e) { endDrag(e, false); });

  canvas.addEventListener('keydown', function (e) {
    if (e.key === 'ArrowLeft') { lambda -= 10; }
    else if (e.key === 'ArrowRight') { lambda += 10; }
    else if (e.key === 'ArrowUp') { phi = Math.max(-60, phi - 10); }
    else if (e.key === 'ArrowDown') { phi = Math.min(60, phi + 10); }
    else if (e.key === 'Enter' || e.key === ' ') { setMode((mode + 1) % painters.length); }
    else { return; }
    e.preventDefault();
    start();
  });

  resize();
  if ('ResizeObserver' in window) { new ResizeObserver(resize).observe(canvas); }
  else { window.addEventListener('resize', resize); }
  if ('IntersectionObserver' in window) {
    new IntersectionObserver(function (entries) {
      onScreen = entries[0].isIntersecting;
      if (onScreen) { start(); }
    }).observe(canvas);
  }
  start();
})();
</script>
