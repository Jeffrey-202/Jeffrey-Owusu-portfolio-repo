<script>
    import { onMount } from 'svelte';
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    
    onMount(() => {
        console.log("Drawings Page Loaded");
    });

    const images = [
        { src: "girl.jpg", alt: "Girl drawing" },
        { src: "freg.jpg", alt: "Freg drawing" },
        { src: "blocky1.jpg", alt: "Blocky character 1" },
        { src: "blocky2.jpg", alt: "Blocky character 2" },
        { src: "blocky3.jpg", alt: "Blocky character 3" },
        { src: "blocky4.jpg", alt: "Blocky character 4" },
        { src: "mouse.jpg", alt: "Mouse drawing" },
        { src: "barty.jpg", alt: "Barty drawing" },
        { src: "car.jpg", alt: "Car drawing" },
        { src: "orange.jpg", alt: "Orange drawing" },
        { src: "fire sketch.jpg", alt: "Fire sketch" },
        { src: "attached.jpg", alt: "Attached drawing" },
        { src: "bottle sketch.jpg", alt: "Bottle sketch" },
        { src: "mann.jpg", alt: "Mann drawing" }
    ];
</script>

<title>Drawings gallery</title>
<meta name="description" content="Gallery of artistic drawings" />
<link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">

<main class="gallery-container">
    <h1>My Drawings</h1>
    <div class="gallery-grid">
        {#each images as image}
            <div class="gallery-item">
                <img 
                    src={image.src} 
                    alt={image.alt}
                    loading="lazy"
                    width="600" 
                    height="600"
                />
            </div>
        {/each}
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
    
    .gallery-container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 2rem;
    }
    
    h1 {
        font-family: 'Audiowide', cursive;
        text-align: center;
        margin-bottom: 2rem;
    }
    
    .gallery-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 20px;
    }
    
    .gallery-item {
        overflow: hidden;
        border-radius: 8px;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease;
        background-color: var(--light);
        aspect-ratio: 1/1;
    }
    
    .gallery-item:hover {
        transform: scale(1.03);
    }
    
    .gallery-item img {
        width: 100%;
        height: 100%;
        display: block;
        object-fit: cover;
        transition: opacity 0.3s ease;
    }
    
    .gallery-item:hover img {
        opacity: 0.9;
    }
    
    @media (max-width: 768px) {
        .gallery-grid {
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
        }
    }
</style>