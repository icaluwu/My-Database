<script lang="ts">
  const videoSrc = '/videos/hero-loop.mp4';
</script>

<section class="hero">
  <video autoplay loop muted playsinline class="hero-video">
    <source src="{videoSrc}" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <h1>Teuku Vaickal Rizki Irdian</h1>
    <h2>University Student & Developer</h2>
    <div class="social-links">
      <a href="https://github.com/icaluwu" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>
      </a>
      <a href="https://www.linkedin.com/in/icaluwu/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg>
      </a>
    </div>
  </div>
</section>

<style>
  .hero {
    position: relative;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: #fff;
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
    background-color: rgba(0, 0, 0, 0.6);
    z-index: -1;
  }

  .hero-content {
    z-index: 1;
    max-width: 800px;
    padding: 1rem;
  }

  h1 {
    font-size: 3.5rem;
    margin-bottom: 0.5rem;
    font-weight: 700;
  }

  h2 {
    font-size: 1.75rem;
    margin-bottom: 2rem;
    font-weight: 400;
  }

  .social-links {
    display: flex;
    justify-content: center;
    gap: 2rem;
  }

  .social-links a {
    color: #fff;
    transition: color 0.3s ease;
  }

  .social-links a:hover {
    color: #00bfff; /* Deep sky blue */
  }

  .social-links a svg {
    stroke: #fff;
    transition: stroke 0.3s ease;
  }

  .social-links a:hover svg {
    stroke: #00bfff;
  }

  @media (max-width: 768px) {
    h1 {
      font-size: 2.5rem;
    }
    h2 {
      font-size: 1.25rem;
    }
  }
</style>