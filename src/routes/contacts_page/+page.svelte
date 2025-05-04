<script>
  import { onMount } from 'svelte';
  import Header from '$lib/components/Header.svelte';
  import Footer from '$lib/components/Footer.svelte';
  
  onMount(() => {
    console.log("Contact Page Loaded");
  });
</script>


  <title>Contact</title>
  <meta name="description" content="contact me" />
  <link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">


<main class="contact-page">
  <section class="hero">
    <div class="container">
      <h1 class="title">Contact Me</h1>
    </div>
  </section>

  <section class="contact-section">
    <div class="container">
      <div class="contact-info">
        <h2>Contact Information</h2>
        <div class="info-grid">
          <div class="info-item">
            <h3>Phone</h3>
            <span>+353 899 89 3830</span>
          </div>
          <div class="info-item">
            <h3>Email</h3>
            <span>jeffreyoseiowusu202@gmail.com</span>
          </div>
          <div class="info-item">
            <h3>Location</h3>
            <span>Longford, Ireland</span>
          </div>
        </div>
        
        <div class="social-links">
          <a href="https://github.com/Jeffrey-202" class="social-link">GitHub idad</a>
          <a href="https://github.com/jaythelad" class="social-link">GitHub 2 </a>
          <a href="https://codeberg.org/Jeffrey_02" class="social-link">Codeberg</a>
          <a href="https://www.instagram.com/jeffreyowusu202" class="social-link">Instagram</a>
        </div>
      </div>
    </div>
  </section>
</main>

<style>
  :global(body) {
    --primary: #a9ff62;
    --secondary: #14680d;
    --dark: #212529;
    --light: #f8f9fa;
    margin: 0;
    font-family: 'Inter', sans-serif;
    color: var(--dark);
    background-color: var(--primary);
    line-height: 1.6;
  }

  .container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
    box-sizing: border-box;
  }

  .hero {
    background: linear-gradient(135deg, var(--primary), var(--secondary));
    color: white;
    padding: 60px 0;
    text-align: center;
  }

  .title {
    font-size: clamp(2rem, 5vw, 3rem);
    margin: 0;
    font-weight: 600;
    line-height: 1.2;
    font-family: audiowide, sans-serif;
  }

  .contact-section {
    padding: 40px 0;
  }

  .contact-info h2 {
    font-size: clamp(1.5rem, 3vw, 2rem);
    margin-bottom: 30px;
    color: var(--secondary);
    text-align: center;
  }

  .info-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
    margin-bottom: 40px;
  }

  .info-item {
    padding: 20px;
    background: white;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  }

  .info-item h3 {
    margin: 0 0 8px 0;
    color: var(--secondary);
    font-size: 1.1rem;
    font-weight: 600;
  }

  .info-item span {
    font-size: 1rem;
    color: var(--dark);
    word-break: break-word;
  }

  .social-links {
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 40px;
    flex-wrap: wrap;
  }

  .social-link {
    padding: 10px 20px;
    background: var(--primary);
    color: white;
    border-radius: 6px;
    text-decoration: none;
    font-weight: 500;
    transition: all 0.2s ease;
    font-size: 0.95rem;
    text-align: center;
  }

  .social-link:hover {
    background: var(--secondary);
  }

  /* Mobile-specific styles */
  @media (max-width: 480px) {
    .hero {
      padding: 40px 0;
    }
    
    .info-grid {
      grid-template-columns: 1fr;
    }

    .social-links {
      flex-direction: column;
      align-items: center;
    }

    .social-link {
      width: 100%;
      max-width: 200px;
    }
  }

  /* Tablet-specific styles */
  @media (min-width: 481px) and (max-width: 768px) {
    .info-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }
</style>