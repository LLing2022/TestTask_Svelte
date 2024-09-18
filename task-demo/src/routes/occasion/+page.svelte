<script>
    import OccasionButton from '../../components/OccasionButton.svelte';
  
    let selectedOccasion = '';
    let occasions = [
      { name: 'Wedding', icon: '💍' },
      { name: 'Corporate Event', icon: '📁' },
      { name: 'Birthday', icon: '🎂' },
      { name: 'Dinner Party', icon: '🍽' },
      { name: 'Celebration', icon: '🎉' },
      { name: 'Public Event', icon: '🗺' },
    ];
  
    function handleSelect(occasion) {
      selectedOccasion = occasion.name;
    }
  
    function handleNext() {
      if (selectedOccasion) {
        alert(`Proceeding with ${selectedOccasion}`);
      } else {
        alert('Please select an occasion.');
      }
    }
  
    function handleBack() {
      window.history.back(); 
    }
  </script>
  
  <div class="occasion-page">
    <h1>What’s the occasion?</h1>
  
    <div class="occasion-buttons">
      {#each occasions as occasion}
        <OccasionButton 
          text={occasion.icon + ' ' + occasion.name}
          selected={selectedOccasion === occasion.name}
          onClick={() => handleSelect(occasion)}
        />
      {/each}
    </div>
  
    <div class="buttons">
      <OccasionButton text="Back" onClick={handleBack} type="secondary" />
      <OccasionButton text="Next" onClick={handleNext} type="primary" />
    </div>
  </div>
  
  <style>
    .occasion-page {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      padding: 20px;
      min-height: 100vh;
      background-color: #d0eded;
    }
  
    h1 {
      font-size: 44px;
      margin-bottom: 20px;
    }
  
    .occasion-buttons {
      display: flex;
      flex-direction: column;
      gap: 10px;
      width: 100%;
      max-width: 400px;
    }
  
    .buttons {
      margin-top: 20px;
      display: flex;
      justify-content: space-between;
      width: 100%;
      max-width: 400px;
    }
  </style>
  