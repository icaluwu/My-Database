<script lang="ts">
  const projects = [
    {
      name: 'BantuLegal',
      description: 'A platform to connect people with legal professionals.',
      image: '/lives/bantulegal.png',
      liveUrl: 'https://bantulegal.web.id/',
      tech: ['Wordpress Fullstack']
    },
    {
      name: 'Vie Group',
      description: 'Company profile for Vie Group, a multi-business company.',
      image: '/lives/viegroup.png',
      liveUrl: 'https://viegroup.my.id/',
      tech: ['Wordpress Fullstack']
    },
    {
      name: 'Alat Uji Saku',
      description: 'E-commerce for pocket testing tools.',
      image: '/lives/alatujisaku.png',
      liveUrl: 'https://alatujisaku.com/',
      tech: ['Wordpress Fullstack']
    },
    {
      name: 'Alat Labor',
      description: 'E-commerce for laboratory equipment.',
      image: '/lives/alatlabor.png',
      liveUrl: 'https://alatlabor.co.id/',
      tech: ['Wordpress SEO']
    }
  ];
</script>

<section id="projects">
  <h2 class="section-title">My Projects</h2>
  <div class="projects-grid">
    {#each projects as project}
      <div class="project-card">
        <div class="card-border"></div>
        <div class="card-content">
          <div class="project-info">
            <div class="project-header">
              <img src="{project.image}" alt="{project.name} logo" class="project-logo">
              <h3>{project.name}</h3>
            </div>
            <p>{project.description}</p>
            <div class="tech-stack">
              {#each project.tech as tech}
                <span class="tech-badge">{tech}</span>
              {/each}
            </div>
            <a href="{project.liveUrl}" target="_blank" rel="noopener noreferrer" class="repo-link">Visit Website &rarr;</a>
          </div>
        </div>
      </div>
    {/each}
  </div>
</section>