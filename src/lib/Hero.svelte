<script lang="ts">
  // Assuming the video is in public/videos/hero-loop.mp4
  // If it's in src/assets, the import path needs to be relative
  // For now, let's use a public path for simplicity.
  const videoSrc = '/videos/hero-loop.mp4';
</script>

<div class="hero">
  <video autoplay loop muted playsinline class="hero-video">
    <source src="{videoSrc}" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <h1>Teuku Vaickal Rizki Irdian</h1>
    <h2>University Student & Developer</h2>
    <div class="social-links">
      <a href="https://github.com/icaluwu" target="_blank" rel="noopener noreferrer">GitHub</a>
      <a href="https://www.linkedin.com/in/teukuvaickal/" target="_blank" rel="noopener noreferrer">LinkedIn</a>
    </div>
  </div>
</div>