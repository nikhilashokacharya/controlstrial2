<template>
  <div>
    <div>
      <button class="commandbutton-element">Find Next</button>
    </div>
    <hr />
    <div class="dialog-action-div">
      <button class="dialog-action-button">Command Button 1</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.commandbutton-element {
  border: 1px solid gray;
  border-radius: 3px;
  background-color: white;
  min-width: 50px;
  max-width: 112px;
  width: fit-content;
  height: fit-content;
  min-height: 20px;
  padding: 0px 5px 0px 5px;
  overflow: hidden;
}
.dialog-action-button {
  background-color: white;
  width: 80px;
  max-width: 80px;
  height: 28px;
  padding-left: 5px;
  padding-right: 5px;
  padding-top: 8px;
  padding-bottom: 8px;
  height: fit-content;
  border: 1px solid gray;
  border-radius: 3px;
  overflow: hidden;
}
</style>