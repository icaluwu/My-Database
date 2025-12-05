<script lang="ts">
  const certifications = [
    { name: 'BNSP Junior Web Developer', issuer: 'LSP BPPTIK', year: '2023', url: '#' },
    { name: 'BNSP Program Analyst', issuer: 'LSP UBSI', year: '2023', url: '#' },
    { name: 'Programming Essentials in Python', issuer: 'PCAP', year: '2022', url: '#' },
    { name: 'Wordpress Development', issuer: 'MySkill', year: '2023', url: '#' },
    { name: 'Frontend Web Development with TypeScript', issuer: 'Edureka', year: '2023', url: '#'},
    { name: 'Build a Full Website using WordPress', issuer: 'Coursera', year: '2022', url: '#'},
    { name: 'Cloud Practitioner Essentials AWS', issuer: 'Dicoding', year: '2024', url: '#'}, 
    { name: 'Alibaba Cloud Associate', issuer: 'Alibaba Cloud', year: '2024', url: '#'},
    { name: 'Database Design', issuer: 'Oracle', year: '2022', url: '#'},
    { name: 'Strategic SEO', issuer: 'Skillshare', year: '2023', url: '#'},
    { name: 'Search Engine Optimization', issuer: 'UC Davis', year: '2023', url: '#'},
    { name: 'Social Media Optimization', issuer: 'Digitalent', year: '2023', url: '#'},
  ];
</script>

<section id="certifications">
  <h2 class="section-title">Certifications</h2>
  <div class="cert-grid">
    {#each certifications as cert}
      <div class="cert-card">
        <div class="card-border"></div>
        <div class="card-content">
          <div class="cert-info">
            <h4>{cert.name}</h4>
            <p class="issuer">Issued by {cert.issuer} &bull; {cert.year}</p>
            <a href="{cert.url}" target="_blank" rel="noopener noreferrer" class="credential-link">View Credential &rarr;</a>
          </div>
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  #certifications {
    background-color: #12161c;
    padding: 6rem 2rem;
  }

  .section-title {
    text-align: center;
    font-size: 2.5rem;
    color: #fff;
    margin-bottom: 4rem;
  }

  .cert-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
    gap: 2.5rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .cert-card {
    position: relative;
    background: rgba(34, 40, 49, 0.65);
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .cert-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
  }

  .cert-card:hover .card-border {
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

  .cert-info {
    padding: 2rem;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
  }

  h4 {
    color: #00bfff;
    font-size: 1.4rem;
    line-height: 1.4;
    margin: 0;
    margin-bottom: 0.75rem;
    flex-grow: 1;
  }

  .issuer {
    color: #bbb;
    font-size: 0.9rem;
    margin-bottom: 1.5rem;
  }
  
  .credential-link {
    display: inline-block;
    align-self: flex-start;
    color: #fff;
    background-color: transparent;
    padding: 0.5rem 0;
    text-decoration: none;
    font-weight: bold;
    transition: color 0.3s ease;
    border-bottom: 2px solid #00bfff;
    font-size: 0.9rem;
  }

  .credential-link:hover {
    color: #00bfff;
  }

  @media (max-width: 480px) {
    #certifications {
      padding: 4rem 1rem;
    }
    .cert-grid {
      grid-template-columns: 1fr;
    }
  }
</style>