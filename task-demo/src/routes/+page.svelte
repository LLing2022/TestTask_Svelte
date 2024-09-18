<script>
    import { goto } from '$app/navigation';
    import Button from '../components/Button.svelte'; 
    import ImageField from '../components/ImageField.svelte'; 
    
  
    function handleLetsGoClick() {
      goto('/occasion'); 
    }
  </script>
  
  <div class="main-container">
    <ImageField src="images/image.png" alt="Concierge Photo" />
  
    <p>👋 Hi I’m <strong>Evelyne</strong>, I will be your concierge today.<br />
    Give me more information about your event and...</p>
  
    <h1>Let’s get you the best quotes</h1>
  
    <p class="subheading">You are just a few questions away from the event of the year. Let’s get started.</p>
  
    <Button text="LET'S GO" onClick={handleLetsGoClick} />
  </div>
  
  <style>
    :global(html, body) {
    margin: 0;
    padding: 0;
    height: 100%;
     background-color:#d0eded;
  }
    .main-container {
      text-align: center;
      padding: 20px;
      background-color: #d0eded;
      min-height: 50vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }
  
  
    h1 {
      font-size: 32px;
      font-weight: bold;
      margin-bottom: 20px;
    }
  
    .subheading {
      font-size: 18px;
      color: #666;
      margin-bottom: 40px;
      font-style: italic;
    }
  </style>
  



<!-- <script>
    import Button from '../components/Button.svelte';
    import ImageField from '../components/ImageField.svelte';
  
    function handleButtonClick() {
      alert('Button clicked!');
    }
  </script>
  
  <div class="main-container">
    <ImageField src="images/image.png" alt="Concierge Photo" />
  
    <p>👋 Hi I’m <strong>Evelyne</strong>, I will be your concierge today.<br />
    Give me more information about your event and...</p>
  
    <h1>Let’s get you the best quotes</h1>
  
    <p class="subheading">You are just a few questions away from the event of the year. Let’s get started.</p>
  
    <Button text="LET'S GO" onClick={handleButtonClick} />
  </div>
  
  <style>
    :global(html, body) {
    margin: 0;
    padding: 0;
    height: 100%;
     background-color:#EDF2F2;
  }

    .main-container {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      min-height: 70vh; 
      background-color: inherit; 
      padding: 0;
      
    }
  
    h1 {
      font-size: 32px;
      font-weight: bold;
      margin-bottom: 20px;
    }
  
    .subheading {
      font-size: 18px;
      color: #666;
      margin-bottom: 40px;
      font-style: italic;
    }

    @media (max-width: 600px) {
    h1 {
      font-size: 24px; /* Reduce font size for smaller screens */
    }

    .subheading {
      font-size: 16px; /* Adjust subheading size */
      margin-bottom: 20px;
    }

    .main-container {
      padding: 0 10px; /* Reduce padding on smaller screens */
    }
  }
  </style>
  
 -->
