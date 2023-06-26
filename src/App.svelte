<script>
  import { Route, Router, Link } from "svelte-routing";
  import Home from "./components/Home.svelte";
  import Meaning from "./components/Meaning.svelte";
</script>

<Router>
  <main class="app">
    <nav>
      <Link to="/">Home</Link>
    </nav>
    <Route path="/" component={Home} />

    <Route path="/find/:word" let:params>
      <Meaning word={params.word} />
    </Route>
  </main>
</Router>