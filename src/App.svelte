<script>
  import Title from "./Title.svelte";
  import Nav from "./Nav.svelte";
  import Kancelaria from "./Kancelaria.svelte";
  import Specjalizacje from "./Specjalizacje.svelte";
  import Kontakt from "./Kontakt.svelte";

</script>

<style>
  main {
    overflow-x: hidden;
  }
</style>

<main>
  <Nav class="nav-component" />
  <Title class="title-component" />
  <Kancelaria class="kancelaria-component" />
  <Specjalizacje />
  <Kontakt />
</main>

