<script>
    import { Router, Route, Link } from "svelte-navigator";
    import Blog from "./Blog.svelte";
  </script>
  
  <Router>
    <header>
      <h1>My site</h1>
  
      <nav>
        <Link to="/">Home</Link>
        <Link to="about">About</Link>
        <Link to="blog">Blog</Link>
      </nav>
    </header>
  
    <main>
      <Route path="blog/*blogRoute" component={Blog} />
  
      <Route path="/">
        <h3>Home</h3>
        <p>Home sweet home...</p>
              <p>
                  Check out the <Link to="/about#digital">digital heading</Link>, a heading with an <code>id </code> of “digital”
              </p>
      </Route>
  
      <Route path="about">
        <h3>About</h3>
              <p>
                  This page has a header with an  <code>id</code> of “digital” that we're trying to link to.
              </p>
                          <p>
                  Check out the <Link to="/about#digital">digital heading</Link>
              </p>
  
        <p>That's what it's all about!</p>
              <p>
                  Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.
              </p>
              <p>
  Bring to the table win-win survival strategies to ensure proactive domination. At the end of the day, going forward, a new normal that has evolved from generation X is on the runway heading towards a streamlined cloud solution. User generated content in real-time will have multiple touchpoints for offshoring.</p>
              <p>
                  Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.
              </p>
              <p>
  Bring to the table win-win survival strategies to ensure proactive domination. At the end of the day, going forward, a new normal that has evolved from generation X is on the runway heading towards a streamlined cloud solution. User generated content in real-time will have multiple touchpoints for offshoring.</p>
              <p>
                  Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.
              </p>
              <p>
  Bring to the table win-win survival strategies to ensure proactive domination. At the end of the day, going forward, a new normal that has evolved from generation X is on the runway heading towards a streamlined cloud solution. User generated content in real-time will have multiple touchpoints for offshoring.</p>
              <p>
                  Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to corporate strategy foster collaborative thinking to further the overall value proposition. Organically grow the holistic world view of disruptive innovation via workplace diversity and empowerment.
              </p>
              <p>
  Bring to the table win-win survival strategies to ensure proactive domination. At the end of the day, going forward, a new normal that has evolved from generation X is on the runway heading towards a streamlined cloud solution. User generated content in real-time will have multiple touchpoints for offshoring.</p>
  <h4 id="digital">
      Digital 
              </h4>
  <p>Capitalize on low hanging fruit to identify a ballpark value added activity to beta test. Override the digital divide with additional clickthroughs from DevOps. Nanotechnology immersion along the information highway will close the loop on focusing solely on the bottom line.
              </p>
      </Route>
  
      <Route>
        <h3>Default</h3>
        <p>No Route could be matched.</p>
      </Route>
    </main>
  </Router>
  
  <style>
      :global(:target) {
  
      background-color: papayawhip;}
  </style>
  