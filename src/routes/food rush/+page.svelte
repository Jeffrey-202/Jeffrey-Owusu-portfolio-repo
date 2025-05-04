<script>
    import { onMount } from 'svelte';
    
    onMount(() => {
        console.log("Home Page Loaded");
    });
</script>


    <title>Food Rush Game</title>
    <meta name="description" content="The Food Rush game - an exciting food-themed adventure" />
    <link href="https://fonts.googleapis.com/css2?family=Audiowide&family=Inter:wght@400;600&display=swap" rel="stylesheet">

<main class="game-page">
    <h1>Food Rush</h1>
    
    <div class="content-wrapper">
        <section class="game-description">
            <p>Food Rush is a game that I've I created for a UI programming project.</p>
            <p>The aim of the game is to collect as much food as you can. When you get hit by 4 boulders it's game over and you restart.</p>
            <p>For mobile devices you can use the left and right buttons on the screen to move the character and for desktop devices you can use the left and right arrow keys on your keyboard </p>
             <a href="https://ui-programming-24-25.codeberg.page/C00314408-Jeffrey-Owusu-Programming-project/" target="_blank" rel="noopener noreferrer">click here to play</a>
        
        </section>

       
        
        <div class="media-container">
            <figure class="screenshot">
                <img 
                    src="foodrush.jpg" 
                    alt="Food Rush game screenshot showing the gameplay" 
                    class="game-image"
                    loading="lazy"
                />
                <figcaption>Gameplay screenshot</figcaption>
            </figure>
            
            <figure class="video-container">
                <video width="600" height="600" controls poster="foodrush-poster.jpg">
                    <source src="foodrush.mp4" type="video/mp4">

                </video>
                <figcaption>Gameplay demonstration</figcaption>
            </figure>
        </div>
    </div>
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
    .game-page {
        max-width: 1200px;
        margin: 0 auto;
        padding: 2rem;
    }
    
    h1 {
        font-family: 'Audiowide', cursive;
        text-align: center;
        color: 
        margin-bottom: 2rem;
        font-size: 2.5rem;
        text-shadow: 1px 1px 2px rgba(0,0,0,0.1);
   
    }
       
       
    p {
        font-size: 1.5rem;
        line-height: 1.5;
        color: #000000;
        margin-bottom: 1rem;
        font-family: 'Inter', sans-serif;
    }
   
    .content-wrapper {
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }
    
    .game-description {
        text-align: center;
        max-width: 800px;
        margin: 0 auto;
        font-size: 1.1rem;
    }
    
    .media-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 2rem;
    }
    
    .game-image {
        max-width: 100%;
        height: auto;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        transition: transform 0.3s ease;
    }
    
    .game-image:hover {
        transform: scale(1.02);
    }
    
    .video-container {
        width: 100%;
        max-width: 600px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    
    video {
        width: 100%;
        height: auto;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    
    figcaption {
        margin-top: 0.5rem;
        font-style: italic;
        color: #666;
        text-align: center;
    }
    
    @media (max-width: 768px) {
        .game-page {
            padding: 1rem;
        }
        
        h1 {
            font-size: 2rem;
        }
    }
</style>