<script>
    import { onMount } from 'svelte';
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    
    onMount(() => {
        console.log("Contact Page Loaded");
    });
</script>


    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>graphic design gallery</title>
    <link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">

<main>
    <h2>Graphic design</h2>

    <div class="gallery-container">
        <div class="responsive">
            <div class="gallery">
                <a target="_blank" href="casa.jpg">
                <img src="casa.jpg" alt="Modern house architecture" loading="lazy">
                <div class="desc">Casa</div>
            </div>
        </div>

        <div class="responsive">
            <div class="gallery">
                <a target="_blank" href="Board.jpg">
                    <img src="Board.jpg" alt="Skateboard on pavement" loading="lazy">
                </a>
                <div class="desc">city poster with my custom font </div>
            </div>
        </div>

        <div class="responsive">
            <div class="gallery">
                <a target="_blank" href="son.jpg">
                <img src="son.jpg" alt="Father and son at beach" loading="lazy">
                <div class="desc">Son poster</div>
            </div>
        </div>

        <div class="responsive">
            <div class="gallery">
                <a href="cartoons.png">
                    <img src="cartoons.png" alt="cartoon pic" loading="lazy">
                </a>
                <div class="desc">Cartoons at Mels</div>
            </div>
        </div>
    </div>

    <div class="gallery-info">
        <p>click on image for full view</p>
    </div>
</main>

<style>
    main {
        max-width: 1400px;
        margin: 0 auto;
        padding: 20px;
    }


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

    p {
        font-family: 'arial', cursive;
        font-size: 1.2rem;
        text-align: center;
        color: #000000;
    }

    h2 {
        text-align: center;
        font-family: 'Audiowide', cursive;
        margin: 20px 0 40px;
        color: #000000;
        font-size: 2.5rem;
    }

    .gallery-container {
        display: flex;
        flex-wrap: wrap;
        gap: 30px;
        justify-content: center;
    }

    .responsive {
        width: calc(25% - 20px);
        min-width: 250px;
    }

    .gallery {
        height: 100%;
        display: flex;
        flex-direction: column;
        border: 1px solid #eee;
        border-radius: 8px;
        transition: all 0.3s ease;
        background: white;
        overflow: hidden;
        box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }

    .gallery:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 15px rgba(0,0,0,0.1);
    }

    .gallery img {
        width: 100%;
        height: 300px;
        object-fit: cover;
        object-position: center;
        transition: transform 0.3s ease;
    }

    .gallery:hover img {
        transform: scale(1.05);
    }

    .desc {
        padding: 20px;
        text-align: center;
        font-family: Arial, bold;
        color: #000000;
        background: #f9f9f9;
        border-top: 1px solid #eee;
        font-size: 1.2rem;
        font-weight: 600;
    }

    .gallery-info {
        padding: 30px;
        margin-top: 40px;
        text-align: center;
        font-family: Arial, sans-serif;
        color: #666;
        font-size: 1.1rem;
        line-height: 1.6;
    }

    /* Medium screens - 2 columns */
    @media screen and (max-width: 1024px) {
        .responsive {
            width: calc(50% - 20px);
        }
    }

    /* Small screens - 1 column */
    @media screen and (max-width: 600px) {
        .responsive {
            width: 100%;
            max-width: 400px;
        }
        
        .gallery img {
            height: 350px;
        }
    }
</style>