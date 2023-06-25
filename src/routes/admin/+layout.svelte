<script>
    import Link from "./Link.svelte";

</script>
<div class="base">
  <div class="left">
    <header>Logo</header>
    <Link url='dashboard' icon='grid_view' display='Dashboard'/>
    <Link url='blog' icon='article' display='Blog'/>
    <Link url='projects' icon='folder' display='Projects'/>
    <Link url='comments' icon='comment' display='Comments'/>

    <Link url='/' icon='home' display='Home'/>

  </div>
  <div>
    <header>Banner thing</header>
    <div class="body">
      <slot/>
    </div>
  </div>
</div>

<style>
  .base {
    display: grid;
    grid-template-columns: 12rem auto;
    min-height: 100vh;
  }
  
  .body {
    padding: 0 2rem;
  }
  
  header {
    padding: 1.2rem 2rem;
    border-bottom: 1px solid var(--slate-200);
    margin-bottom: 2rem;
  }

  .left {
    background-color: var(--slate-50);
  }

</style>