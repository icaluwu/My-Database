<script lang="ts">
  let y = 0;
</script>

<svelte:window bind:scrollY={y} />

<header class:scrolled={y > 0}>
  <div class="header-container">
    <nav>
      <a href="#about">About</a>
      <a href="#experience">Experience</a>
      <a href="#projects">Projects</a>
      <a href="#certifications">Certifications</a>
      <a href="#volunteering">Volunteering</a>
    </nav>
    <div class="social-links">
      <a href="https://github.com/icaluwu" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>
      </a>
      <a href="https://www.linkedin.com/in/icaluwu" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg>
      </a>
    </div>
  </div>
</header>

<style>
  header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    padding: 1rem 2rem;
    background-color: transparent;
    transition: background-color 0.3s ease;
    z-index: 10;
  }

  header.scrolled {
    background-color: rgba(24, 28, 36, 0.8);
    backdrop-filter: blur(10px);
  }

  .header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
  }

  nav {
    display: flex;
    justify-content: center;
    gap: 2rem;
  }

  a {
    color: #fff;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s ease;
    display: flex;
    align-items: center;
  }

  a:hover {
    color: #00bfff;
  }
  
  .social-links {
    display: flex;
    gap: 1.5rem;
  }

  .social-links a svg {
    stroke: #fff;
    transition: stroke 0.3s ease;
  }

  .social-links a:hover svg {
    stroke: #00bfff;
  }
</style>