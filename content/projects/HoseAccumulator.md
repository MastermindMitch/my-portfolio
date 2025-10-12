---
title: "Hose Accumulator"
layout: hoseaccumulator
image: "images/HoseAccumulatorThumbnail.png"
description: "A compact vertical accumulator that stores hose during high-speed assembly line operations"
draft: false
markup: "html"
---

<style>
/* ===== Reset Theme Margins ===== */
.single .content,
.post-content {
  margin-left: 0 !important;
  padding-left: 0 !important;
  max-width: 100% !important;
}

/* ===== Hide Description Text ===== */
.single .post-description,
header .post-description {
  display: none !important;
}

/* ===== Page Layout ===== */
.project-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
  flex-wrap: wrap;
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
  padding: 2rem;
  box-sizing: border-box;
  font-family: "Inter", sans-serif;
  line-height: 1.6;
  color: #e0e0e0;
}

/* ===== Left Text Section ===== */
.details {
  flex: 1 1 600px;
  background-color: #1a1a1a;
  padding: 2rem;
  border-radius: 16px;
  margin-right: 2rem;
  box-sizing: border-box;
}

.details p {
  margin: 0.6rem 0;
}

.details strong {
  color: #ff4b4b;
  font-weight: 700;
  margin-right: 0.3rem;
}

/* ===== Right Image Section ===== */
.robot-image {
  flex: 0 0 350px;
  text-align: center;
}

.robot-image img {
  width: 100%;
  max-width: 350px;
  border-radius: 16px;
  object-fit: cover;
  box-shadow: 0 0 10px rgba(0,0,0,0.6);
}

/* ===== Video Section ===== */
.video-section {
  width: 100%;
  margin-top: 2.5rem;
}

.video-section h2 {
  color: #ff4b4b;
  font-size: 1.3rem;
  text-transform: uppercase;
  letter-spacing: 0.05em;
  border-bottom: 1px solid #333;
  padding-bottom: 0.3rem;
  margin-bottom: 0.8rem;
}

.video-wrapper {
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 0 8px rgba(0,0,0,0.6);
}

video {
  display: block;
  width: 100%;
  height: auto;
  border-radius: 12px;
  background: #000;
}

/* ===== Responsive ===== */
@media (max-width: 900px) {
  .project-container {
    flex-direction: column;
  }

  .details {
    margin-right: 0;
    margin-bottom: 2rem;
  }

  .robot-image {
    flex: 1 1 auto;
  }
}
</style>

<div class="project-container">

  <div class="details">
    <p><strong>Challenge:</strong> Find a way for operators to keep the assembly line at high speeds while cutting and storing processed hose. The solution also had to fit within a small 5×8 foot footprint.</p>

    <p><strong>Solution:</strong> Instead of redesigning the cutting process, I utilized the unused vertical space — over 30 feet of height — to accumulate the hose upward. This provided operators with roughly 50 seconds of buffer time to cut and reset the line before the next cycle began.</p>

    <p><strong>CAD:</strong> Inventor</p>

    <p><strong>Animation:</strong> Because the design was unconventional and difficult to visualize, I created a 3D CAD model and animation to demonstrate how the accumulator functions. This served as the first proof of concept and aligned the team on the idea.</p>
  </div>

  <div class="robot-image">
    <img src="/images/HoseAccumulatorThumbnail.png" alt="Hose Accumulator Machine">
  </div>
</div>

<div class="video-section">
  <h2>Accumulator Animation</h2>
  <div class="video-wrapper">
    <video controls autoplay muted playsinline loop>
      <source src="/videos/HoseAccumulatorFixed.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<script>
// ========== Only Play the Closest Video ==========
document.addEventListener("DOMContentLoaded", () => {
  const videos = document.querySelectorAll("video");

  const playClosest = () => {
    let closestVideo = null;
    let closestDistance = Infinity;

    videos.forEach(video => {
      const rect = video.getBoundingClientRect();
      const videoCenter = rect.top + rect.height / 2;
      const screenCenter = window.innerHeight / 2;
      const distance = Math.abs(videoCenter - screenCenter);

      if (distance < closestDistance) {
        closestDistance = distance;
        closestVideo = video;
      }
    });

    videos.forEach(v => {
      if (v === closestVideo && closestDistance < window.innerHeight / 2) {
        v.play();
      } else {
        v.pause();
      }
    });
  };

  window.addEventListener("scroll", playClosest);
  window.addEventListener("resize", playClosest);
  playClosest();
});
</script>

