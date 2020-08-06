<template>
  <div>
    <label class="control">
       <input type="radio" class="control-input visually-hidden"/>
       <span class="control-indicator"></span>
       OptionButton
   </label>
   </div>
</template>

<script>
export default {};
</script>

<style scoped>
.visually-hidden{
        border: 0;
        clip: rect(0,0,0,0);
        height: 1px;
        margin: -1px;
        overflow: hidden;
        padding: 0;
        position: absolute;
        width: 1px;
    }
    .control{
        display: inline-flex;
        align-items: center;
    }
    .control-indicator{
        width:14px;
        height: 14px;
        margin: 1px;
        margin-right: 6px;
        border: 1px solid black;
        border-radius: 14px;
        /* background-image: url('./checkmark.png'); */
    }
    .control-input:hover ~ .control-indicator {
        background-color: rgb(184, 209, 255);
    }
    .control-input:checked ~ .control-indicator {
        /* background-color: rgb(145, 182, 250); */
        background-image: url('../assets/pictures/option.png');
        background-size: 6px;
        background-position: center;
        background-repeat: no-repeat;
    }
</style>