<script lang="ts">
  import { slide } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';
  import works from "./works.json";

  let selectedIndex: number | null = null;
</script>

<svelte:head>
  <title>yerma.dev | works</title>
</svelte:head>

<div class="works">
  <main in:slide={{delay: 250, duration: 300, easing: quintOut, axis: 'x'}}>
    <h1>Works</h1>
    <div class="work-grid" class:work-selected={selectedIndex !== null}>
      {#each works as work, i}
        <div class="work-item"
          role="contentinfo"
          class:active={selectedIndex === i}
          on:mouseenter={() => selectedIndex = i}>
          <figure>
            <img src={`/img/${work.imgUrl}`} alt={work.title} />
          </figure>
        </div>
      {/each}
    </div>
    {#if selectedIndex !== null}
      <div class="work-details">
        <h2>{works[selectedIndex].title}</h2>
        <div class="text-block">
          <p >{works[selectedIndex].description}</p>
          {#if works[selectedIndex].url}
            <a href={works[selectedIndex].url} target="_blank">
              View project
              <span class="material-symbols-sharp">
                open_in_new
              </span>
            </a>
          {/if}
        </div>
      </div>
    {/if}
  </main>
</div>

<style>
  .works main {
    padding: 36px 48px;
  }

  @media (max-width: 640px) {
    .works main {
      padding: 24px;
    }
  }

  .work-grid {
    margin: 64px 48px;
    display: flex;
    min-height: 30vh;
    gap: 8px;
  }

  .work-item {
    clip-path: polygon(25% 0%, 100% 0%, 75% 100%, 0% 100%);
    margin: 0 -3.5%;
    flex-basis: 50%;
    cursor: pointer;
    opacity: 1;
    transition: opacity 200ms ease-in-out;
  }

  .work-grid figure {
    height: 100%;
    width: 100%;
    margin: 0;
  }

  .work-grid figure img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .work-selected .work-item:not(.active) {
    opacity: 0.3;
  }

  .text-block {
    margin-top: 24px;
    margin-left: 20px;
    padding-left: 20px;
    border-left: 2px solid var(--cyan);
    max-width: 74vw;
    width: 640px;
  }

  .work-details a {
    display: flex;
    gap: 4px;
    align-items: center;
    margin-top: 16px;
    text-decoration: none;
    cursor: pointer;
  }

</style>
