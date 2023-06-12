<script>
  export let url = '';
  export let label = 'unknown';

  import { page } from '$app/stores';
  let path;

  $: path = $page.url.pathname;
</script>

<a class:active={path = url} href={url}>{label}</a>

<style>

a {
  display: block;
}

.active {
  background-color: grey;
}

@media screen and (min-width: 800px) {
  a {
    display: flex;
    padding: 0 1rem;
    height: 100%;
    align-items: center;
  }
}

</style>