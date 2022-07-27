<svelte:head>
  <style>
    @import url("https://fonts.googleapis.com/css2?family=Mulish&display=swap")
  </style>
</svelte:head>

<script>
  import logo from "$lib/pinnie.svg";
  import { ConfettiExplosion } from 'svelte-confetti-explosion'
	import { tick } from 'svelte'
  import { onMount } from 'svelte'
	
  let isVisible = false;
  let isLoaded = false;

  const handleClick = async e => {
		isVisible = false;
		await tick();
    isVisible = true
  }

  onMount(async () => {
    isVisible = false
    await tick()
    isVisible = true
  })
</script> 

<svelte:body on:click={handleClick} />


<div class="container">
  {#if isVisible}
    <ConfettiExplosion colors={['#8000DB', '#580098', '#98005E', '#FF009E', '#FFE001', '#FF9900', '#008298', '#00BEDD' ]} particlesShape="rectangles" force={0.7} />
  {/if}
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
