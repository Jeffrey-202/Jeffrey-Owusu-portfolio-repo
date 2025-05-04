<script>
    import { onMount } from 'svelte';
    import { fade, fly } from 'svelte/transition';
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    
    onMount(() => {
        console.log("Digital Art Gallery Loaded");
    });
</script>





    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital art gallery</title>
    <link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">



<h1 >Digital Art</h1>

<div class="gallery-container">
    <!-- Art Piece 1 -->
    <div class="full-width-art" in:fade={{ delay: 100, duration: 600 }}>
        <img src="dizzy.jpg" alt="Marvin the Mayor 3D model" class="large-art-image"/>
        <div class="art-info">
            <h2>Dizzy - Jeffrey Owusu</h2>
            <p>Jonathan and his cat feeling dizzy</p>
        </div>
    </div>

    <!-- Art Piece 2 -->
    <div class="full-width-art" in:fade={{ delay: 200, duration: 600 }}>
        <img src="mayor weapon.jpg" alt="Marvin the Mayor weapon" class="large-art-image"/>
        <div class="art-info">
            <h2>Marvin the mayor's weapon - Jeffrey Owusu</h2>
            <p>Concept art for the game Mole Patrol</p>
        </div>
    </div>

    <!-- Art Piece 3 -->
    <div class="full-width-art" in:fade={{ delay: 300, duration: 600 }}>
        <img src="thelad.jpg" alt="Character portrait" class="large-art-image"/>
        <div class="art-info">
            <h2>The Lad - Jeffrey Owusu</h2>
            <p>He's just a lad</p>
        </div>
    </div>

    <!-- Art Piece 4 -->
    <div class="full-width-art" in:fade={{ delay: 400, duration: 600 }}>
        <img src="mayor concept.jpg" alt="Enemy mole concept art" class="large-art-image"/>
        <div class="art-info">
            <h2>Marvin the mayor</h2>
            <p>Concept art for the game Mole Patrol</p>
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
  line-height: 1.6;
}
    
    
    
    h1 {
        font-family: 'Audiowide', cursive;
        text-align: center;
        margin: 2rem 0;
        font-size: 2.5rem;
        color: #000000;
    }

    .gallery-container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 20px;
    }

    .full-width-art {
        margin-bottom: 4rem;
        background: #f8f8f8;
        border-radius: 8px;
        overflow: hidden;
        box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .full-width-art:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 20px rgba(0,0,0,0.15);
    }

    .large-art-image {
        width: 100%;
        height: auto;
        max-height: 80vh;
        object-fit: contain;
        display: block;
        background: #000;
        transition: transform 0.5s ease;
    }

    .full-width-art:hover .large-art-image {
        transform: scale(1.02);
    }

    .art-info {
        padding: 2rem;
        transition: background-color 0.3s ease;
    }

    .full-width-art:hover .art-info {
        background-color: #f0f0f0;
    }

    .art-info h2 {
        font-family: 'Audiowide', cursive;
        margin-bottom: 1rem;
        color: #222;
        font-size: 1.8rem;
        transition: color 0.3s ease;
    }

    .full-width-art:hover .art-info h2 {
        color: #000;
    }

    .art-info p {
        color: #555;
        line-height: 1.6;
        font-size: 1.1rem;
        max-width: 800px;
        margin: 0 auto;
        transition: color 0.3s ease;
    }

    .full-width-art:hover .art-info p {
        color: #333;
    }

    @media (max-width: 768px) {
        .art-info {
            padding: 1.5rem;
        }
        
        .art-info h2 {
            font-size: 1.5rem;
        }
        
        .art-info p {
            font-size: 1rem;
        }

        .full-width-art:hover {
            transform: none;
        }
    }
</style>