
<script>
</script>

<header>
  <input type="checkbox" id="nav-toggle">
  <cs>
  <label for="nav-toggle"><span class="material-symbols-rounded">menu</span></label>
    Portfolio();
  </cs>
  <nav>
    <a href="#">Home</a>
    <a href="#">Blog</a>
    <a href="#">Projects</a>
    <a href="#">About</a>
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
  margin-bottom: 0.5rem;
  place-items: center;
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
  padding: 2rem;
}

nav {
  text-align: left;
  /* display: grid; */
  transform: scale(1, 0);
  transform-origin: top;
  transition: transform 400ms ease-in-out;
}

nav a {
  margin-right: 1rem;
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
  }

  nav {
    transition: none;
    transform: scale(1, 1);
  }

  nav a {
    display: inline;
  }

  label[for='nav-toggle'] {
    display: none;
  }
}

</style>