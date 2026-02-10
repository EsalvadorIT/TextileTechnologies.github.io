---
layout: default
title: About
permalink: /about/
---

# About Textile Technologies

Textile Technologies is a leading provider of software products and industry insights. Our team is passionate about leveraging technology to empower businesses and drive success.

---

## Our Mission

Our mission at TT is rooted in a deep commitment to the textile rental industry.
We engage directly with industry associations and initiatives to ensure continuous innovation and collective progress.

<!-- Meet the Team Section -->
<section style="padding:2rem; background-color:#fff; text-align:center; border-top:1px solid #ddd;">

  <h2 style="color:#1f52a5; margin-top:0;">Meet the Team</h2>

  <p style="max-width:800px; margin:0 auto 2rem; font-size:1.1rem; line-height:1.6;">
    We’re the team behind the technology—designing, programming, and supporting solutions that make your experience smooth, reliable, and personal.
  </p>

  <style>
    .team-grid{
      display: grid;

      /* Two columns that HUG the card widths */
      grid-template-columns: repeat(2, minmax(280px, 420px));

      grid-template-areas:
        "dawn dawn"
        "emily joe";

      gap: 2rem;

      /* KEY: centers the two-column grid as a whole */
      justify-content: center;

      margin: 0 auto;
      align-items: start;
    }

    .team-card{
      border: 1px solid #ddd;
      border-radius: 12px;
      padding: 1.5rem;
      background: #fff;
      line-height: 1.6;
      text-align: center;
      box-sizing: border-box;
    }

    .team-dawn{ grid-area: dawn; justify-self: center; width: min(700px, 100%); }
    .team-emily{ grid-area: emily; }
    .team-joe{ grid-area: joe; }

    @media (max-width: 768px){
      .team-grid{
        grid-template-columns: 1fr;
        grid-template-areas:
          "dawn"
          "emily"
          "joe";
        justify-content: stretch;
        max-width: 540px;
      }
      .team-dawn{ width: 100%; }
    }
  </style>

  <div class="team-grid">

    <!-- Dawn (centered above) -->
    <div class="team-card team-dawn">
      <h4 style="margin:0; color:#1f52a5;">Owner and President</h4>
      <h3 style="margin:.25rem 0;">Dawn Vaughn</h3>
      <p>
        As Owner and President, Dawn anchors our team with unmatched technical skill and operational depth. From programming to managing high-level support strategies, she ensures our software and support stays strong and responsive.
      </p>
    </div>

    <!-- Emily -->
    <div class="team-card team-emily">
      <h4 style="margin:0; color:#1f52a5;">Software Support &amp; Reporting Specialist</h4>
      <h3 style="margin:.25rem 0;">Emily Salvador</h3>
      <p>
        With a foundation in data analytics and a growing focus in business development, Emily is an ambitious specialist evolving alongside the company, delivering hands-on assistance and custom reporting that empower business owners to make data-driven decisions.
      </p>
    </div>

    <!-- Joe -->
    <div class="team-card team-joe">
      <h4 style="margin:0; color:#1f52a5;">Chief Advisor</h4>
      <h3 style="margin:.25rem 0;">Joe Dulworth</h3>
      <p>
        Joe is the visionary behind our success. As the original developer of our proprietary software, he laid the foundation that helps businesses boost revenue, streamline operations, and grow profitably.
      </p>
    </div>

  </div>

  <hr class="tt-divider">
</section>

<p class="cta-wrap" style="text-align:center; margin-top:2rem;">
  <a class="btn-demo" href="{{ '/contact/' | relative_url }}">
    Request a Demo / Get a Quote
  </a>
</p>
