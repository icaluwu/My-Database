<script lang="ts">
  let y = 0;
</script>

<svelte:window bind:scrollY={y} />

<header class:scrolled={y > 0}>
  <div class="header-container">
    <div class="logo">
      <a href="/">ICAL</a>
    </div>

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
    position: sticky; /* Keep header at the top */
    top: 0;
    left: 0;
    right: 0;
    padding: 0.75rem 0.75rem; /* Further reduced padding for mobile */
    background-color: transparent;
    transition: background-color 0.3s ease, box-shadow 0.3s ease;
    z-index: 1000;
  }

  header.scrolled {
    background-color: rgba(14, 16, 21, 0.8);
    backdrop-filter: blur(10px);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }

  .header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
    gap: 0.75rem; /* Further reduced gap */
  }

  .logo a {
    font-size: 1.4rem; /* Made logo text slightly smaller on mobile */
    font-weight: 700;
    color: #fff;
    text-decoration: none;
    letter-spacing: 1px;
    flex-shrink: 0; /* Prevent logo from shrinking */
  }

  nav {
    display: flex;
    align-items: center;
    gap: 0.25rem; /* Further reduced gap */
    overflow-x: auto; /* Allow horizontal scrolling if needed */
    scrollbar-width: none; /* Hide scrollbar for Firefox */
    -ms-overflow-style: none; /* Hide scrollbar for IE/Edge */
  }
  
  nav::-webkit-scrollbar {
    display: none; /* Hide scrollbar for Chrome/Safari */
  }

  nav a {
    color: #e0e0e0;
    text-decoration: none;
    font-weight: 500;
    font-size: 0.7rem; /* Made font size even smaller */
    transition: color 0.3s ease;
    white-space: nowrap; /* Prevent text wrapping */
    padding: 0.2rem 0.4rem; /* Adjusted padding */
    border-radius: 4px;
  }
  
  nav a:hover {
    color: #fff;
    background-color: rgba(255, 255, 255, 0.1);
  }

  .social-links {
    display: flex;
    gap: 0.5rem; /* Further reduced gap */
    align-items: center;
  }

  .social-links a svg {
    stroke: #e0e0e0;
    width: 18px; /* Made icons smaller */
    height: 18px;
    transition: stroke 0.3s ease, transform 0.3s ease;
  }

  .social-links a:hover svg {
    stroke: #00bfff;
    transform: scale(1.1);
  }

  /* --- Desktop Styles --- */
  @media (min-width: 768px) {
    header {
      padding: 1rem 2rem;
    }

    .header-container {
      gap: 1rem;
    }

    .logo a {
      font-size: 1.8rem;
    }
    
    nav {
      gap: 1rem;
    }

    nav a {
      font-size: 1rem;
      padding: 0.5rem 1rem;
    }

    .social-links {
      gap: 1.5rem;
    }

    .social-links a svg {
      width: 24px;
      height: 24px;
    }
  }
</style>