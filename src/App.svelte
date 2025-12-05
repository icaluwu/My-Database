<script lang="ts">
  import Header from './lib/Header.svelte';
  import Hero from './lib/Hero.svelte';
  import About from './lib/About.svelte';
  import Experience from './lib/Experience.svelte';
  import Projects from './lib/Projects.svelte';
  import Certifications from './lib/Certifications.svelte';
  import Volunteering from './lib/Volunteering.svelte';
</script>

<main>
  <Header />
  <Hero />
  <About />
  <Experience />
  <Projects />
  <Certifications />
  <Volunteering />
</main>

<footer>
  <p>&copy; 2024 Teuku Vaickal Rizki Irdian. All rights reserved.</p>
</footer>

<style>
  main {
    display: block;
  }

  footer {
    text-align: center;
    padding: 2rem;
    background-color: #181c24;
    color: #aaa;
  }
</style>