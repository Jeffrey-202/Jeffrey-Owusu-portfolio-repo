<script>
    import Header from '$lib/components/Header.svelte';
    import Footer from '$lib/components/Footer.svelte';
  </script>
  
  <div class="page-wrapper">
    <Header />
    <main>
      <slot /> <!-- Your page content injects here -->
    </main>
    <Footer />
  </div>
  
  <style>
    :global(body) {
      margin: 0;
      min-height: 100vh; /* Full viewport height */
    }
  
    .page-wrapper {
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }
  
    main {
      flex: 1; /* Pushes footer down */
    }
  
    
    

  
  
   </style>