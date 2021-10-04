<script lang="ts">
  import { Header, Footer, Toolbar, Tab } from "./Components/components.js";
  import { Home, Player, DungeonMaster } from "./Components/Tabs/tabs.js";
  import { selectedTab } from "./Components/store.js"

  const options = {
    tabName: ["Player", "Home", "DungeonMaster"],
    components: [Player, Home, DungeonMaster],
  };
</script>

<div class="app">
  <div class="row">
    <div class="col">
      <Header />
    </div>
  </div>
  <div class="row">
    <div class="col">
      <div class="d-flex justify-content-center">
        <svelte:component
          this={options.components[options.tabName.indexOf($selectedTab)]}
        />
      </div>
    </div>
  </div>
  <Toolbar>
    <Tab tabName="Player">Player</Tab>
    <Tab tabName="Home">Home</Tab>
    <Tab tabName="DungeonMaster">Dungeon Master</Tab>
  </Toolbar>
  <Footer />
</div>
