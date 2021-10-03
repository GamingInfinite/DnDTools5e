<script>
</script>

<div id="toolbar">
  <div class="row">
    <slot />
  </div>
</div>

<style>
  #toolbar {
    position: absolute;
    width: 100%;
    border-top: 4px solid rgb(133, 0, 0);
    bottom: 0;
    left: 0;
    z-index: 200;
    transform: translate3d(0, 0, 0);
    background-color: rgb(43, 51, 59);
  }
</style>
