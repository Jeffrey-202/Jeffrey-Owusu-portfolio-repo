<script>

    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
    import { onMount } from 'svelte';

    const videos = [
      { id: 1, title: "leostaytrill pink lemonade remix", mp4: "vid1.mp4", ogg: "vid1.ogg" },
      { id: 2, title: "hope instrumental", mp4: "vid2.mp4", ogg: "vid2.ogg" },
      { id: 3, title: "above the horizons", mp4: "vid3.mp4", ogg: "vid3.ogg" },
      { id: 4, title: "sainte champagne shots remix", mp4: "vid4.mp4", ogg: "vid4.ogg" },
      { id: 5, title: "chip tim westwood freestyle remix", mp4: "vid5.mp4", ogg: "vid5.ogg" },
      { id: 6, title: "playboi carti 2024 remix", mp4: "vid6.mp4", ogg: "vid6.ogg" }
    ];
  </script>
 

 <title>music</title>
 <meta name="music" content="music page" />
 <link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">



 <div class="music-title">
<h1>Music</h1>
<p>These are the remixes and instrumenals that i've made</p>
<p>You can find my other remixes and instrumenals soundcloud</p>
<button class="soundcloud-button" on:click={() => window.open('https://soundcloud.com/jepaloon')}>Visit SoundCloud</button>
</div>



<div class="container"> 
    {#each videos as video}
      <div class="video-box">
        <h2>{video.title}</h2>
        <video width="500" height="280" controls>
          <source src={video.mp4} type="video/mp4">
          <source src={video.ogg} type="video/ogg">
          Your browser doesn't support videos
        </video>
      </div>
    {/each}
  </div>
  
  <style> :global(body) {
    --primary: #a9ff62;
    --secondary: #14680d;
    --dark: #212529;
    --light: #f8f9fa;
    margin: 0;
    font-family: 'Inter', sans-serif;
    color: var(--dark);
    background-color: var(--primary);
  }


  
    
    .page-title {
      font-family: 'Audiowide', sans-serif;
      font-size: 2.5rem;
      text-align: center;
      margin: 20px 0;
      color: #fff;
    }
    
    .music-title {
      font-family: 'Audiowide', cursive;
      font-size: 1.5rem;
      text-align: center;
      margin: 20px 0;
      color: #000000;
    }
    
    .music-title p {
      font-size: 1.5rem;
      color: #000000;
      margin-top: 10px;
     font-family: 'Arial', sans-serif;}
    
    
    .container {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
      max-width: 1100px;
      margin: 0 auto;
      padding: 20px;
    }
  
    .video-box {
      background: rgb(12, 49, 3);
      padding: 15px;
      border-radius: 8px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    }
  
    h2 {
      margin: 0 0 10px 0;
      font-size: 1.3rem;
      color: aliceblue;
      font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    }
  
    video {
      width: 100%;
      height: auto;
      border-radius: 4px;
    }

    
  .soundcloud-button {
    background-color: #ff5500;
    color: white;
    border: none;
    padding: 10px 20px;
    font-size: 1rem;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 10px;
  }

  .soundcloud-button:hover {
    background-color: #e64e00;
  }

  
    @media (max-width: 800px) {
      .container {
        grid-template-columns: 1fr;
      }
      
      video {
        height: 300px;
      }
    }
  </style>