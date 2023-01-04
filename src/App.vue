<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style lang="scss">
#app {
  height: 100vh;
  width: 100vw;
}
::-webkit-scrollbar {
  /*滚动条整体*/
  width: 5px;
}
::-webkit-scrollbar-track {
  /*滑轨*/
  background-color: transparent;
}
::-webkit-scrollbar-thumb {
  /*滑块*/
  background-color: #000;
}
::-webkit-scrollbar-thumb:hover {
  cursor: pointer;
  background-color: #aaa;
}
</style>
