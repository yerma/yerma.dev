<script>
  import { slide } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';
</script>

<div class="home">
  <main in:slide={{delay: 250, duration: 300, easing: quintOut, axis: 'y'}}>
    <h1>yerma<span>.dev</span></h1>
    <nav>
      <a href="/works">Works</a>
      <a href="/about">About</a>
    </nav>
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
    align-items: center;
    justify-content: center;
    text-align: center;
    color: white;
    z-index: 1;
  }

  h1 {
    font-size: clamp(3rem, 8vw, 6rem);
    margin: 0;
    color: var(--cyan);
  }

  h1 span {
    opacity: 0.6;
    font-weight: 300;
  }

  .home nav {
    margin-top: 20px;
    padding: 12px 0 0;
    border-top: 1px solid rgba(255, 255, 255, 0.2);
    display: flex;
    gap: 32px;
    justify-content: center;
  }

  .home nav a {
    color: rgba(255, 255, 255, 0.3);
    text-decoration: none;
    font-size: 1.5rem;
    font-weight: 300;
    padding: 8px 24px;
    border-radius: 4px;
    transition: all 200ms;
    letter-spacing: 0.3rem;
  }

  .home nav a:hover {
    font-weight: 500;
    color: rgba(255, 255, 255, 1);
  }

  .home nav:hover {
    padding: 12px 40px 0;
  }

  .home nav:hover a {
    letter-spacing: 0.6rem;
  }
</style>