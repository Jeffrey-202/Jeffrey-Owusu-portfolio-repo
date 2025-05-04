<script>
    import { onMount } from 'svelte';
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    
    onMount(() => {
        console.log("Video Editing Gallery Page Loaded");
    });
</script>

<svelte:head>
    <title>projects</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link href="https://fonts.googleapis.com/css2?family=Audiowide&family=Inter:wght@400;500;700&display=swap" rel="stylesheet" />
</svelte:head>



<main class="container">
    <h1>Projects</h1>
    <p class="subtitle">Use dropdown toggle to navigate through projects</p>
    
    <!-- Placeholder for your video gallery content -->
    <div class="gallery">
        <!-- Your video projects would go here -->
    </div>
</main>



<style>
    :global(body) {
        --primary: #a9ff62;
        --secondary: #14680d;
        --dark: #212529;
        --light: #f8f9fa;
        
        margin: 0;
        padding: 0;
        font-family: 'Inter', sans-serif;
        color: var(--dark);
        background-color: var(--primary);
        line-height: 1.6;
    }

    .container {
        width: 100%;
        max-width: 1200px;
        margin: 0 auto;
        padding: 20px;
        box-sizing: border-box;
    }

    h1 {
        font-family: 'Audiowide', sans-serif;
        font-size: clamp(2rem, 5vw, 2.5rem); /* Responsive font size */
        text-align: center;
        margin: 20px 0 10px;
        color: var(--dark);
    }

    .subtitle {
        font-family: 'Audiowide', sans-serif;
        font-size: clamp(1rem, 3vw, 1.5rem); /* Responsive font size */
        text-align: center;
        margin: 0 auto 30px;
        color: var(--dark);
        max-width: 600px;
    }

    .gallery {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        gap: 20px;
        padding: 20px 0;
    }

    /* Responsive adjustments */
    @media (max-width: 768px) {
        .container {
            padding: 15px;
        }
        
        .gallery {
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
        }
    }

    @media (max-width: 480px) {
        .gallery {
            grid-template-columns: 1fr;
        }
    }
</style>