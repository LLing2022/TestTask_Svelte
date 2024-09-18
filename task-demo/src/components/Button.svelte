<script>
    export let text = 'Click me';
    export let onClick = () => {};
  </script>
  
  <button on:click={onClick} class="button">
    {text}
  </button>
  
  <style>
    .button {
      background-color: #00A99D; 
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 15px;
      font-size: 16px;
      cursor: pointer;
    }
  </style>
  