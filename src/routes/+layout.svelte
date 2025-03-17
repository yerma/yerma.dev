export const prerender = true;

<script>
  import '../global.css';
  import Menu from "$lib/components/Menu.svelte";
</script>
<slot></slot>
<Menu />
