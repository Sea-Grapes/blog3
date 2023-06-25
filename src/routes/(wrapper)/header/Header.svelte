
<script>
import Nav from "./Nav.svelte";
</script>

<header class="ns">
  <input type="checkbox" id="nav-toggle">
  <cs>
  <label for="nav-toggle"><span class="material-symbols-rounded">menu</span></label>
    <a href="/">Portfolio();</a>
  </cs>
  <nav>
    <Nav url='/' label='Home'/>
    <Nav url='/blog' label='Blog'/>
    <Nav url='/projects' label='Projects'/>
    <Nav url='/about' label='About'/>
  </nav>
</header>



<style>

cs {
  font-family: Consolas;
}

header cs {
  display: grid;
  place-items: center;
  height: 4rem;
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
  
  label[for='nav-toggle'] {
    display: none;
  }
}

</style>