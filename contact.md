---
layout: default
title: Contact Us
permalink: /contact/
---

# Contact Us

## Customer Support Portal
[Click here to access our Support Portal](https://textiletechnologies.freshdesk.com/support/home){:target="_blank"}  
Get quick answers, submit support tickets, and track progress all in one place.

---

## Phone
**800-536-7652**

## Email
[info@textile-tech.com](mailto:info@textile-tech.com)

## Address
1 N Walnut St. Suite 15  
Cleburne, TX 76033

---

<p style="text-align:center; margin-top:2rem;">
  <!-- Changed href to jump to the form on this page -->
  <a href="#request-demo" style="padding:0.8rem 1.5rem; background:#309c2f; color:#fff; text-decoration:none; border-radius:6px; font-weight:bold; font-size:1.1rem;">
    Request a Demo / Get a Quote
  </a>
</p>

<hr style="margin:3rem 0;" />

<h2 id="request-demo" style="scroll-margin-top: 90px;">Request a Demo / Get a Quote</h2>
<p>Fill this out and we’ll get back to you shortly.</p>

<form
  action="https://formspree.io/f/myznpvdd"
  method="POST"
  style="max-width:640px; padding:1rem 0;"
>
  <!-- Email subject line you’ll see -->
  <input type="hidden" name="_subject" value="New Demo/Quote Request from textile-tech.com" />
  <!-- Will be set to the Email field via JS just below -->
  <input type="hidden" name="_replyto" value="" />

  <!-- Honeypot (spam trap) -->
  <div style="position:absolute; left:-5000px;" aria-hidden="true">
    <label>Leave this field empty:
      <input type="text" name="_gotcha" tabindex="-1" autocomplete="off" />
    </label>
  </div>

  <div style="display:grid; gap:1rem;">
    <label style="display:block;">
      <span style="display:block; font-weight:600; margin-bottom:0.25rem;">Your Name *</span>
      <input name="name" type="text" required
             placeholder="First Last"
             style="width:100%; padding:0.6rem; border:1px solid #ccc; border-radius:6px;" />
    </label>

    <label style="display:block;">
      <span style="display:block; font-weight:600; margin-bottom:0.25rem;">Business Name *</span>
      <input name="business_name" type="text" required
             placeholder="Company, LLC"
             style="width:100%; padding:0.6rem; border:1px solid #ccc; border-radius:6px;" />
    </label>

    <fieldset style="border:1px solid #e5e7eb; border-radius:8px; padding:1rem;">
      <legend style="font-weight:700; padding:0 0.4rem;">Best Contact *</legend>

      <div style="display:flex; gap:2rem; align-items:center; flex-wrap:wrap;">
        <label style="display:flex; align-items:center; gap:0.5rem;">
          <input type="radio" name="preferred_contact" value="email" required />
          Email
        </label>
        <label style="display:flex; align-items:center; gap:0.5rem;">
          <input type="radio" name="preferred_contact" value="phone" required />
          Phone
        </label>
      </div>

      <div style="margin-top:1rem; display:grid; gap:0.75rem;">
        <label style="display:block;">
          <span style="display:block; font-weight:600; margin-bottom:0.25rem;">Email</span>
          <input name="email" type="email"
                 placeholder="name@company.com"
                 style="width:100%; padding:0.6rem; border:1px solid #ccc; border-radius:6px;" />
        </label>

        <label style="display:block;">
          <span style="display:block; font-weight:600; margin-bottom:0.25rem;">Phone</span>
          <input name="phone" type="tel"
                 placeholder="(555) 123-4567"
                 pattern="^(\+?\d{1,2}\s?)?(\(?\d{3}\)?[\s.-]?)\d{3}[\s.-]?\d{4}$"
                 style="width:100%; padding:0.6rem; border:1px solid #ccc; border-radius:6px;" />
        </label>
      </div>
    </fieldset>

    <label style="display:block;">
      <span style="display:block; font-weight:600; margin-bottom:0.25rem;">Anything else we should know?</span>
      <textarea name="message" rows="4" placeholder="Briefly describe your needs"
                style="width:100%; padding:0.6rem; border:1px solid #ccc; border-radius:6px;"></textarea>
    </label>

    <button type="submit"
            style="justify-self:start; padding:0.8rem 1.4rem; background:#309c2f; color:#fff; border:none; border-radius:6px; font-weight:700; cursor:pointer;">
      Submit Request
    </button>
  </div>

  <p id="form-status" style="margin-top:1rem;"></p>
</form>

<script>
  // Optional: Ajax submit to stay on page (works on GitHub Pages)
  (function () {
    const form = document.currentScript.previousElementSibling;
    const status = document.getElementById('form-status');
    if (!form || form.tagName !== 'FORM') return;

    form.addEventListener('submit', async function (e) {
      // Comment out the next 5 lines if you prefer Formspree’s default redirect/thank-you
      e.preventDefault();
      const data = new FormData(form);

      // Make preferred contact field enforce the right input
      const pref = data.get('preferred_contact');
      if (pref === 'email' && !data.get('email')) { alert('Please enter your email.'); return; }
      if (pref === 'phone' && !data.get('phone')) { alert('Please enter your phone number.'); return; }

      // Set reply-to so your email client can reply with one click
      data.set('_replyto', data.get('email') || '');

      try {
        const res = await fetch(form.action, { method: 'POST', body: data, headers: { 'Accept': 'application/json' } });
        if (res.ok) {
          status.textContent = 'Thanks! Your request has been sent.';
          form.reset();
        } else {
          status.textContent = 'Hmm, something went wrong sending the form. Please email info@textile-tech.com.';
        }
      } catch (err) {
        status.textContent = 'Network error. Please try again or email info@textile-tech.com.';
      }
    });
  })();
</script>

