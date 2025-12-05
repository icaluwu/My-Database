<script lang="ts">
  const volunteering = [
    {
      role: 'Google Student Ambassador 2025',
    },
    {
      role: 'Event Committee',
      event: 'PKKMB UBSI 2023',
    },
  ];
</script>

<section id="volunteering">
  <h2>Volunteering</h2>
  <div class="volunteer-grid">
    {#each volunteering as item}
      <div class="volunteer-card">
        <h4>{item.role}</h4>
        {#if item.event}
          <p>{item.event}</p>
        {/if}
      </div>
    {/each}
  </div>
</section>

<style>
  #volunteering {
    padding: 4rem 2rem;
    background-color: #181c24;
  }

  h2 {
    text-align: center;
    font-size: 2.5rem;
    color: #fff;
    margin-bottom: 3rem;
  }

  .volunteer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .volunteer-card {
    background-color: #222831;
    padding: 1.5rem;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    text-align: center;
  }

  h4 {
    color: #00bfff;
    margin-bottom: 0.5rem;
  }
</style>