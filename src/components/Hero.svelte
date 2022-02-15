<script>
  import { fade, fly } from 'svelte/transition'
  import { onMount } from 'svelte'
  //state
  let name = ''
  let isloading = true

  onMount(() => {
    isloading = false
  })
</script>

<section >
  {#if !isloading}
  <input transition:fly="{{ x: -400, duration: 1000 }}" type="text" bind:value={name} placeholder="Enter your name">
  {/if}
	<h1  class="title">Hello {name || 'world'}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
  {#if name}
  <p transition:fade class="secret">Svelte is fun and simple</p>
  {/if}
</section>

<style>
	section {
		text-align: center;
		padding: 1em;
		max-width: fit-content;
		margin: 0 auto;
	}

	.title {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

  .secret {
    font-size: 2rem;
  }

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
	
</style>