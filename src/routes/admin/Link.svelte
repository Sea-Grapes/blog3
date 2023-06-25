<script>
export let icon;
export let url;
export let display;

import { page } from '$app/stores';
let path;

$: path = $page.url.pathname;
// console.log(path)

</script>


<a class:active={path.endsWith(url)} href={url}><span class="material-symbols-rounded">{icon}</span>{display}</a>

<style>

  span {
    color: var(--zinc-400)
  }

  a {
    padding: 0 2rem;
    margin-bottom: 0.7rem;
    display: flex;
    align-items: center;
    border: 2px solid transparent;
    transition: color 0.2s;
    color: var(--zinc-600)
  }

  .active {
    color: var(--amber-500) !important;
    border-left: 2px solid var(--amber-500);
  }

  .active span {
    color: var(--amber-500) !important;
  }

  a span {
    margin-right: 0.5em;
  }
</style>