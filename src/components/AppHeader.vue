<script>
export default {
  data() {
     return {
        
     }
  }
}
</script>

<template>
<header>
  <nav>
    <div class="logo">
      <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg/1200px-Yu-Gi-Oh%21_%28Logo%29.jpg" alt="">
    </div>
    <h1>Yu-Gi-Oh Api</h1>
  </nav>
</header>
  
</template>

<style lang="scss">
@use '../styles/general.scss';

nav{
  padding: 1rem;
  display: flex;
  align-items: center;


  .logo {
    max-width: 100px;
  
    img {
      width: 100%;
    }
  }

  h1 {
    font-size: 50px;
    font-weight: lighter;
    margin-left: 2rem;
  }
}

</style>
