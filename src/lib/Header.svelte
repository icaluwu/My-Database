<script lang="ts">
  let y = 0;
  let menuOpen = false;

  function toggleMenu() {
    menuOpen = !menuOpen;
  }

  function closeMenu() {
    menuOpen = false;
  }
</script>

<svelte:window bind:scrollY={y} />

<header class:scrolled={y > 0 || menuOpen}>
  <div class="header-container">
    <div class="logo">
      <a href="/" on:click={closeMenu}>ICAL</a>
    </div>

    <button class="hamburger" on:click={toggleMenu} aria-label="Toggle menu" class:open={menuOpen}>
      <div class="bar1"></div>
      <div class="bar2"></div>
      <div class="bar3"></div>
    </button>

    <nav class:open={menuOpen}>
      <a href="#about" on:click={closeMenu}>About</a>
      <a href="#experience" on:click={closeMenu}>Experience</a>
      <a href="#projects" on:click={closeMenu}>Projects</a>
      <a href="#certifications" on:click={closeMenu}>Certifications</a>
      <a href="#volunteering" on:click={closeMenu}>Volunteering</a>
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
    transition: background-color 0.3s ease, box-shadow 0.3s ease;
    z-index: 1000;
  }

  header.scrolled {
    background-color: rgba(14, 16, 21, 0.8);
    backdrop-filter: blur(10px);
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
  }

  .logo a {
    font-size: 1.8rem;
    font-weight: 700;
    color: #fff;
    text-decoration: none;
    letter-spacing: 1px;
  }

  .hamburger {
    display: none;
    cursor: pointer;
    background: transparent;
    border: none;
    width: 28px;
    height: 28px;
    position: relative;
    z-index: 1001;
    padding: 0;
  }

  .bar1, .bar2, .bar3 {
    display: block;
    width: 100%;
    height: 3px;
    background-color: #fff;
    margin: 5px 0;
    transition: 0.4s;
    border-radius: 3px;
  }

  .hamburger.open .bar1 {
    transform: rotate(-45deg) translate(-6px, 6px);
  }

  .hamburger.open .bar2 {
    opacity: 0;
  }

  .hamburger.open .bar3 {
    transform: rotate(45deg) translate(-7px, -7px);
  }
  
  nav {
    display: flex;
    align-items: center;
    gap: 2.5rem;
  }

  nav a {
    color: #e0e0e0;
    text-decoration: none;
    font-weight: 500;
    font-size: 1rem;
    transition: color 0.3s ease;
    position: relative;
  }

  nav a::after {
    content: '';
    position: absolute;
    width: 0;
    height: 2px;
    bottom: -5px;
    left: 0;
    background-color: #00bfff;
    transition: width 0.3s ease;
  }

  nav a:hover {
    color: #fff;
  }
  
  nav a:hover::after {
    width: 100%;
  }

  .social-links-desktop {
    display: flex;
    gap: 1.5rem;
  }

  .social-links-desktop a svg {
    stroke: #e0e0e0;
    transition: stroke 0.3s ease, transform 0.3s ease;
  }

  .social-links-desktop a:hover svg {
    stroke: #00bfff;
    transform: scale(1.1);
  }

  .social-links-mobile {
    display: none;
  }

  @media (max-width: 992px) {
    nav {
      gap: 1.5rem;
    }
  }

  @media (max-width: 768px) {
    .hamburger {
      display: block;
    }

    nav {
      display: flex;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 2rem;
      background-color: rgba(14, 16, 21, 0.98);
      backdrop-filter: blur(15px);
      transform: translateY(-100%);
      transition: transform 0.5s cubic-bezier(0.76, 0, 0.24, 1);
      padding: 0;
      z-index: 1000;
    }

    nav.open {
      transform: translateY(0);
    }
    
    nav a {
      font-size: 1.8rem;
      font-weight: 600;
      color: #fff;
    }
    
    nav a::after {
      display: none;
    }

    .social-links-desktop {
      display: none;
    }

    .social-links-mobile {
      display: flex;
      gap: 2.5rem;
      margin-top: 3rem;
    }

    .social-links-mobile a svg {
      stroke: #fff;
      width: 32px;
      height: 32px;
      transition: stroke 0.3s ease, transform 0.3s ease;
    }

    .social-links-mobile a:hover svg {
      stroke: #00bfff;
      transform: scale(1.1);
    }
  }
</style>