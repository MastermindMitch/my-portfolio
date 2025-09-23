<form name="contact" method="POST" data-netlify="true" style="max-width:400px; margin:auto; display:flex; flex-direction:column; gap:12px;">
  <label>
    Your name:
    <input type="text" name="name" required style="width:100%; padding:8px; border:1px solid #ccc; border-radius:4px;">
  </label>

  <label>
    Your email:
    <input type="email" name="email" required style="width:100%; padding:8px; border:1px solid #ccc; border-radius:4px;">
  </label>

  <label>
    Your message:
    <textarea name="message" required style="width:100%; padding:8px; border:1px solid #ccc; border-radius:4px; min-height:120px;"></textarea>
  </label>

  <button type="submit" style="padding:10px; background-color:#0077cc; color:white; border:none; border-radius:4px; cursor:pointer;">
    Send
  </button>
</form>

