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

<style>
  #experience {
    padding: 6rem 2rem;
    background-color: #12161c;
  }

  .section-title {
    text-align: center;
    font-size: 2.5rem;
    color: #fff;
    margin-bottom: 4rem;
  }

  .timeline {
    position: relative;
    max-width: 900px;
    margin: 0 auto;
  }

  .timeline::after {
    content: '';
    position: absolute;
    width: 4px;
    background-color: #00bfff;
    top: 0;
    bottom: 0;
    left: 50%;
    margin-left: -2px;
  }

  .timeline-item {
    padding: 1rem 2.5rem;
    position: relative;
    width: 50%;
  }

  .timeline-item:nth-child(odd) {
    left: 0;
    padding-right: 4rem;
  }

  .timeline-item:nth-child(even) {
    left: 50%;
    padding-left: 4rem;
  }

  .timeline-item::after {
    content: '';
    position: absolute;
    width: 20px;
    height: 20px;
    right: -10px;
    background-color: #12161c;
    border: 4px solid #00bfff;
    top: 25px;
    border-radius: 50%;
    z-index: 1;
    top: 50%;
    transform: translateY(-50%);
  }

  .timeline-item:nth-child(odd)::after {
    right: -12px;
  }
  .timeline-item:nth-child(even)::after {
    left: -12px;
  }


  .timeline-content {
    padding: 2rem;
    background: #181c24;
    position: relative;
    border-radius: 8px;
    box-shadow: 0 4px 25px rgba(0,0,0,0.2);
    transition: transform 0.3s ease;
  }

  .timeline-content:hover {
    transform: translateY(-5px);
  }

  .company-logo {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    position: absolute;
    top: -25px;
    left: 50%;
    transform: translateX(-50%);
    border: 3px solid #00bfff;
    background: #fff;
  }

  h3 {
    font-size: 1.5rem;
    color: #00bfff;
    margin-top: 20px; /* Space for logo */
    margin-bottom: 0.5rem;
  }

  h4 {
    font-size: 1.2rem;
    color: #eee;
    margin-bottom: 0.5rem;
  }

  .period {
    display: block;
    color: #888;
    font-size: 0.9rem;
    margin-bottom: 1rem;
  }

  p {
    color: #ccc;
    line-height: 1.5;
  }

  /* Responsive */
  @media screen and (max-width: 768px) {
    .timeline::after {
      left: 20px;
    }

    .timeline-item {
      width: 100%;
      padding-left: 50px;
      padding-right: 15px;
    }

    .timeline-item:nth-child(even) {
      left: 0;
    }

    .timeline-item::after {
      left: 10px;
    }
  }
</style>