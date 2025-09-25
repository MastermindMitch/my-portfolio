---
title: "Contact"
---
<div class="contact-intro">
  <p>
    Fill out the form below or email me directly at  
    <a href="mailto:mthenry@ksu.edu">mthenry@ksu.edu</a>.
  </p>
</div>

<form name="contact" method="POST" data-netlify="true" style="max-width:500px; margin:auto; padding:20px; background:#f9f9f9; border-radius:8px; box-shadow:0 2px 6px rgba(0,0,0,0.1); font-family:Arial, sans-serif;">
  <p style="margin-bottom:16px;">
    <label style="display:block; margin-bottom:6px; font-weight:bold;">Your Name:</label>
    <input type="text" name="name" required
      style="width:100%; padding:10px; border:1px solid #ccc; border-radius:4px; box-sizing:border-box;">
  </p>

  <p style="margin-bottom:16px;">
    <label style="display:block; margin-bottom:6px; font-weight:bold;">Your Email:</label>
    <input type="email" name="email" required
      style="width:100%; padding:10px; border:1px solid #ccc; border-radius:4px; box-sizing:border-box;">
  </p>

  <p style="margin-bottom:16px;">
    <label style="display:block; margin-bottom:6px; font-weight:bold;">Message:</label>
    <textarea name="message" required
      style="width:100%; padding:10px; border:1px solid #ccc; border-radius:4px; min-height:120px; box-sizing:border-box;"></textarea>
  </p>

  <p style="text-align:right; margin:0;">
    <button type="submit"
      style="padding:10px 20px; background-color:#0077cc; color:white; border:none; border-radius:4px; cursor:pointer; font-weight:bold;">
      Send
    </button>
  </p>
</form>

<!-- Social Links Section -->
<div class="social-links">
  <h3>Connect with me</h3>
  <div class="social-buttons">
    <a href="#" target="_blank" class="social-btn linkedin">LinkedIn</a>
    <a href="#" target="_blank" class="social-btn handshake">Handshake</a>
    <a href="#" target="_blank" class="social-btn github">GitHub</a>
    <a href="#" target="_blank" class="social-btn twitter">Twitter</a>
  </div>
</div>

<style>
  .social-links {
    margin-top: 2rem;
    text-align: center;
  }
  .social-buttons {
    display: flex;
    justify-content: center;
    gap: 1rem;
    flex-wrap: wrap;
    margin-top: 0.5rem;
  }
  .social-btn {
    padding: 0.6rem 1.2rem;
    border-radius: 8px;
    text-decoration: none;
    font-weight: bold;
    color: white;
    transition: background 0.3s;
  }
  .social-btn.linkedin { background: #0077b5; }
  .social-btn.handshake { background: #0a66c2; }
  .social-btn.github { background: #333; }
  .social-btn.twitter { background: #1da1f2; }
  .social-btn:hover { opacity: 0.85; }
</style>
