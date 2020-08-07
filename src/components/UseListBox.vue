<template>
  <div>
    <div class="list-outer">
      <ul class="ul">
        <li class="li" v-for="value in liContent" :key="value">
          <div class="div">
            <i style="font-size:11px" class="fa">&#xf15b;</i>
            <span class="span">{{value}}</span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      liContent: [
        "AcceptAllChanges",
        "AccuracyVersion",
        "Activate",
        "ActiveChart",
        "ActiveSheet",
        "ActiveSlicer",
        "AddToFavorites",
        "Application",
        "ApplyTheme",
        "AutoFilter",
        "AutoFilterMode",
        "Hello1",
        "Hello1",
        "Hello1",
      ],
    };
  },
};
</script>

<style>
.list-outer {
  border: 1px solid gray;
  width: 250px;
  height: 280px;
  overflow-y: auto;
  overflow-x: none;
}
.ul {
  display: block;
  list-style-type: none;
  margin-block-start: 0em;
  margin-block-end: 0em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  padding-inline-start: 0px;
}
.li {
  padding: 3px;
  margin: 1px;
  text-align: left;
  font-size: 14px;
  height: 16px;
  border: 0.5px solid white;
  cursor: pointer;
}
.li:hover {
  margin: 1px;
  border-color: rgb(132, 132, 255);
  border-radius: 2px;
  background-color: rgb(209, 223, 248);
}
.fa {
  margin-left: 4px;
  margin-top: 3px;
}
.span {
  margin: 4px;
  margin-left: 7px;
  margin-top: 0px;
  font-family: Arial, Helvetica, sans-serif;
}
.div {
  display: grid;
  grid-template-columns: 12px 1fr;
}
</style>