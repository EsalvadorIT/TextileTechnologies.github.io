---
layout: default
title: Request a Demo / Get a Quote
permalink: /request-demo/
---

<h1>Request a Demo / Get a Quote</h1>

<form action="https://formspree.io/f/myznpvdd" method="POST">
  <!-- Subject line you'll see in the email -->
  <input type="hidden" name="_subject" value="Website request from textile-tech.com">

  <!-- Where to send users after submit (see step 2) -->
  <input type="hidden" name="_redirect" value="{{ '/thanks/' | absolute_url }}">

  <label for="name">Your name</label>
  <input id="name" name="name" required>

  <label for="company">Company name</label>
  <input id="company" name="company">

  <label for="best_contact">Best contact (email or phone)</label>
  <input id="best_contact" name="best_contact" required>

  <!-- Simple spam honeypot -->
  <div style="position:absolute; left:-10000px;" aria-hidden="true">
    <input type="text" name="_gotcha" tabindex="-1" autocomplete="off">
  </div>

  <button type="submit" style="padding:0.8rem 1.5rem; background:#309c2f; color:#fff; border:none; border-radius:6px; font-weight:bold; font-size:1.05rem;">
    Send
  </button>
</form>
