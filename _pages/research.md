---
layout: page
permalink: /research/
title: Research
nav: true
nav_order: 2
---

<style>
  /* Hide default page title */
  .post-header h1.post-title { display: none; }

  /* Fade-in */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(14px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .research-label, .research-heading, .research-intro {
    opacity: 0;
    animation: fadeUp 0.6s ease forwards;
  }
  .research-label   { animation-delay: 0.05s; }
  .research-heading { animation-delay: 0.15s; }
  .research-intro   { animation-delay: 0.25s; }

  .research-section {
    opacity: 0;
    animation: fadeUp 0.6s ease forwards;
  }
  .research-section:nth-of-type(1) { animation-delay: 0.35s; }
  .research-section:nth-of-type(2) { animation-delay: 0.48s; }
  .research-section:nth-of-type(3) { animation-delay: 0.58s; }

  /* Page layout */
  .research-wrapper {
    font-family: 'EB Garamond', Georgia, serif;
    max-width: 780px;
  }

  /* Header */
  .research-label {
    display: block;
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.78em;
    font-weight: 600;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #52b788;
    margin-bottom: 0.4em;
  }
  .research-heading {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 2.2rem;
    font-weight: 400;
    color: #1b4332;
    margin: 0 0 0.3em 0;
  }
  .research-intro {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-style: italic;
    color: #2d6a4f;
    font-size: 1.1em;
    margin-bottom: 2rem;
    padding-bottom: 1rem;
    border-bottom: 1px solid #d0e8dc;
    line-height: 1.6;
  }

  /* Section headers */
  .research-section-title {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.78em;
    font-weight: 600;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #52b788;
    display: flex;
    align-items: center;
    gap: 0.75em;
    margin-bottom: 1.4rem;
    margin-top: 2.5rem;
  }
  .research-section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(to right, #d0e8dc, transparent);
  }

  /* Dissertation block */
  .dissertation-block {
    border-left: 3px solid #52b788;
    padding-left: 1.2em;
    margin-bottom: 2rem;
  }
  .dissertation-title {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 1.45rem;
    font-weight: 400;
    font-style: italic;
    color: #1b4332;
    margin: 0 0 0.4em 0;
  }
  .dissertation-meta {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.82em;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: #52b788;
    margin-bottom: 0.75em;
  }
  .dissertation-desc {
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 1.05em;
    color: #2a2218;
    line-height: 1.75;
    margin: 0;
  }
  .dissertation-desc p {
    margin: 0 0 1.2em 0;
  }
  .dissertation-desc p:last-child {
    margin-bottom: 0;
  }

  /* Next project block */
  .next-project-block {
    background: transparent;
    border: 1px solid #d0e8dc;
    border-radius: 3px;
    padding: 1.2em 1.4em;
    margin-bottom: 2rem;
  }
  .next-project-label {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.75em;
    font-weight: 600;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: #52b788;
    margin-bottom: 0.3em;
  }
  .next-project-title {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 1.3rem;
    font-style: italic;
    font-weight: 400;
    color: #1b4332;
    margin: 0 0 0.5em 0;
  }
  .next-project-desc {
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 1.02em;
    color: #2a2218;
    line-height: 1.7;
    margin: 0;
  }
  .next-project-desc p {
    margin: 0 0 1.1em 0;
  }
  .next-project-desc p:last-child {
    margin-bottom: 0;
  }

  /* Presentation items */
  .presentation-item {
    padding: 1.2rem 0;
    border-bottom: 1px solid #f0ede8;
  }
  .presentation-item:last-child {
    border-bottom: none;
  }
  .presentation-title {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 1.2rem;
    font-weight: 400;
    font-style: italic;
    color: #1b4332;
    margin: 0 0 0.3em 0;
    line-height: 1.4;
  }
  .presentation-venue {
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 1em;
    color: #2a2218;
    margin: 0 0 0.2em 0;
  }
  .presentation-meta {
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.78em;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: #52b788;
    margin: 0;
  }
  .presentation-type {
    display: inline-block;
    font-family: 'Cormorant Garamond', Georgia, serif;
    font-size: 0.72em;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: #fff;
    background: #2d6a4f;
    border-radius: 2px;
    padding: 0.1em 0.5em;
    margin-right: 0.5em;
    vertical-align: middle;
  }
  .presentation-type.invited {
    background: #52b788;
  }
  .presentation-type.scheduled {
    background: transparent;
    color: #2d6a4f;
    border: 1px solid #2d6a4f;
  }
</style>

<div class="research-wrapper">

<h1 class="research-heading">Research</h1>

<p class="research-intro">My work sits at the intersection of democratic theory, environmental political thought, and the philosophy of politics. I examine how Earth—as a narrative, metaphoric, and imaginative concept—figures in the politics of ecological crisis and planetary governance.</p>

<!-- DISSERTATION -->
<div class="research-section">
<div class="research-section-title">Dissertation</div>

<div class="dissertation-block">
  <p class="dissertation-title">Imaginaries of Earth</p>
  <p class="dissertation-meta">Cornell University &nbsp;·&nbsp; Defended: July 2026 &nbsp;·&nbsp; Committee: Patchen Markell, Jill Frank, Alex Livingston</p>
  <div class="dissertation-desc">
    <p>This dissertation investigates the relationship of humans to their planet through the framework of Earth imaginaries: the implicit, shared background understandings of Earth, carried in images, metaphors, and stories, that make sense of practices including Earth photography, climate science and engineering, and the extension of rights to nature. The dominant planetary imaginary figures a promethean human-planet relation of human exceptionalism, mastery, and stewardship that is premised on the disavowal of terrestriality, the constitutive earthliness of human being. The opposing Earth community imaginary, sustained by the transnational Rights of Nature movement, avows a figuration of terrestriality through declaration. The philosophical encounter between these imaginaries is investigated through the problem space of Gaia, which is characterized by the displacement of ontological reflection about planetary being by systems understandings of the planet. However, instead of adjudicating between these imaginaries, I propose attending to their meeting at sites of confluence: where the disavowal of terrestriality meets its avowal. Reading the self-declaration of the personhood of the Mutehekau Shipu/Magpie River alongside Jacques Rancière’s theory of politics, I argue that confluential politics can emerge at these confluence sites, generating the more-than-human collective political subjects whose emplaced practices refigure the human-planet relation.</p>
  </div>
</div>

<div class="next-project-block">
  <p class="next-project-label">Next Project</p>
  <p class="next-project-title">Democracy at Earth's Edge</p>
  <div class="next-project-desc">
    <p>My next project, tentatively titled <em>Democracy at Earth's Edge</em>, aims to extend this research by examining how Earth imaginaries are negotiated between global frameworks of climate governance and local democratic practices. At the global scale, I plan to analyze imaginaries embedded in institutions such as the IPCC, the UNFCCC and its COP summits, and the ICJ—institutions that rest on simultaneously contested and underexamined background understandings of Earth. At the local scale, my research will examine how communities facing floods, droughts, wildfires, and other environmental disasters draw on imaginaries to make sense of crisis and in doing so articulate new forms of democratic practice.</p>

    <p>Methodologically, I plan to combine textual and discourse analysis of international institutional documents with qualitative case studies of communities navigating environmental disruption. By bringing these scales into conversation, I aim to show that the relationship between imaginaries and democratic practice is not unidirectional: global frameworks shape the resources available to communities, while local practices transform or rearticulate imaginaries in ways that unsettle official accounts.</p>
  </div>
</div>
</div>

<!-- CONFERENCE PRESENTATIONS -->
<div class="research-section">
<div class="research-section-title">Conference Presentations</div>

<div class="presentation-item">
  <p class="presentation-title">"Towards a Democratic Theory of Confluential Earth Politics"</p>
  <p class="presentation-venue">Western Political Science Association Annual Meeting</p>
  <p class="presentation-meta"><span class="presentation-type">Paper</span> San Diego &nbsp;·&nbsp; 2026</p>
</div>

<div class="presentation-item">
  <p class="presentation-title">"Figures of Gaia: Planetary Thinking Beyond Systems Theory"</p>
  <p class="presentation-venue">Association for Political Theory Conference</p>
  <p class="presentation-meta"><span class="presentation-type">Paper</span> Chicago &nbsp;·&nbsp; 2025</p>
</div>

<div class="presentation-item">
  <p class="presentation-title">"Contestable Earth: On the Earth Community and the Rights of Nature Movement"</p>
  <p class="presentation-venue">American Political Science Association Annual Meeting</p>
  <p class="presentation-meta"><span class="presentation-type">Paper</span> Philadelphia &nbsp;·&nbsp; 2024</p>
</div>
</div>

<!-- INVITED TALKS & WORKSHOPS -->
<div class="research-section">
<div class="research-section-title">Invited Talks &amp; Workshops</div>

<div class="presentation-item">
  <p class="presentation-title">"What Makes a Good Environmentalist from a Political Perspective?"</p>
  <p class="presentation-venue">Cornell Faith &amp; Environment Collective</p>
  <p class="presentation-meta"><span class="presentation-type invited">Invited</span> Ithaca &nbsp;·&nbsp; 2025</p>
</div>


</div>

</div>
