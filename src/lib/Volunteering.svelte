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

<style>
  #volunteering {
    background-color: #12161c;
    padding: 6rem 2rem;
  }

  .section-title {
    text-align: center;
    font-size: 2.5rem;
    color: #fff;
    margin-bottom: 4rem;
  }

  .volunteer-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 2.5rem;
    max-width: 1200px;
    margin: 0 auto;
  }

  .volunteer-card {
    position: relative;
    background: rgba(34, 40, 49, 0.65);
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .volunteer-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
  }

  .volunteer-card:hover .card-border {
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
    border-radius: 11px;
  }

  .volunteer-info {
    padding: 2rem;
    display: flex;
    align-items: flex-start; /* Align items to the top */
    gap: 1.5rem;
  }

  .volunteer-logo {
    width: 60px;
    height: 60px;
    object-fit: contain;
    border-radius: 10px;
    flex-shrink: 0; /* Prevent logo from shrinking */
  }

  .volunteer-text {
    display: flex;
    flex-direction: column;
  }

  h4 {
    color: #00bfff;
    font-size: 1.3rem;
    line-height: 1.4;
    margin: 0;
    margin-bottom: 0.25rem;
  }

  .organization {
    color: #bbb;
    font-size: 0.9rem;
    margin-bottom: 1rem;
  }

  .description {
    color: #ccc;
    line-height: 1.6;
    font-size: 0.95rem;
    margin: 0;
  }

  @media (max-width: 480px) {
    #volunteering {
      padding: 4rem 1rem;
    }
    .volunteer-grid {
      grid-template-columns: 1fr;
    }
    .volunteer-info {
      flex-direction: column;
      align-items: center;
      text-align: center;
    }
  }
</style>