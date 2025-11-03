---
title: "Autonomous Combat Robot"
layout: autonomouscombatrobot
image: "images/Unity.webp"
description: "Autonomous combat robot"
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
    <p><strong>What:</strong>A combat robot that uses sensors to find our position and the enemies position for faster attacks, and defensive maneuvers. </p>
    
    <p><strong>How:</strong>A simulation was built to test ideas and code faster. Many routes were investigated and attempted, such as using AI or SLAM. Due to extreme limitations, the only real-time solution was to hard code a vision system that took advantage of our environment.</p>

    <p><strong>Results:</strong>The simulation proved everything I was looking for and we could reliably track our position. I built a mock up of the arena to start testing a real life version. The real life bot showed some promising aspects and parts that would need work. However, I reached the end of college, and my time on this project.</p>
    
    <p><strong>Perseverance:</strong>I wanted to take a moment to highlight that this project is my magnum opus. I had people tell me the idea was too hard, would take to long, and even be impossible. I couldn't find anyone else who believed in the idea, so I built everything myself. All the CAD, code, research, etc. was me alone. Even after I had proof-of-concepts showing the idea could work, the club I was in did not want to fund the project. I did not let that deter me, and I just kept researching. This project represents years of determination to push boundaries and lead innovation.</p>

    <p><strong>CAD:</strong>Onshape</p>
    <p><strong>Code:</strong>Python</p>
    <p><strong>Simulation Software:</strong>Unity</p>
    <p><strong>Computer Vision Library:</strong>OpenCV</p>
    <p><strong>Single-Board Computer:</strong>Raspberry Pi 3</p>
  </div>

  <div class="robot-image">
    <img src="/images/Unity.webp" alt="Maze Bot Robot">
  </div>
</div>

<div class="video-section">
  <h2>Learning the Maze in Real Time</h2>
  <div class="video-wrapper">
    <video controls muted preload="auto" loop playsinline>
      <source src="/videos/BattleBot/Original2.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<div class="video-section">
  <h2>Learning the Maze (Sped Up)</h2>
  <div class="video-wrapper">
    <video controls muted preload="auto" loop playsinline>
      <source src="/videos/BattleBot/HSV2.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<div class="video-section">
  <h2>Traversing the Optimal Path</h2>
  <div class="video-wrapper">
    <video controls muted preload="auto" loop playsinline>
      <source src="/videos/BattleBot/Position2.mp4" type="video/mp4">
      Your browser does not support the video tag.
    </video>
  </div>
</div>

<script>
/*
  Synchronize all videos to start together on page load.
  - Wait for all videos to fire canplaythrough (or timeout).
  - Seek all to 0, then requestAnimationFrame -> play all.
  - Run a short resync loop to correct small drift.
  Notes:
  - Autoplay works only if the video is muted (we keep muted).
  - If you want sound, unmute after the videos are playing (user gesture required by some browsers).
*/

document.addEventListener("DOMContentLoaded", () => {
  const videos = Array.from(document.querySelectorAll("video"));
  if (!videos.length) return;

  // Ensure helpful attributes
  videos.forEach(v => {
    v.muted = true;          // required by most browsers to autoplay without user gesture
    v.playsInline = true;
    v.preload = "auto";
  });

  // Wait for canplaythrough for each video, or fallback timeout
  const waitForReady = (video, timeout = 5000) => new Promise(resolve => {
    if (video.readyState >= 3) return resolve();
    let resolved = false;
    const onReady = () => {
      if (resolved) return;
      resolved = true;
      cleanup();
      resolve();
    };
    const onError = () => {
      if (resolved) return;
      resolved = true;
      cleanup();
      resolve();
    };
    const cleanup = () => {
      video.removeEventListener("canplaythrough", onReady);
      video.removeEventListener("error", onError);
      clearTimeout(timer);
    };
    video.addEventListener("canplaythrough", onReady);
    video.addEventListener("error", onError);
    const timer = setTimeout(() => {
      if (resolved) return;
      resolved = true;
      cleanup();
      resolve(); // allow proceed after timeout
    }, timeout);
  });

  (async () => {
    // wait for all videos to be ready (or timeout)
    await Promise.all(videos.map(v => waitForReady(v, 6000)));

    // Seek all to 0 (try/catch because some browsers block seeking until ready)
    videos.forEach(v => {
      try { v.currentTime = 0; } catch (e) { /* ignore */ }
    });

    // Start all in same animation frame for best synch
    requestAnimationFrame(() => {
      videos.forEach(v => {
        // play() returns a promise; ignore errors (some browsers may block briefly)
        v.play().catch(() => { /* ignore autoplay block if any */ });
      });

      // short delay then run resync loop to correct drift
      setTimeout(() => resyncLoop(videos), 200);
    });
  })();

  // Simple resync loop: compute average time and snap videos that drift beyond threshold
  function resyncLoop(videos) {
    const driftThreshold = 0.08; // seconds (80 ms)
    const checkInterval = 500;   // ms
    const maxDuration = 15000;   // run resync for at most 15s
    const start = Date.now();

    const id = setInterval(() => {
      // stop if we've been at it too long
      if (Date.now() - start > maxDuration) { clearInterval(id); return; }

      // If any video is paused by the user/controls, stop automatic resync
      if (videos.some(v => v.paused)) { clearInterval(id); return; }

      // get current times (filter out NaN)
      const times = videos.map(v => v.currentTime).filter(t => !isNaN(t));
      if (!times.length) return;

      const avg = times.reduce((a,b) => a + b, 0) / times.length;

      videos.forEach(v => {
        const t = v.currentTime;
        if (isNaN(t)) return;
        const diff = t - avg;
        if (Math.abs(diff) > driftThreshold) {
          // snap back to average; small jumps are preferable to big drifting offsets
          try { v.currentTime = avg; } catch (e) { /* ignore if seeking denied */ }
        }
      });
    }, checkInterval);
  }
});
</script>

