<script>
    export let occasions = [];
    export let selectedOccasion = '';
    export let onSelect = (occasion) => {};
  </script>
  
  <div class="occasion-selector">
    {#each occasions as occasion}
      <div 
        class="occasion-item {selectedOccasion === occasion.name ? 'selected' : ''}" 
        on:click={() => onSelect(occasion)}>
        {occasion.icon} {occasion.name}
      </div>
    {/each}
  </div>
  
  <style>
    .occasion-selector {
      width: 100%;
      border: 1px solid #ddd;
      border-radius: 5px;
      overflow: hidden;
    }
  
    .occasion-item {
      padding: 10px;
      font-size: 18px;
      display: flex;
      align-items: center;
      cursor: pointer;
      background-color: white;
      transition: background-color 0.3s;
    }
  
    .occasion-item.selected {
      background-color: #00A99D; 
      color: white;
    }
  
    .occasion-item + .occasion-item {
      border-top: 1px solid #ddd;
    }
  </style>
  