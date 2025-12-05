<script lang="ts">
  const specializations = [
    'Web Development',
    'SEO (Search Engine Optimization)',
    'Cloud Computing',
    'Project Management'
  ];

  const techIcons = [
    { name: 'ASP.NET', path: '/icons/asp.png' },
    { name: 'Flutter', path: '/icons/flutter.png' },
    { name: 'Google Cloud', path: '/icons/gcloud.png' },
    { name: 'Go', path: '/icons/golang.png' },
    { name: 'HTML5', path: '/icons/html.png' },
    { name: 'Laravel', path: '/icons/laravel.png' },
    { name: 'React', path: '/icons/react.png' },
    { name: 'Vite', path: '/icons/vite.png' },
    { name: 'Vue.js', path: '/icons/vue.png' },
    { name: 'WordPress', path: '/icons/wordpress.png' },
  ];

  const duplicatedIcons = [...techIcons, ...techIcons, ...techIcons, ...techIcons]; // Duplicate for a smoother, longer loop
</script>

<section id="about">
  <!-- Centered container for Bio and Specializations -->
  <div class="about-content-container">
    <div class="about-image-wrapper">
      <div class="about-image">
        <img src="/personals/profile.png" alt="Teuku Vaickal Rizki Irdian" />
      </div>
    </div>
    <div class="about-text">
      <h2 class="section-title">About Me</h2>
      <p class="bio">
        A passionate Information Systems student at Bina Sarana Informatika University with a drive for technology. I have hands-on experience across web development, mobile applications, and cloud computing. I'm a quick study, always excited to embrace and master new challenges.
      </p>
      
      <div class="info-section">
          <h4><span class="highlight">Name:</span> Teuku Vaickal Rizki Irdian</h4>
          <h4><span class="highlight">Location:</span> Jatiasih, Bekasi, Indonesia</h4>
      </div>

      <h3 class="specializations-title">My Specializations</h3>
      <div class="specializations-grid">
        {#each specializations as spec}
          <div class="spec-card">
            <span class="spec-text">{spec}</span>
          </div>
        {/each}
      </div>
    </div>
  </div>

  <!-- Full-width container for Tech Stack Carousel -->
  <div class="tech-stack-section">
    <h3 class="tech-stack-title">Technologies I Use</h3>
    <div class="tech-carousel-container">
        <div class="carousel-track">
            {#each duplicatedIcons as icon}
                <div class="tech-logo">
                    <img src="{icon.path}" alt="{icon.name}" title="{icon.name}" />
                </div>
            {/each}
        </div>
    </div>
  </div>

</section>