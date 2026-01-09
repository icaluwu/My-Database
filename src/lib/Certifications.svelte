<script lang="ts">
  const certifications = [
    { name: 'BNSP Junior Web Developer', issuer: 'LSP BPPTIK', year: '2023', url: 'https://drive.google.com/file/d/1KvKTlESFEGHIcotXiYnA1D841ebi35Ag/view?usp=sharing' },
    { name: 'BNSP Program Analyst', issuer: 'LSP UBSI', year: '2023', url: 'https://drive.google.com/file/d/1vuloxjD9wZglQtyr-wOYEIe0WzOW5bD-/view?usp=sharing' },
    { name: 'Programming Essentials in Python', issuer: 'PCAP', year: '2022', url: 'https://drive.google.com/file/d/1xTnKRZv97mXMtMZVeoafQLC5NH__mYBq/view?usp=sharing' },
    { name: 'Wordpress Development', issuer: 'MySkill', year: '2023', url: 'https://storage.googleapis.com/myskill-v2-certificates/topic-EzpMYkTamzIlqazTx9Z6/7920jOmuBYeEFECaW31d3oearq23-2bLMAlgdzR2vnX2gEAjv.pdf' },
    { name: 'Frontend Web Development with TypeScript', issuer: 'Edureka', year: '2023', url: 'https://www.coursera.org/account/accomplishments/verify/R7KJ33V4X3YM'},
    { name: 'Build a Full Website using WordPress', issuer: 'Coursera', year: '2022', url: 'https://www.coursera.org/account/accomplishments/verify/9BXQWZISFAEW'},
    { name: 'Cloud Practitioner Essentials AWS', issuer: 'Dicoding', year: '2024', url: 'https://www.dicoding.com/certificates/2VX3O5WYQZYQ'}, 
    { name: 'Alibaba Cloud Associate', issuer: 'Alibaba Cloud', year: '2024', url: 'https://drive.google.com/file/d/1mKY01AH20Q936KK4TzOuHkvMcNUJOTEd/view?usp=sharing'},
    { name: 'Database Design', issuer: 'Oracle', year: '2022', url: 'https://drive.google.com/file/d/1RlDwrSON1dd7OFM4NzSdzeGSuZEBqOTF/view?usp=sharing'},
    { name: 'Strategic SEO', issuer: 'Skillshare', year: '2023', url: 'https://www.coursera.org/account/accomplishments/specialization/7ALDV15YRNVU'},
    { name: 'Search Engine Optimization', issuer: 'UC Davis', year: '2023', url: 'https://www.coursera.org/account/accomplishments/specialization/2XQIAX6Q7ZW9'},
    { name: 'Social Media Optimization', issuer: 'Digitalent', year: '2023', url: 'https://www.linkedin.com/in/icaluwu/details/certifications/'},
    { name: 'Introduction to Front-End Development', issuer: 'Meta', year: '2026', url: 'https://www.coursera.org/account/accomplishments/verify/KFDINI3WPWQQ/'},
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