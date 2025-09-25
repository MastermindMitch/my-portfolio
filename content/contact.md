---
title: "Contact"
---
{{< rawhtml >}}
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

<!-- Contact Section -->
<section id="contact" style="text-align: center; padding: 2rem;">
  <h2>Contact Me</h2>
  <p>Feel free to reach out via the form below or connect with me on these platforms:</p>

  <div style="margin-top: 1rem;">
    <!-- LinkedIn -->
    <a href="https://linkedin.com/in/yourusername" target="_blank" rel="noopener noreferrer" class="social-icon linkedin">
      <i class="fab fa-linkedin"></i>
    </a>

    <!-- Handshake -->
    <a href="https://joinhandshake.com/" target="_blank" rel="noopener noreferrer" class="social-icon handshake">
      <i class="fas fa-handshake"></i>
    </a>

    <!-- GitHub -->
    <a href="https://github.com/yourusername" target="_blank" rel="noopener noreferrer" class="social-icon github">
      <i class="fab fa-github"></i>
    </a>
  </div>
</section>

<!-- Font Awesome -->
<script src="https://kit.fontawesome.com/your-kit-id.js" crossorigin="anonymous"></script>

<style>
  .social-icon {
    font-size: 2.5rem;
    margin: 0 15px;
    color: #888;
    transition: color 0.3s ease;
    text-decoration: none;
    border: none;       /* kill stray borders */
    outline: none;      /* kill focus outlines */
    box-shadow: none;   /* kill shadows */
  }

  /* Hover colors */
  .social-icon.linkedin:hover {
    color: #0A66C2;
  }

  .social-icon.handshake:hover {
    color: #f7b529;
  }

  .social-icon.github:hover {
    color: #333;
  }
</style>


{{< /rawhtml >}}
