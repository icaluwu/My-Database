<script lang="ts">
  const volunteerExperiences = [
    {
      role: 'Google Student Ambassador 2025',
      organization: 'Google',
      icon: '/volunteers/googlestudentambassador.png',
      year: '2025',
      description: 'Representing Google and fostering a developer community at Bina Sarana Informatika University.'
    },
    {
      role: 'Event Committee',
      organization: 'PKKMB UBSI 2023',
      icon: '/volunteers/ubsi.png',
      year: '2023',
      description: 'Contributed to the successful execution of the university\'s new student orientation program.'
    }
  ];
</script>

<section id="volunteering">
  <h2 class="section-title">Volunteering</h2>
  <div class="volunteer-grid">
    {#each volunteerExperiences as item}
      <div class="volunteer-card">
        <div class="card-border"></div>
        <div class="card-content">
          <div class="volunteer-info">
            <img src="{item.icon}" alt="{item.organization} logo" class="volunteer-logo">
            <div class="volunteer-text">
                <h4>{item.role}</h4>
                <p class="organization">{item.organization} &bull; {item.year}</p>
                <p class="description">{item.description}</p>
            </div>
          </div>
        </div>
      </div>
    {/each}
  </div>
</section>