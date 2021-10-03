<script lang="ts">
  import Header from "./Components/Header.svelte";
  import Footer from "./Components/Footer.svelte";
  import Toolbar from "./Components/Toolbar.svelte";
  import Tab from "./Components/Tab.svelte";
</script>

<div class="app">
  <div class="row">
    <div class="col">
      <Header />
    </div>
  </div>
  <div class="row">
    <div class="col">
      <div class="d-flex justify-content-center" id="toolbar-content" />
    </div>
  </div>
  <Toolbar>
    <Tab>Player</Tab>
    <Tab>Home</Tab>
    <Tab>Dungeon Master</Tab>
  </Toolbar>
  <Footer />
</div>
