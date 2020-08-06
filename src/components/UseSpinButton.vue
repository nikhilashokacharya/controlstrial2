<template>
   <div class="outer-spin">
  <!--  <div></div> -->
    <div class="inner-buttons">
      <button class="buttons">
        <div class="triangle-up"></div>
      </button>
      <button class="buttons">
        <div class="triangle-down"></div>
      </button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
/* .outer-spin {
  display: grid;
  grid-template-columns: 85% 15%;
  border: 1px solid gray;
  height: 30px;
  width: 150px;
} */
.outer-spin {
    height: 40px;
  width: 50px;
}
.inner-buttons {
  display: grid;
  grid-template-columns: 1fr;
}
.buttons {
  border: none;
  background: white;
  margin-right: 1px;
  margin-top:1px;
  /* height: 13px; */
}
.triangle-up {
  width: 0;
  height: 0;
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-bottom: 5px solid black;
}
.triangle-down {
  width: 0;
  height: 0;
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: 5px solid black;
}
</style>