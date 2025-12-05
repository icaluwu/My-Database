<script lang="ts">
  const certifications = [
    { name: 'BNSP Junior Web Developer', issuer: 'LSP BPPTIK' },
    { name: 'BNSP Program Analyst', issuer: 'LSP UBSI' },
    { name: 'Programming Essentials in Python', issuer: 'PCAP' },
    { name: 'Wordpress Development', issuer: 'MySkill' },
    { name: 'Frontend Web Development with TypeScript', issuer: 'Edureka' },
    { name: 'Build a Full Website using WordPress', issuer: 'Coursera' },
    { name: 'Cloud Practitioner Essentials AWS', issuer: 'Dicoding' },
    { name: 'Alibaba Cloud Associate', issuer: 'Alibaba Cloud' },
    { name: 'Database Design', issuer: 'Oracle' },
    { name: 'Strategic SEO', issuer: 'Skillshare' },
    { name: 'Search Engine Optimization', issuer: 'University of California, Davis' },
    { name: 'Social Media Optimization', issuer: 'Digital Entrepreneurship Academy (Digitalent)' },
    { name: 'Project Management and Scrum Framework', issuer: 'MySkill' },
    { name: 'Gemini Certified Student', issuer: 'Google Gemini University' },
    { name: 'UX/UI Design Fundamentals', issuer: 'IBM' },
  ];
</script>

<section id="certifications">
  <h2>Certifications</h2>
  <div class="cert-grid">
    {#each certifications as cert}
      <div class="cert-card">
        <h4>{cert.name}</h4>
        <p>{cert.issuer}</p>
      </div>
    {/each}
  </div>
</section>

<style>
  #certifications {
    padding: 4rem 2rem;
  }

  h2 {
    text-align: center;
    font-size: 2.5rem;
    color: #fff;
    margin-bottom: 3rem;
  }

  .cert-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .cert-card {
    background-color: #222831;
    padding: 1.5rem;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  }

  h4 {
    color: #00bfff;
    margin-bottom: 0.5rem;
  }
</style>