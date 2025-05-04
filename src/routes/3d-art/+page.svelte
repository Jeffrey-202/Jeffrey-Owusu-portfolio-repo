<script>
    import { onMount } from 'svelte';
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    onMount(() => {
        console.log("3D-art Page Loaded");
    });
</script>

<title>3d Art</title>
  <meta name="description" content="3D Art page" />
  <link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">




    <title>3D Art</title>
    <link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500&display=swap" rel="stylesheet">


<div class="container">
    <h1>3D Art </h1>
    
    <div class="intro">
        <p>These are the low poly style 3D art pieces that i've made for the game mole patrol using blender</p>
      
    </div>

    <div class="art-gallery">
        <div class="art-piece">
            <img src="mayor.png" alt="Marvin the Mayor 3D model" class="art-image"/>
            <div class="art-description">
                <h2 class="art-title">Marvin the Mayor</h2>
            </div>
        </div>

        <div class="art-piece">
            <img src="bullet.png" alt="3D bullet model" class="art-image"/>
            <div class="art-description">
                <h2 class="art-title">Bullet 3D</h2>
            </div>
        </div>
    </div>
</div>

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
  line-height: 1.6
    }

    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 2rem;
    }

    h1 {
        font-family: 'Audiowide', cursive;
        color: #212529;
        text-align: center;
        margin-bottom: 1.5rem;
        font-size: 2.5rem;
    }

     P {
        font-size: 1.5rem;
      color: #000000;
      margin-top: 10px;
     font-family: 'Arial', sans-serif;
    }
     

    .intro {
        text-align: center;
        margin-bottom: 3rem;
        line-height: 1.6;
    }

    .art-gallery {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 2rem;
    }

    .art-piece {
        background: white;
        border-radius: 4px;
        overflow: hidden;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease;
    }

    .art-piece:hover {
        transform: translateY(-5px);
    }

    .art-image {
        width: 100%;
        height: auto;
        display: block;
    }

    .art-description {
        padding: 1.5rem;
    }

    .art-title {
        font-family: 'Audiowide', cursive;
        margin: 0 0 0.5rem 0;
        color:#212529 ;
        font-size: 1.3rem;
    }


</style>