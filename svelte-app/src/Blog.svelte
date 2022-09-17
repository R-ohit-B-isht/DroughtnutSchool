<script>
  import { Router, Route, Link } from "svelte-navigator";

  export let blogRoute;
</script>

<div class="Blog">
  <h2>Blog</h2>

  <span>You're at blog/{blogRoute}</span>

  <nav>
    <Link to="../">Go back to the landing page</Link>
  </nav>

  <p>
    Read about interesting stuff here, like
    <Link to="svelte">Svelte</Link>
    or
    <Link to="navigator">Svlete Navigator</Link>
  </p>

</div>
