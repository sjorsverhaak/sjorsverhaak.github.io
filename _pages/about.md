---
layout: about
title: Sjors Verhaak
description: "Sjors Verhaak is a political theorist and doctoral candidate at Cornell University. His research explores ecological crisis, Earth metaphors, and democratic theory."
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
<p class="about-hero-sub">PhD Candidate in Political Theory &nbsp;·&nbsp; Cornell University</p>
</div>

<div class="about-fade">
<span style="display: block; font-family: 'Cormorant Garamond', Georgia, serif; font-size: 0.78em; font-weight: 600; letter-spacing: 0.18em; text-transform: uppercase; color: #52b788; margin-bottom: 0.75em;">About</span>
</div>

<div class="about-fade">
<p style="font-family: 'Cormorant Garamond', Georgia, serif; font-size: 1.28em; font-weight: 400; font-style: italic; color: #2d6a4f; border-left: 3px solid #52b788; padding-left: 0.85em; line-height: 1.5; margin-bottom: 1.6em;">Doctoral candidate at Cornell University specializing in democratic thought and environmental political theory.</p>
</div>

<div class="about-fade" style="font-family: 'EB Garamond', Georgia, serif; font-size: 1.08em; line-height: 1.85; color: #2a2218;">
  <p class="about-bio-first">I am a doctoral candidate in political thought whose research examines the ecological crisis from the standpoint of political theory. More specifically, my dissertation, <em>Imaginaries of Earth</em> (defense: July 2026), investigates the role of Earth—in its narrative, metaphoric, and imaginative dimensions—not only in environmental politics, but in planetary politics writ large.</p>

  <p style="margin-top: 1em;">It does so through a series of interrelated investigations: the emergence of the metaphor of Spaceship Earth in the 1960s and its diffusion into the planetary imaginary; the theoretical underpinnings of the Rights of Nature movement, with an emphasis on the Earth community as an ontological community of being; and the discursive figure of Gaia in the environmental humanities and Gaia theory.</p>

  <p style="margin-top: 1em;">In weaving these strands together, guided by a structuring focus on the conceptual role of Earth, I aim to cultivate a distinctive multi-species and post-anthropocentric approach to contemporary democratic theorizing, while reorienting political theory to the imaginaries that both sustain—and are sustained by—politics. My next project, <em>Democracy at Earth's Edge</em>, extends this research by examining how Earth imaginaries are negotiated between global frameworks of climate governance and local democratic practices.</p>
</div>

<div class="about-fade about-divider">
  <span class="about-divider-glyph">✦</span>
</div>

<div class="about-fade" style="font-family: 'EB Garamond', Georgia, serif; font-size: 1em; color: #2a2218;">
  For more information please visit my <a href="https://government.cornell.edu/sjors-verhaak" style="color: #2d6a4f; border-bottom: 1px solid #52b788; text-decoration: none;">Cornell University profile</a>.
</div>
