---
url: "/resume/"
showToc: false
hideTitle: true
---

{{< rawhtml >}}
<style>
  /* Keep PaperMod's background, but allow full width content */
  main {
    max-width: 100vw !important;
    width: 100vw !important;
    margin: 0 !important;
    padding: 0 !important;
  }

  .resume-wrapper {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 2rem 0;
  }

  .resume-header {
    text-align: center;
    margin-bottom: 1.5rem;
  }

  .resume-header h1 {
    font-size: 2.3rem;
    margin: 0;
  }

  .download-btn {
    display: inline-block;
    background-color: #ff4b4b;
    color: white;
    padding: 0.6rem 1.4rem;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 500;
    transition: background-color 0.2s ease-in-out;
    margin-top: 1rem;
  }

  .download-btn:hover {
    background-color: #ff6a6a;
  }

  .resume-display {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0;
    padding: 0;
  }

  .resume-display embed {
    width: 90vw;
    height: calc(90vw * 1.294);
    max-width: 1000px;
    max-height: 1294px;
    border: none;
    border-radius: 10px;

    /* Thicker, more defined border */
    box-shadow: 0 0 40px 10px rgba(0, 0, 0, 0.35);

    background-color: white;
    display: block;
  }

  @media (max-width: 768px) {
    .resume-display embed {
      width: 95vw;
      height: calc(95vw * 1.294);
      box-shadow: 0 0 30px 8px rgba(0, 0, 0, 0.35);
    }

    .resume-header h1 {
      font-size: 1.8rem;
    }
  }
</style>

<div class="resume-wrapper">
  <div class="resume-header">
    <h1>Resumé</h1>
    <a href="/images/Resume11_4_2025.pdf" class="download-btn" download>Download PDF</a>
  </div>

  <div class="resume-display">
    <embed src="/images/Resume11_4_2025.pdf#toolbar=0&view=FitH" type="application/pdf">
  </div>
</div>
{{< /rawhtml >}}

