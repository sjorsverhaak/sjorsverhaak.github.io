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
  <p class="dissertation-meta">Cornell University &nbsp;·&nbsp; Defense: July 2026 &nbsp;·&nbsp; Committee: Patchen Markell, Jill Frank, Alex Livingston</p>
  <div class="dissertation-desc">
    <p>My dissertation asks: how do background understandings of Earth—socially and historically situated horizons of meaning about the planet—enable and constrain human and more-than-human democratic practices? I argue that these background understandings, or imaginaries of Earth, are not external to politics but rather constituted in and through politics. This then raises an important question: if imaginaries shape and are shaped by politics, how can we intervene in this dynamic to extend democracy to non-human others?</p>

    <p>My dissertation, <em>Imaginaries of Earth</em>, addresses this question in two ways. First, it examines how different imaginaries relate to practices, whether as ecosystems to be managed, a community of subjects with rights to be recognized, or as an intrusive actor to be institutionally accounted for. Second, it develops a general account of how the plurality of these imaginaries is not an obstacle but the very condition for democratic practices that can sustainably extend the boundaries of political inclusion beyond the human. More specifically, my dissertation develops this post-anthropocentric democratic theory by tracing how different ways of imagining Earth flow together at sites of confluential politics, opening possibilities for democratic renewal grounded in confluential democratic practices. I begin with the planetary imaginary that emerged in the mid-twentieth century, when the metaphor of “Spaceship Earth” and photographs of the planet from space encouraged people to picture Earth as a unified system to be managed. Against this, I examine the rise of a counter-imaginary that frames Earth as a community of beings, most clearly expressed in the transnational Rights of Nature movement, where the Earth community is treated as a subject with rights. Finally, I turn to contemporary thinkers who invoke the figure of Gaia to capture the planet’s unpredictable agency. Taken together, these different imaginaries can be seen coming together at sites of confluential politics, a politics that highlights both flows and turbulence; particularly, in the relations between Earth imaginaries (and the discursive, sociotechnical, and political practices that carry them). I weave these strands together to develop an account of a confluential Earth politics, which draws on critical democratic theory and riverine environmental thought to reframe the plurality of imaginaries not as a problem to be managed, but as a headwater for democratic renewal. These different imaginaries coming together at sites of confluential politics also provide the groundwork for my broader argument: that democratic theory must take seriously the plurality of Earth imaginaries as a condition for extending democracy beyond the human, and for cultivating post-anthropocentric forms of collective life in the context of ecological crisis.</p>

    <p>Taken together, these chapters show how Earth imaginaries constitute the horizon within which human and more-than-human democratic struggles unfold. <em>Imaginaries of Earth</em> contributes to democratic theory, environmental political thought, and the environmental humanities by demonstrating how imaginaries shape the scope of political community and by offering a framework for rethinking democracy in a time of planetary and ecological crisis.</p>
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
  <p class="presentation-meta"><span class="presentation-type scheduled">Scheduled</span> San Diego &nbsp;·&nbsp; April 2026</p>
</div>

<div class="presentation-item">
  <p class="presentation-title">"Figures of Gaia: Planetary Thinking Beyond Systems Theory"</p>
  <p class="presentation-venue">Association for Political Theory Conference</p>
  <p class="presentation-meta"><span class="presentation-type">Paper</span> Chicago &nbsp;·&nbsp; November 2025</p>
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
