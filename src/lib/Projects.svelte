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

<style>
  #projects {
    background-color: #12161c;
    padding: 6rem 2rem;
  }

  .section-title {
    text-align: center;
    font-size: 2.5rem;
    color: #fff;
    margin-bottom: 4rem;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 3rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .project-card {
    position: relative;
    background: rgba(34, 40, 49, 0.65);
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .project-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
  }

  .project-card:hover .card-border {
    opacity: 1;
  }

  .card-border {
    position: absolute;
    top: 0; left: 0; right: 0; bottom: 0;
    background: conic-gradient(from 180deg at 50% 50%, #00bfff 0deg, #ff00c3 50%, #00bfff 360deg);
    opacity: 0;
    transition: opacity 0.4s ease-in-out;
    z-index: 0;
    filter: blur(15px);
  }

  .card-content {
    position: relative;
    z-index: 1;
    background: #181c24;
    height: 100%;
    display: flex;
    flex-direction: column;
    border-radius: 11px;
  }

  .project-info {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
  }

  .project-header {
    display: flex;
    align-items: center;
    margin-bottom: 1rem;
  }

  .project-logo {
    width: 45px;
    height: 45px;
    object-fit: cover;
    border-radius: 8px;
    margin-right: 1rem;
    border: 1px solid rgba(255,255,255,0.2);
  }

  h3 {
    color: #00bfff;
    font-size: 1.6rem;
    margin: 0;
  }

  p {
    color: #ccc;
    line-height: 1.6;
    font-size: 0.95rem;
    margin-bottom: 1.5rem;
    flex-grow: 1;
  }
  
  .tech-stack {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 1.5rem;
  }

  .tech-badge {
    background-color: rgba(0, 191, 255, 0.1);
    color: #00bfff;
    padding: 0.25rem 0.6rem;
    border-radius: 5px;
    font-size: 0.8rem;
    font-weight: 500;
  }

  .repo-link {
    display: inline-block;
    align-self: flex-start;
    color: #fff;
    background-color: transparent;
    padding: 0.5rem 0;
    text-decoration: none;
    font-weight: bold;
    transition: color 0.3s ease;
    border-bottom: 2px solid #00bfff;
  }

  .repo-link:hover {
    color: #00bfff;
  }

  @media (max-width: 480px) {
    #projects {
      padding: 4rem 1rem;
    }
    .projects-grid {
      grid-template-columns: 1fr;
    }
  }
</style>