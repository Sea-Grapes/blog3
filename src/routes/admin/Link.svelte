<script>
export let icon;
export let url;
export let display;

import { page } from '$app/stores';
let path;

$: path = $page.url.pathname;
// console.log(path)

</script>


<a class:active={path.includes(url)} href={url}><span class="material-symbols-rounded">{icon}</span>{display}</a>

<style>
  a {
    padding: 0 2rem;
    margin-bottom: 0.7rem;
    display: flex;
  }

  .active {
    color: var(--amber-500) !important;
  }

  a span {
    margin-right: 0.5em;
  }
</style>