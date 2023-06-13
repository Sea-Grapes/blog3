<script>
  export let url = '';
  export let label = 'unknown';

  import { page } from '$app/stores';
  let path;

  $: path = $page.url.pathname;
</script>

<a class:active={path === url} href={url}>{label}</a>

<style>

a {
  display: block;
}

a:hover {
  background-color: var(--slate-50);
}

.active {
  color: var(--blue-500);
  /* font-weight: 600; */
  border-bottom: 3px solid var(--blue-500);
  background-color: var(--blue-50) !important;
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