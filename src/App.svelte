<script lang="ts">
  import { onMount } from 'svelte';
  import { World } from '../threejs/World';

  let wrapper: HTMLElement;

  onMount(async () => {
    const world = new World(wrapper);
    world.start();
  });
</script>

<div id="app">
  <h1>Night scene</h1>
  <div id="scene-container" bind:this={wrapper} />
</div>

<style>
  #scene-container {
    height: 80vh;
  }
</style>
