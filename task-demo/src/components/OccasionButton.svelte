<script>
    export let text = 'Occasion';
    export let selected = false;  
    export let onClick = () => {};
  </script>
  
  <button class="occasion-button {selected ? 'selected' : ''}" on:click={onClick}>
    {text}
  </button>
  
  <style>
    .occasion-button {
      padding: 10px 20px;
      font-size: 18px;
      border: none;
      border-radius: 15px;
      cursor: pointer;
      background-color: white;
      color: black;
      width: 100%;
      text-align: left;
      display: flex;
      align-items: center;
      transition: background-color 0.3s, color 0.3s;
    }
  
    .occasion-button:hover {
      background-color: #f0f0f0; 
    }
  
    
    .selected {
      background-color: #00A99D;
      color: white;
    }
  
    
    .occasion-button span {
      margin-right: 10px; 
    }
  </style>
  