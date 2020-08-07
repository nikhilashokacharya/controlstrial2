<template>
  <div class="scroll-content">
    <div class="scroll-inner"></div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.scroll-content {
    /* position: absolute; */
  border: none;
  height: 380px;
  width: 120px;
  overflow-y: scroll;
  
}
.scroll-inner {
  width: fit-content;
  height: calc(100% + 100px);
  scrollbar-width: none;
}
/* ::-webkit-scrollbar{
    width: 50px;
    height:100px;
}
::-webkit-scrollbar-button{
    background-color: #ccc;
}
::-webkit-scrollbar-track-piece {
    background: #888;
}
::-webkit-scroll-thumb{
    background:#eee;
} */

</style>