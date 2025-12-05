<script lang="ts">
  let y = 0;
</script>

<svelte:window bind:scrollY={y} />

<header
  class:scrolled={y > 0}
>
  <nav>
    <a href="#about">About</a>
    <a href="#experience">Experience</a>
    <a href="#projects">Projects</a>
    <a href="#certifications">Certifications</a>
    <a href="#volunteering">Volunteering</a>
  </nav>
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
  }

  a:hover {
    color: #00bfff;
  }
</style>