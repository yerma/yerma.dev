<script>
  /** @type {boolean} */
  export let open = false;
  let active = open;

  /** @param {MouseEvent} event */
	function toggleMenu(event) {
		open = !open;
	}
</script>
<nav class:open>
  <div class="links">
    <a href="">Projects</a>
    <a href="">About</a>
  </div>
  <button on:click={toggleMenu}>
    <span class="material-symbols-sharp">
      {#if open } close {:else } menu {/if }
    </span>
  </button>
</nav>

<style>
  nav {
    --button-size: 36px;
    position: absolute;
    z-index: 10;
    top: 0;
    right: 12px;
    height: 100vh;
    width: calc(100vh + 10px);
    background: var(--cyan);
    color: var(--background);
    padding: 16px 24px;
    
    transform-origin: bottom right;
    transform: rotate(86deg);
    transition: all 400ms cubic-bezier(0.04, 1.33, 0.98, 1);
  }

  nav.open {
    transform: rotate(8deg);
    max-width: 100vw;
  }

  button {
    background: var(--background);
    color: var(--cyan);
    font-family: var(--display-font);
    appearance: none;
    border: none;
    border-radius: 50%;
    width: var(--button-size);
    height: var(--button-size);
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    transform: rotate(-86deg);
    transition: transform 400ms cubic-bezier(0.04, 1.33, 0.98, 1);
  }

  nav.open button {
    transform: rotate(0deg);
  }

  .links {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;;
    gap: 16px;
    height: calc(100% - var(--button-size));
    color: var(--background);
  }

  .links a {
    color: var(--background);
    width: fit-content;
    padding: 8px 16px;
    text-decoration: none;
    transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }

  .links a:hover {
    background: var(--background);
    color: var(--cyan);
  }
</style>