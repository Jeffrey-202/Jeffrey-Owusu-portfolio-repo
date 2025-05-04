<script>
  import { onMount } from 'svelte';
  
  onMount(() => {
      console.log("Home Page Loaded");
  });
</script>


  <title>Jeffrey Owusu - Homepage</title>
  <meta name="description" content="Welcome to Jeffrey Owusu's personal website" />
  <link href="https://fonts.googleapis.com/css2?family=Audiowide&display=swap" rel="stylesheet">


<main>
  <h1>Jeffrey Owusu</h1>
  <h2>Welcome</h2>
 
  
  <div class="image-container">
      <img src="girl.jpg" alt="Artistic work by Jeffrey" class="girl-image"/>
      <img src="thelad.jpg" alt="Jeffrey's portrait" class="lad-image"/>
      <img src="foodrush.jpg" alt="Food Rush project" class="foodrush-image"/>
  </div>
</main>

<style>
  @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
  }
  
  @keyframes slideInFromTop {
      from { transform: translateY(-100px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
  }
  
  @keyframes slideInFromBottom {
      from { transform: translateY(100px); opacity: 0; }
      to { transform: translateY(0); opacity: 1; }
  }
  
  @keyframes pulse {
      0% { transform: scale(1); }
      50% { transform: scale(1.05); }
      100% { transform: scale(1); }
  }
  
  @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-20px); }
      100% { transform: translateY(0px); }
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
  line-height: 1.6;
}

  
  main {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 2rem;
      min-height: 100vh;
  }
  
  h1 {
      font-size: 6.5rem;
      color: #000000;
      margin-bottom: 1rem;
      font-family: "Audiowide", sans-serif;
      font-weight: 600;
      padding: 20px;
      text-align: center;
      animation: slideInFromTop 1s ease-out, pulse 3s infinite;
      text-shadow: 3px 3px 0px rgba(0,0,0,0.2);
  }
  
  h2 {
      font-size: 3rem;
      color: #000000;
      margin-bottom: 1.5rem;
      font-weight: 600;
      text-align: center;
      animation: slideInFromBottom 1s ease-out;
  }
  
  p {
      font-size: 2rem;
      color: #000000;
      margin-bottom: 3rem;
      font-weight: 600;
      text-align: center;
      animation: fadeIn 1.5s ease-out;
  }
  
  .image-container {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
      gap: 50px;
      margin-top: 2rem;
      width: 100%;
  }
  
  .girl-image, .lad-image, .foodrush-image {
      border-radius: 20px;
      transition: all 0.3s ease;
      box-shadow: 0 5px 15px rgba(0,0,0,0.1);
  }
  
  .girl-image {
      width: 500px;
      max-width: 100%;
      animation: float 4s ease-in-out infinite;
  }
  
  .lad-image {
      width: 600px;
      max-width: 100%;
      animation: float 4s ease-in-out infinite 1s;
  }
  
  .foodrush-image {
      width: 500px;
      max-width: 100%;
      animation: float 4s ease-in-out infinite 0.5s;
  }
  
  .girl-image:hover {
      transform: scale(1.05) rotate(2deg);
      box-shadow: 0 10px 20px rgba(0,0,0,0.3);
  }
  
  .lad-image:hover {
      transform: scale(1.05);
      box-shadow: 0 10px 20px rgba(0,0,0,0.3);
      filter: brightness(1.05);
  }
  
  .foodrush-image:hover {
      transform: scale(1.05) rotate(-2deg);
      box-shadow: 0 10px 20px rgba(0,0,0,0.3);
  }
  
  @media (max-width: 1200px) {
      h1 {
          font-size: 4.5rem;
      }
  }
  
  @media (max-width: 768px) {
      h1 {
          font-size: 3rem;
          padding: 10px;
      }
      
      h2 {
          font-size: 2rem;
      }
      
      p {
          font-size: 1.5rem;
          margin-bottom: 2rem;
      }
      
      .image-container {
          gap: 30px;
      }
  }
  
  @media (max-width: 480px) {
      h1 {
          font-size: 2.5rem;
      }
      
      h2 {
          font-size: 1.5rem;
      }
      
      p {
          font-size: 1.2rem;
      }
  }
</style>