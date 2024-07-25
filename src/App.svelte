<script lang="ts">
  import { Router, Route } from "svelte-routing";
  import home from "./main.svelte";
  import contact from "./contact.svelte";
  import about from "./about.svelte";
  import first from "./first.svelte"
  import adarsh from "./adarsh.svelte"
  import aji from "./AJI.svelte"
  import prasanth from "./prasanth.svelte"
  import praveen from "./praveen.svelte"
  import project from "./projects.svelte"
  import Aji from "./AJI.svelte";
</script>

<Router>
    <Route path="/" component={home} />
    <Route path="/Home" component={first} />
  <Route path="/About" component={about} />
  <Route path="/Projects" component={project} />
  <Route path="/Contact" component={contact} />
  <Route path="/PRASANTH" component={prasanth} />
  <Route path="/AJI" component={aji} />
  <Route path="/Adarsh" component={adarsh} />
  <Route path="/PRAVEEN" component={praveen} />
</Router>
