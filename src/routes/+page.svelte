<script>
  import { slide } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';
</script>

<div class="home">
  <main in:slide={{delay: 250, duration: 300, easing: quintOut, axis: 'x'}}>
    <h1>yerma<span>.dev</span></h1>
  </main>
</div>

<style>
  .home main {
    padding: 36px 48px;
    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    text-align: center;
    color: white;
    z-index: 1;
  }

  h1 {
    font-size: 3em;
    text-align: left;
    margin: 0;
    color: var(--cyan);
  }

  h1 span {
    opacity: 0.6;
    font-weight: 300;
  }
</style>