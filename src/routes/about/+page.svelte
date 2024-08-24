<script>
  import { slide } from 'svelte/transition';
  import { quintOut } from 'svelte/easing';
</script>

<div class="about">
  <main in:slide={{delay: 250, duration: 300, easing: quintOut, axis: 'x'}}>
    <h1>About</h1>
    <div class="text-block">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus tempor urna felis, at iaculis sem tristique nec. Phasellus imperdiet sodales massa vitae feugiat. Pellentesque dolor lorem, tristique a tellus non, aliquam elementum diam. Proin auctor arcu massa, id elementum orci gravida id. Suspendisse potenti. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Praesent sodales sodales ante at malesuada. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Suspendisse interdum odio vitae felis dictum rhoncus. Cras rhoncus eget lacus at hendrerit. Quisque id tempus ligula. Fusce blandit ex nisl, in pellentesque enim feugiat luctus. Duis malesuada scelerisque sollicitudin. Sed laoreet, elit nec eleifend fringilla, nibh dui eleifend mauris, a imperdiet erat erat tristique ligula. Proin placerat felis quis vehicula lobortis.</p>
      <p>Sed eget feugiat ligula. Sed vitae tempus mauris. Pellentesque nisl orci, vehicula ac laoreet eu, suscipit et purus. Vestibulum aliquet diam metus, non commodo enim sollicitudin eget. Suspendisse at placerat massa, efficitur consequat quam. Proin hendrerit, velit a maximus malesuada, enim tortor posuere diam, at sagittis mauris nunc in erat. Curabitur non turpis dictum nibh fermentum euismod. Phasellus sapien ex, faucibus vitae consectetur nec, commodo sed risus. Quisque eget molestie libero, dictum pellentesque ante. Nulla maximus nibh libero, in ornare massa tempor ut. Etiam iaculis tempor nisl vel pellentesque. Phasellus ultrices, orci eget imperdiet faucibus, massa lorem condimentum risus, sed dignissim lorem turpis eget eros. Etiam at leo ante.</p>
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
