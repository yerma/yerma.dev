<script>
  import { slide } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';
</script>

<svelte:head>
  <title>yerma.dev | about</title>
</svelte:head>

<div class="about">
  <main in:slide={{delay: 250, duration: 300, easing: quintOut, axis: 'x'}}>
    <h1>About me</h1>
    <div class="text-block">
      <p>I'm <em>currently</em> a web developer based in Chile.</p>
      <p>I'm also a school teacher and graphic designer. Dedicated almost exclusively to web development since 2016, I'm always eager to integrate this diverse range of interests and abilities into any project.</p>
      <p>English · Español · Português</p>
    </div>
  </main>
</div>

<style>
  .about main {
    padding: 36px 48px;
  }

  @media (max-width: 640px) {
    .about main {
      padding: 24px;
    }
  }

  .text-block {
    margin-left: 20px;
    padding-left: 20px;
    border-left: 2px solid var(--cyan);
    max-width: 74vw;
    width: 640px;
  } 
</style>
