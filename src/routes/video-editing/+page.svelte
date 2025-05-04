<script>
    import { onMount } from 'svelte';
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    
    onMount(() => {
        console.log("video-editing Page Loaded");
    });

    const videos = [
        { id: 1, title: "Jermemy kyle", mp4: "jeremy kyle.mp4", ogg: "lebronedit.ogg" },
        { id: 2, title: "Nemzz edit", mp4: "nemzz.mp4", ogg: "nemzz.mp4" },
        { id: 3, title: "Maury show edit", mp4: "notthefather.mp4", ogg: "pizza.ogg" },
        { id: 4, title: "Rats n lasers edit", mp4: "ratsnlasers.mp4", ogg: "ratsnlasers.ogg" },
        { id: 5, title: "druski edit", mp4: "druski.mp4", ogg: "druski.ogg" },
        { id: 6, title: "big fan man edit", mp4: "bigfan.mp4", ogg: "bigfan.ogg" }
    ];
</script>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Video Editing Gallery</title>
<link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">

<div class="video-editing-title">
    <h1>My edits</h1>
</div>

<p> </p>


<div class="container"> 
    {#each videos as video}
    <div class="video-box">
        <h2>{video.title}</h2>
        <div class="video-wrapper">
            <video controls>
                <source src={video.mp4} type="video/mp4">
                <source src={video.ogg} type="video/ogg">
                Your browser doesn't support videos
            </video>
        </div>
    </div>
    {/each}
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
    }
    
    .video-editing-title h1 {
        font-family: 'Audiowide', sans-serif;
        font-size: 3rem;
        text-align: center;
        margin: 30px 0;
        color: var(--dark);
        text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
    }
    
    .container {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 30px;
        max-width: 1400px;
        margin: 0 auto;
        padding: 30px;
    }
    
    .video-box {
        background: rgb(12, 49, 3);
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        transition: transform 0.3s ease;
    }
    
    .video-box:hover {
        transform: translateY(-5px);
    }
    
    h2 {
        margin: 0 0 15px 0;
        font-size: 1.5rem;
        color: var(--light);
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        text-align: center;
    }
    
    .video-wrapper {
        position: relative;
        padding-bottom: 56.25%; /* 16:9 aspect ratio */
        height: 0;
        overflow: hidden;
    }
    
    .video-wrapper video {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border-radius: 8px;
    }
    
    @media (max-width: 900px) {
        .container {
            grid-template-columns: 1fr;
            max-width: 700px;
        }
        
        .video-editing-title h1 {
            font-size: 2.5rem;
        }
    }
    
    @media (max-width: 600px) {
        .container {
            padding: 15px;
            gap: 20px;
        }
        
        .video-box {
            padding: 15px;
        }
        
        .video-editing-title h1 {
            font-size: 2rem;
            margin: 20px 0;
        }
        
        h2 {
            font-size: 1.3rem;
        }
    }
</style>