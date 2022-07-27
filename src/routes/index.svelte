<svelte:head>
  <style>
    @import url("https://fonts.googleapis.com/css2?family=Mulish&display=swap")
  </style>
</svelte:head>

<script>
  import logo from "$lib/pinnie.svg";
</script> 

<div class="container">
  <img src={logo} alt="Pinata Logo" />
  <h1>No</h1>
</div>

<style>

  .container {
    height: 100vh;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
  }  

  h1 {
    font-family: "Mulish", sans-serif;
    font-size: 90px;
    font-weight: bold;
  }

</style>
