<div class="base">
  <div class="left">
    <header>Logo</header>
    <a href="dashboard"><span class="material-symbols-rounded">grid_view</span>Dashboard</a>
    <a href="blog"><span class="material-symbols-rounded">article</span>Blog</a>
    <a href="projects"><span class="material-symbols-rounded">folder</span>Projects</a>
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
  
  header {
    padding: 1.2rem 2rem;
    border-bottom: 1px solid var(--slate-200);
    margin-bottom: 1.2rem;
  }

  .left {
    background-color: var(--slate-50);
  }

  .body {
    padding: 0 2rem;
  }

  a {
    padding: 0 2rem;
    margin-bottom: 0.6em;
    display: flex;
  }

  a span {
    margin-right: 0.5em;
  }

  .base:last-child {

  }
</style>