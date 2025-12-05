<script lang="ts">
  const experiences = [
    {
      role: 'Intern Mobile Application Developer',
      company: 'PT. Bank Mandiri',
      period: 'December 2025 - January 2026',
      description: 'Developing Flutter Application.',
    },
    {
      role: 'Intern SEO Specialist',
      company: 'PT. Anugrah Niaga Mandiri',
      period: 'September 2025 - January 2026',
      description: 'Developing and SEO for `alatujisaku`.',
    },
    {
      role: 'Intern Front-end Developer',
      company: 'Core Initiative',
      period: 'October 2025 - November 2025',
      description: 'Developing Front-end for clothing store single page using VueJS and API.',
    },
    {
      role: 'Intern Wordpress Developer',
      company: 'PT. Taharica',
      period: 'April 2025 - August 2025',
      description: 'Developing E-Knowledge Taharica.',
    },
  ];
</script>

<section id="experience">
  <h2>Experience</h2>
  <div class="timeline">
    {#each experiences as exp, i}
      <div class="timeline-item">
        <div class="timeline-content">
          <h3>{exp.role}</h3>
          <h4>{exp.company}</h4>
          <p class="period">{exp.period}</p>
          <p>{exp.description}</p>
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  #experience {
    padding: 4rem 2rem;
  }

  h2 {
    text-align: center;
    font-size: 2.5rem;
    color: #fff;
    margin-bottom: 3rem;
  }

  .timeline {
    position: relative;
    max-width: 1200px;
    margin: 0 auto;
  }

  .timeline::after {
    content: '';
    position: absolute;
    width: 6px;
    background-color: #222831;
    top: 0;
    bottom: 0;
    left: 50%;
    margin-left: -3px;
  }

  .timeline-item {
    padding: 1rem 40px;
    position: relative;
    width: 50%;
  }

  .timeline-item:nth-child(odd) {
    left: 0;
  }

  .timeline-item:nth-child(even) {
    left: 50%;
  }

  .timeline-item::after {
    content: '';
    position: absolute;
    width: 25px;
    height: 25px;
    right: -17px;
    background-color: white;
    border: 4px solid #00bfff;
    top: 15px;
    border-radius: 50%;
    z-index: 1;
  }

  .timeline-item:nth-child(even)::after {
    left: -16px;
  }

  .timeline-content {
    padding: 1.5rem;
    background-color: #222831;
    position: relative;
    border-radius: 6px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  }

  h3 {
    color: #00bfff;
    font-size: 1.5rem;
    margin-bottom: 0.5rem;
  }

  h4 {
    color: #eee;
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
  }

  .period {
    font-style: italic;
    color: #aaa;
    margin-bottom: 1rem;
  }

</style>