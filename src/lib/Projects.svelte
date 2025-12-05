<script lang="ts">
  const liveProjects = [
    { name: 'viegroup.my.id', type: 'Wordpress Fullstack', url: 'https://viegroup.my.id/' },
    { name: 'alatujisaku.com', type: 'Wordpress Fullstack', url: 'https://alatujisaku.com/' },
    { name: 'alatlabor.co.id', type: 'Wordpress SEO', url: 'https://alatlabor.co.id/' },
    { name: 'bantulegal.web.id', type: 'Wordpress Fullstack', url: 'https://bantulegal.web.id/' },
  ];

  const githubProjects = [
    { name: 'Web-Vue-JS', url: 'https://github.com/icaluwu/Web-Vue-JS' },
    { name: 'TokoMobile', url: 'https://github.com/icaluwu/TokoMobile' },
    { name: 'Victovia', url: 'https://github.com/icaluwu/Victovia' },
    { name: 'Project-Property-Web', url: 'https://github.com/icaluwu/Project-Property-Web' },
    { name: 'Project-Movie-Web', url: 'https://github.com/icaluwu/Project-Movie-Web' },
    { name: 'Project-Quizz-App', url: 'https://github.com/icaluwu/Project-Quizz-App' },
  ];
</script>

<section id="projects">
  <h2>Projects</h2>
  <h3>Live Deployments</h3>
  <div class="project-grid">
    {#each liveProjects as project}
      <a href={project.url} target="_blank" rel="noopener noreferrer" class="project-card">
        <h4>{project.name}</h4>
        <p>{project.type}</p>
      </a>
    {/each}
  </div>

  <h3>GitHub Repositories</h3>
  <div class="project-grid">
    {#each githubProjects as project}
      <a href={project.url} target="_blank" rel="noopener noreferrer" class="project-card">
        <h4>{project.name}</h4>
      </a>
    {/each}
  </div>
</section>

<style>
  #projects {
    padding: 4rem 2rem;
    background-color: #181c24;
  }

  h2, h3 {
    text-align: center;
    color: #fff;
    margin-bottom: 2rem;
  }

  h2 { font-size: 2.5rem; }
  h3 { font-size: 1.8rem; color: #00bfff; }

  .project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
    max-width: 1200px;
    margin: 0 auto 3rem auto;
  }

  .project-card {
    background-color: #222831;
    padding: 1.5rem;
    border-radius: 10px;
    text-decoration: none;
    color: #fff;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  }

  .project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(0, 191, 255, 0.2);
  }

  h4 {
    color: #00bfff;
    margin-bottom: 0.5rem;
  }
</style>