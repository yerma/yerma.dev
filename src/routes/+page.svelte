<div class="home video-background">
  <video autoplay muted loop playsinline>
    <source src="/noise.webm" type="video/webm">
  </video>

  <main>
    <h1>yerma<span>.dev</span></h1>
  </main>
</div>

<style>
  .video-background {
    position: relative;
    width: 100vw;
    height: 100vh;
    overflow: hidden;
    background: var(--cyan);
  }

  .video-background video {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    overflow: hidden;
    min-width: 100%;
    min-height: 100%;
    mix-blend-mode: luminosity;
    opacity: 0.98;
  }

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
    color: rgba(48, 242, 223, 0.4);
  }

  h1 span {
    opacity: 0.6;
    font-weight: 300;
  }
</style>