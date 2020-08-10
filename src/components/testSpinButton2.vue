<template>
  <div class="spin">
    <button class="button-element-top"></button>
    <button class="button-element-bottom"></button>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.spin {
  display: grid;
  grid-template-columns: 1fr;
  width: 150px;
  height: 150px;
}
.button-element-top {
  background-image: url("../assets/pictures/triangle-up-img.png");
  background-size: 20%;
  background-position: center;
  background-repeat: no-repeat;
}

.button-element-bottom {
  background-image: url("../assets/pictures/triangle-down-img.png");
  background-size: 20%;
  background-position: center;
  background-repeat: no-repeat;
}
/* .button-element-bottom:hover, .button-element-top:hover{
    border-color: 1px solid rgb(188, 192, 248);
    background-color: rgb(209, 212, 253);
}
.button-element-bottom:focus, .button-element-top:focus{
    border-color: 1px solid rgb(188, 192, 248);
    background-color: rgb(138, 146, 252);
} */
</style>