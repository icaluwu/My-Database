<script lang="ts">
  let y = 0;
  let menuOpen = false;

  function toggleMenu() {
    menuOpen = !menuOpen;
  }
</script>

<svelte:window bind:scrollY={y} />

<header class:scrolled={y > 0}>
  <div class="header-container">
    <div class="logo">
      <a href="/">ICAL</a>
    </div>
    <button class="hamburger" on:click={toggleMenu} aria-label="Toggle menu">
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <line x1="3" y1="12" x2="21" y2="12"></line>
        <line x1="3" y1="6" x2="21" y2="6"></line>
        <line x1="3" y1="18" x2="21" y2="18"></line>
      </svg>
    </button>
    <nav class:open={menuOpen}>
      <a href="#about" on:click={() => menuOpen = false}>About</a>
      <a href="#experience" on:click={() => menuOpen = false}>Experience</a>
      <a href="#projects" on:click={() => menuOpen = false}>Projects</a>
      <a href="#certifications" on:click={() => menuOpen = false}>Certifications</a>
      <a href="#volunteering" on:click={() => menuOpen = false}>Volunteering</a>
      <div class="social-links-mobile">
        <a href="https://github.com/icaluwu" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"></path></svg>
        </a>
        <a href="https://www.linkedin.com/in/icaluwu" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"></path><rect x="2" y="9" width="4" height="12"></rect><circle cx="4" cy="4" r="2"></circle></svg>
        </a>
      </div>
    </nav>
    <div class="social-links-desktop">
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

  .logo a {
    font-size: 1.5rem;
    font-weight: bold;
    color: #fff;
    text-decoration: none;
  }

  .hamburger {
    display: none;
    background: none;
    border: none;
    cursor: pointer;
    padding: 0;
  }

  .hamburger svg {
    stroke: #fff;
  }

  nav {
    display: flex;
    justify-content: center;
    gap: 2rem;
  }

  nav a {
    color: #fff;
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s ease;
    display: flex;
    align-items: center;
  }

  nav a:hover {
    color: #00bfff;
  }
  
  .social-links-desktop {
    display: flex;
    gap: 1.5rem;
  }

  .social-links-desktop a svg {
    stroke: #fff;
    transition: stroke 0.3s ease;
  }

  .social-links-desktop a:hover svg {
    stroke: #00bfff;
  }

  .social-links-mobile {
    display: none;
  }

  @media (max-width: 768px) {
    .hamburger {
      display: block;
      z-index: 11;
    }

    nav {
      position: fixed;
      top: 0;
      right: 0;
      bottom: 0;
      width: min(75vw, 400px);
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
      padding: 6rem 2rem 2rem;
      background-color: rgba(24, 28, 36, 0.95);
      backdrop-filter: blur(10px);
      transform: translateX(100%);
      transition: transform 0.3s ease-in-out;
    }

    nav.open {
      transform: translateX(0);
    }
    
    .social-links-desktop {
      display: none;
    }

    .social-links-mobile {
      display: flex;
      gap: 1.5rem;
      margin-top: 2rem;
    }

    .social-links-mobile a svg {
      stroke: #fff;
      transition: stroke 0.3s ease;
    }

    .social-links-mobile a:hover svg {
      stroke: #00bfff;
    }
  }
</style>