<script lang="ts">
  const specializations = [
    { name: 'Laravel', icon: '/icons/laravel.png' },
    { name: 'Vue', icon: '/icons/vue.png' },
    { name: 'React', icon: '/icons/react.png' },
    { name: 'Flutter', icon: '/icons/flutter.png' },
    { name: 'Go', icon: '/icons/golang.png' },
    { name: 'Google Cloud', icon: '/icons/gcloud.png' },
    { name: 'Wordpress', icon: '/icons/wordpress.png' },
    { name: 'ASP.NET', icon: '/icons/asp.png' },
    { name: 'HTML', icon: '/icons/html.png' },
  ];
</script>

<section id="about">
  <div class="about-container">
    <div class="about-image">
      <img src="/personals/profile.png" alt="Teuku Vaickal Rizki Irdian" />
    </div>
    <div class="about-text">
      <h2>About Me</h2>
      <p>
        I am a student at Bina Sarana Informatika University, majoring in Information Systems. I am passionate about technology and have experience in various fields such as web development, mobile app development, and cloud computing. I am a fast learner and always eager to learn new things.
      </p>
      <h3>Specializations</h3>
      <div class="specializations-grid">
        {#each specializations as spec}
          <div class="spec-card">
            <img src="{spec.icon}" alt="{spec.name}" class="spec-icon"/>
            <span>{spec.name}</span>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>

<style>
  #about {
    background-color: #181c24;
    padding: 6rem 2rem;
  }

  .about-container {
    display: grid;
    grid-template-columns: 1fr 2fr;
    gap: 3rem;
    max-width: 1200px;
    margin: 0 auto;
    align-items: center;
  }

  .about-image img {
    max-width: 100%;
    border-radius: 50%;
    border: 5px solid #00bfff;
    box-shadow: 0 0 25px rgba(0, 191, 255, 0.5);
  }

  h2 {
    font-size: 2.5rem;
    color: #fff;
    margin-bottom: 1.5rem;
  }

  p {
    color: #ccc;
    line-height: 1.6;
    margin-bottom: 2rem;
  }

  h3 {
    font-size: 1.8rem;
    color: #00bfff;
    margin-bottom: 1.5rem;
  }

  .specializations-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1.5rem;
  }

  .spec-card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: #222831;
    padding: 1.5rem;
    border-radius: 10px;
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .spec-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.4);
  }

  .spec-icon {
    width: 50px;
    height: 50px;
    margin-bottom: 1rem;
  }

  .spec-card span {
    color: #fff;
    font-weight: 500;
  }

  /* Responsive */
  @media (max-width: 768px) {
    .about-container {
      grid-template-columns: 1fr;
      text-align: center;
    }

    .about-image {
      margin-bottom: 2rem;
    }
    .specializations-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 480px) {
    .specializations-grid {
      grid-template-columns: 1fr;
    }
  }
</style>