---
title: "Nylon Heat Welder"
layout: nylonheatwelder
image: "images/NylonHeatWelderThumbnail.jpg"
description: "Designed a machine to heat weld two nylon rods"
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
    <p><strong>What:</strong> A machine to make two rods of extruded nylon become one. The rods are stored around four-foot drums giving them a natural curvature.</p>

    <p><strong>How:</strong> A belt, shaped to match the nylon's curvature, was used to move the nylon. Pneumatics kept the nylon stable against the belt.</p>

    <p><strong>Result:</strong> A proof of concept for the movement mechanism, the hardest part, got built. The friction of the belt and force of the pneumatics ensured a firm grip without deforming or damaging the nylon. Operators could quickly and easily insert the nylon from the front of the machine.</p>

    <p><strong>CAD:</strong> Inventor</p>
  </div>

  <div class="robot-image">
    <img src="/images/NylonHeatWelderThumbnail.png" alt="Nylon Heat Welder">
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

