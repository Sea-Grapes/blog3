
<script>
    import Nav from "./header/Nav.svelte";

</script>

<header class="ns">
  <input type="checkbox" id="nav-toggle">
  <cs>
  <label for="nav-toggle"><span class="material-symbols-rounded">menu</span></label>
    Portfolio();
  </cs>
  <nav>
    <Nav url='/' label='Home'/>
    <Nav url='/' label='Blog'/>
    <Nav url='/' label='Projects'/>
    <Nav url='/' label='About'/>

    
    
    <!-- <a href="#">Home</a>
    <a href="#">Blog</a>
    <a href="#">Projects</a>
    <a href="#">About</a> -->
  </nav>
</header>
<main>
  <section>
    <div class="container">
      Hello this is a test
    </div>
  </section>
</main>



<style>

input {

}

cs {
  font-family: Consolas;
}

header cs {
  display: grid;
  place-items: center;
  height: 4rem;
}

.container {
  max-width: 50rem;
  margin: 0 auto;
  padding: 0 2rem;
}

section {
  padding: 3.5rem 0;
}

header {
  padding: 0 2rem;
}

nav {
  text-align: left;
  transform: scale(1, 0);
  transform-origin: top;
  transition: transform 400ms ease-in-out;
}

nav a {
  display: block;
}


#nav-toggle {
  display: none;
}


#nav-toggle:checked ~ nav {
  transform: scale(1, 1);
}

label[for='nav-toggle'] {
  display: flex;
  position: absolute;
  left: 2rem;
  font-size: 2em;
}

@media screen and (min-width: 800px) {
  cs {
    display: inline;
  }

  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 4rem;
  }

  nav {
    transition: none;
    transform: scale(1, 1);
    display: flex;
    align-items: center;
    height: 100%;
  }

  nav a {
    display: flex;
    padding: 0 1rem;
    height: 100%;
    align-items: center;
  }

  label[for='nav-toggle'] {
    display: none;
  }
}

</style>