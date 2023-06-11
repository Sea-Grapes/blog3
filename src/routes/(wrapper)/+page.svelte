
<script>
</script>

<header>
  <cs>Portfolio();</cs>
  <input type="checkbox" id="nav-toggle">
  <label for="nav-toggle"></label>
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
  display: block;
  text-align: center;
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


#nav-toggle:checked ~ nav {
  transform: scale(1, 1);
}

#nav-toggle + label {
  background-image: url('logo.svg');
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

  #nav-toggle {
    display: none;
  }
}

</style>