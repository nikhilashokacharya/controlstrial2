<template>
  <div>
      <div class="box">
        <select class="box-select" @mouseover="hovered">
            <option class="box-option" value="" @mouseover="hovered">Option 1</option>
            <option class="box-option" value="">Option 2</option>
            <option class="box-option" value="">Option 3</option>
            <option class="box-option" value="">Option 4</option>
            <option class="box-option" value="">Option 5</option>
        </select>
    </div>
  </div>
</template>

<script>
export default {
methods:{
    hovered(e){
        console.log(e);
    }
}
}
</script>

<style scoped>
    .box {
        position: absolute;
    }

    .box-select {
        background-color: white;
        color: black;
        border-color: lightgray;
        padding-left: 10px;
        width: 150px;
        height: 25px;
        font-size: 14px;
        outline: none;
        -webkit-appearance: none;
        -moz-appearance: none;        
        appearance: none;
        border-radius: 3px;
    }
    option:hover{
        /* box-shadow: 0 0 10px 100px #111111 inset; */
       /* rgb(226, 235, 255) */
        border-radius: 6px;
        -webkit-appearance: none;
        background:  red !important;
    }

    .box:before {
        content: '';
        position: absolute;
        top: 1px;
        right: 1px;
        width: 25px;
        height: 23px;
        float: right;
        background: white;
        background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="50" border="1px solid red"><polygon points="0,0 100,0 50,50" style="fill:%23666666;stroke-width:3;stroke:rgb(0,0,250)" /></svg>');
        background-size: 40%;
        background-position: center;
        background-repeat: no-repeat;
        pointer-events: none;
    }

    .box:hover:before {
        background-color: rgb(233, 243, 255);
        border-left: 1px solid rgb(57, 159, 255);
    }
    .box:focus:before {
        background-color: rgb(136, 189, 255);
        border-left: 1px solid rgb(57, 159, 255);
    }

    .box select:hover {
        border-color: rgb(57, 159, 255);
    }
</style>