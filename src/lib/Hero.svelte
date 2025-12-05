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

<style>
  .hero {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    text-align: center;
    overflow: hidden;
  }

  .hero-video {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 100%;
    height: 100%;
    object-fit: cover;
    transform: translate(-50%, -50%);
    z-index: -2;
  }

  .hero-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(18, 22, 28, 0.7); /* Dark overlay */
    z-index: -1;
  }

  .hero-content {
    z-index: 1;
    position: relative;
    color: #fff;
  }

  h1 {
    font-size: 4rem;
    color: #fff;
    margin-bottom: 0.5rem;
  }

  h2 {
    font-size: 1.5rem;
    color: #00bfff;
    margin-bottom: 2rem;
  }

  .social-links a {
    color: #fff;
    text-decoration: none;
    margin: 0 1rem;
    font-size: 1.2rem;
    transition: color 0.3s ease;
  }

  .social-links a:hover {
    color: #00bfff;
  }
</style>
