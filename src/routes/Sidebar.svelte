<script>
    import { fly } from 'svelte/transition';
    export let show = false;
</script>

{#if show}
  <nav transition:fly={{x: 600, opacity: 1}}>
    <button class="text-primary-500" on:click={() => show? show = !show : show}>X</button>
  </nav>
{/if}

		
<style>
nav {
  position: fixed;
  top: 0;
  right: 0;
  height: 100%;
  padding: 2rem 1rem 0.6rem;
  border-left: 1px solid #aaa;
  background: #fff;
  overflow-y: auto;
	width: 600px;
}
</style>