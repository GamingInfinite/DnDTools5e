<script>
  import { selectedTab } from "./store.js";

  export let tabName;

  function update() {
      selectedTab.set(tabName)
  }
</script>

<div class="col">
  <div class="d-flex justify-content-center align-items-center" id="tab" on:click={update}>
    <slot />
  </div>
</div>

<style>
  #tab {
    height: 50px;
    opacity: 1;
    -webkit-transition: opacity .2s;
  }

  #tab:hover {
    opacity: .2;
  }
</style>
