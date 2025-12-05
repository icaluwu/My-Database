<script lang="ts">
  const experiences = [
    {
      role: 'Intern Mobile Application Developer',
      company: 'PT. Bank Mandiri',
      period: 'December 2025 - January 2026',
      description: 'Developing Flutter Application.',
      logo: '/experiences/bankmandiri.png'
    },
    {
      role: 'Intern SEO Specialist',
      company: 'PT. Anugrah Niaga Mandiri',
      period: 'September 2025 - January 2026',
      description: 'Developing and SEO for `alatujisaku`.',
      logo: '/experiences/anugrahniagamandiri.png'
    },
    {
      role: 'Intern Front-end Developer',
      company: 'Core Initiative',
      period: 'October 2025 - November 2025',
      description: 'Developing Front-end for clothing store single page using VueJS and API.',
      logo: '/experiences/coreinitiative.png'
    },
    {
      role: 'Intern Wordpress Developer',
      company: 'PT. Taharica',
      period: 'April 2025 - August 2025',
      description: 'Developing E-Knowledge Taharica.',
      logo: '/experiences/taharica.png'
    },
  ];
</script>

<section id="experience">
  <h2 class="section-title">Work Experience</h2>
  <div class="timeline">
    {#each experiences as exp, i}
      <div class="timeline-item">
        <div class="timeline-content">
          <img src="{exp.logo}" alt="{exp.company} logo" class="company-logo">
          <h3>{exp.role}</h3>
          <h4>{exp.company}</h4>
          <span class="period">{exp.period}</span>
          <p>{exp.description}</p>
        </div>
      </div>
    {/each}
  </div>
</section>