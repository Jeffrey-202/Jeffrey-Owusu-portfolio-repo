<script>
  import { onMount } from 'svelte';
  import { fade, fly } from 'svelte/transition';
  import Header from '$lib/components/Header.svelte';
  import Footer from '$lib/components/Footer.svelte';
  
  onMount(() => {
      console.log("Home Page Loaded");
  });
</script>

<title>Jeffrey Owusu - About page</title>
  <meta name="about page" content="the about page" />
<link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />


<main class="about-page">
  <section class="hero">
    <div class="container">
      <h1 class="title animate__animated animate__fadeInDown">About <span class="highlight">Me</span></h1>
    </div>
  </section>

  <section class="about-section">
    <div class="container grid">
      <div class="profile" in:fade={{ duration: 800 }}>
        <img src="profile.jpg" alt="Jeffrey Owusu portrait" class="profile-img" />
      </div>
      
      <div class="bio" in:fly={{ y: 50, duration: 800 }}>
        <h2>Who Am I?</h2>
        <p>
          I'm Jeffrey Owusu, i'm a 22 year old student from Longford currently studying digital art and design in S.E.T.U carlow
        </p>
        <p>
          I have a passion when it comes to Art and other forms of media such as music, video editing, graphic design etc. I love to explore new creative skills and push the boundaries of my creativity.
        </p>
      </div>
    </div>
  </section>

  <section class="skills-section">
    <div class="container">
      <h2 class="section-title animate__animated animate__fadeIn">My Skills & Interests</h2>
      <div class="skills-grid">
        <!-- Languages Column -->
        <div class="skill-card" in:fade={{ delay: 200, duration: 600 }}>
          <div class="skill-icon">
            <i class="fas fa-language"></i>
          </div>
          <h3>Programming Languages</h3>
          <ul class="skill-list">
            <li>JavaScript</li>
            <li>CSS</li>
            <li>HTML</li>
            <li>SQL</li>
          </ul>
        </div>
        
        <!-- Art Column -->
        <div class="skill-card" in:fade={{ delay: 400, duration: 600 }}>
          <div class="skill-icon">
            <i class="fas fa-palette"></i>
          </div>
          <h3>Art & Design</h3>
          <ul class="skill-list">
            <li>Web design</li>
            <li>Graphic Design</li>
            <li>3D Modeling</li>
            <li>Digital art</li>
            <li>Traditional art</li>
          </ul>
        </div>
        
        <!-- Media Column -->
        <div class="skill-card" in:fade={{ delay: 600, duration: 600 }}>
          <div class="skill-icon">
            <i class="fas fa-film"></i>
          </div>
          <h3>Media</h3>
          <ul class="skill-list">
            <li>Video Editing</li>
            <li>Music production</li>
            <li>Social media marketing</li>
            <li>Content Creation</li>
          </ul>
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
    padding: clamp(40px, 8vw, 80px) 0;
    text-align: center;
    font-family: 'Audiowide', sans-serif;
  }

  .title {
    font-size: clamp(2rem, 5vw, 3.5rem);
    margin: 0;
    font-weight: 800;
    font-family: 'Audiowide', sans-serif;
    line-height: 1.2;
    animation: pulse 2s infinite alternate;
  }

  @keyframes pulse {
    from { transform: scale(1); }
    to { transform: scale(1.03); }
  }

  .highlight {
    color: #075e35;
    position: relative;
    display: inline-block;
  }

  .highlight::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 100%;
    height: 3px;
    background: white;
    transform: scaleX(0);
    transform-origin: right;
    transition: transform 0.3s ease;
  }

  .highlight:hover::after {
    transform: scaleX(1);
    transform-origin: left;
  }

  .subtitle {
    font-size: clamp(1.2rem, 3vw, 1.5rem);
    opacity: 0.9;
    margin-top: 10px;
    transition: all 0.3s ease;
  }

  .subtitle:hover {
    letter-spacing: 1px;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: clamp(30px, 5vw, 50px);
    align-items: center;
    padding: clamp(30px, 5vw, 60px) 0;
  }

  .profile {
    display: flex;
    justify-content: center;
  }

  .profile-img {
    width: 100%;
    max-width: 400px;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.1);
    transition: all 0.5s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }

  .profile-img:hover {
    transform: rotate(-2deg) scale(1.02);
    box-shadow: 0 15px 40px rgba(0,0,0,0.2);
  }

  .bio {
    font-family: 'Inter', sans-serif;
    text-align: left;
    max-width: 600px;
    font-size: clamp(1rem, 2vw, 1.2rem);
    margin: 0 auto;
  }

  .bio h2 {
    font-size: clamp(1.5rem, 3vw, 2rem);
    margin-bottom: 20px;
    color: var(--secondary);
  }

  .skills-section {
    padding: 40px 0;
    background: linear-gradient(#14680d, #a9ff62);
  }

  .section-title {
    text-align: center;
    font-size: clamp(1.8rem, 4vw, 2.5rem);
    margin-bottom: clamp(30px, 5vw, 50px);
    color: var(--light);
    text-shadow: 0 2px 5px rgba(0,0,0,0.2);
  }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: clamp(20px, 3vw, 30px);
  }

  .skill-card {
    background: var(--light);
    border-radius: 15px;
    padding: clamp(20px, 3vw, 30px);
    box-shadow: 0 5px 15px rgba(8, 26, 3, 0.05);
    transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
  }

  .skill-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 30px rgba(8, 26, 3, 0.15);
  }



  .skill-card:hover .skill-icon {
    transform: rotate(15deg) scale(1.2);
  }

  .skill-card h3 {
    font-size: clamp(1.2rem, 2.5vw, 1.5rem);
    margin-bottom: clamp(15px, 3vw, 20px);
    color: var(--secondary);
    position: relative;
    display: inline-block;
    text-align: center;
    width: 100%;
  }

  .skill-card h3::after {
    content: '';
    position: absolute;
    bottom: -8px;
    left: 50%;
    transform: translateX(-50%);
    width: 0;
    height: 3px;
    background: var(--primary);
    transition: width 0.3s ease;
  }

  .skill-card:hover h3::after {
    width: 80%;
  }

  .skill-list {
    list-style-type: none;
    padding: 0;
    text-align: center;
  }

  .skill-list li {
    padding: 8px 0;
    border-bottom: 1px solid #eee;
    transition: all 0.2s ease;
    font-size: clamp(0.9rem, 2vw, 1rem);
  }

  .skill-list li:hover {
    color: var(--secondary);
    padding-left: 5px;
  }

  .skill-list li:last-child {
    border-bottom: none;
  }

  /* Mobile-specific adjustments */
  @media (max-width: 480px) {
    .hero {
      padding: 30px 0;
    }
    
    .title {
      font-size: 2.2rem;
    }
    
    .subtitle {
      font-size: 1.2rem;
    }
    
    .grid {
      gap: 20px;
    }
    
    .profile-img {
      max-width: 280px;
    }
    
    .bio {
      text-align: center;
    }
    
    .skills-section {
      padding: 30px 0;
    }
    
    .skill-card {
      padding: 20px 15px;
    }
  }

  /* Tablet-specific adjustments */
  @media (min-width: 481px) and (max-width: 768px) {
    .hero {
      padding: 50px 0;
    }
    
    .title {
      font-size: 2.8rem;
    }
    
    .subtitle {
      font-size: 1.4rem;
    }
    
    .grid {
      grid-template-columns: 1fr;
    }
    
    .profile {
      justify-content: center;
      margin-bottom: 30px;
    }
    
    .bio {
      text-align: center;
    }
    
    .skills-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }
</style>