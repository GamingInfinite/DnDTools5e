<script>
  import { selectedTab } from "./store.js";

  let tabClass;

  const ClassSelector = selectedTab.subscribe((value) => {
    tabClass = value;
  });
</script>

<div id="toolbar">
  <div class="row">
    <slot />
  </div>
  <img
    src="./images/crossed_swords.png"
    alt="crossed swords"
    class="indicator {tabClass}"
  />
</div>

<style>
  #toolbar {
    position: fixed;
    width: 100%;
    border-top: 4px solid rgb(133, 0, 0);
    bottom: 0;
    left: 0;
    z-index: 200;
    transform: translate3d(0, 0, 0);
    background-color: rgb(43, 51, 59);
  }

  .indicator {
    position: absolute;
    top: 10px;
    opacity: 0.5;
    height: 30px;
    width: auto;
    transition: left 0.2s;
  }

  .indicator.Home {
    left: 48.9%;
  }

  .indicator.Player {
    left: 15.1%;
  }

  .indicator.DungeonMaster {
    left: 82.8%;
  }
</style>
