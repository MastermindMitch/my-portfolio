---
title: "Roller Coaster CAD Model"
layout: rollercoastercadmodel
image: "images/MillenniumForceModel.png"
description: "CAD model of the first ride I ever worked, Millennium Force"
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
    <p><strong>What:</strong> A passion project to create a model of the first ride I ever worked at using only a 3D printer.</p>

    <p><strong>Process:</strong> Used Google Earth to record the height of the track every 30 feet. I also used it to stitch together top down view images to create the layout.</p>

    <p><strong>3D Printing:</strong> Used vase mode to print a single continuous wall at 0.05mm. This achieved incredibly smooth results.</p>
    
    <p><strong>Project Future:</strong> Incredible work has been made, but the project is on hold until I have more time.</p>
    
    <p><strong>CAD:</strong> Fusion 360</p>
  </div>

  <div class="robot-image">
    <img src="/images/MillenniumForceModel.png" alt="Hose Accumulator Machine">
  </div>
</div>

