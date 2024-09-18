<script>
    export let src = '';
    export let alt = '';
  </script>
  
  <div class="image-field">
    <img src={src} alt={alt} class="profile-image" />
  </div>
  
  <style>
    .image-field {
      text-align: center;
      margin-top: 20px;
    }
  
    .profile-image {
      width: 70px;
      height: 70px;
      border-radius: 30%;
      object-fit: cover;
    }

    @media (max-width: 600px) { 
    .profile-image {
      width: 50px; 
      height: 50px;
    }
  }
  </style>
  