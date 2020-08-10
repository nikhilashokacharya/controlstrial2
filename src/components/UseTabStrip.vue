<template>
  <div class="outer">
    <div class="tabs">
      <div style="display: inline-block;overflow: auto;scroll-behavior: smooth;">
        <div class="tab" v-for="(value,key) in selectedCopy" :key="key">
            <!-- <div v-if="key<=3"> -->
          <input name="tab-group-1" :id="value.id" type="radio" />
          <label :for="value.id">{{value.tabLabel}}</label>
          <div class="content">{{value.tabContent}}</div>
          <span v-if="selectedCopy.length-1>key">
            <span class="seperator"></span>
          </span>
          <!-- </div> -->
          <!-- <div v-if="key==4">
          <input name="tab-group-1" :id="value.id" type="radio" />
          <label :for="value.id">{{value.tabLabel}}</label>
          <div class="content">{{value.tabContent}}</div>
          <span v-if="values.length-1>key">
            <span class="seperator"></span>
          </span>
          </div> -->
        </div>
      </div>
      <div class="scroll-tab tab" style="margin-top:13px">
        <button class="tab-button" @click="decrease">
          <i class="fa fa-angle-double-left"></i>
        </button>
        <button class="tab-button" @click="increase">
          <i class="fa fa-angle-double-right"></i>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      values: [
        {
          id: "tab-1",
          tabLabel: "Tab One",
          tabContent: "Hello",
        },
        {
          id: "tab-2",
          tabLabel: "Tab Two",
          tabContent: "How",
        },
        {
          id: "tab-3",
          tabLabel: "Tab Three",
          tabContent: "Are",
        },
        {
          id: "tab-4",
          tabLabel: "Tab Four",
          tabContent: "You",
        },
        { id: "tab-5", tabLabel: "Tab Five", tabContent: "Content Five" },
        { id: "tab-6", tabLabel: "Tab Six", tabContent: "Content Six" },
        // { id: "tab-7", tabLabel: "Tab Seven", tabContent: "Content Seven" },
        // { id: "tab-8", tabLabel: "Tab Eight", tabContent: "Content Eight" },
        // { id: "tab-9", tabLabel: "Tab Nine", tabContent: "Content Nine" },
      ],
      selectedCopy:[
        {
          id: "tab-1",
          tabLabel: "Tab One",
          tabContent: "Hello",
        },
        {
          id: "tab-2",
          tabLabel: "Tab Two",
          tabContent: "How",
        },
        {
          id: "tab-3",
          tabLabel: "Tab Three",
          tabContent: "Are",
        },
        {
          id: "tab-4",
          tabLabel: "Tab Four",
          tabContent: "You",
        },
        { id: "tab-5", tabLabel: "Tab Five", tabContent: "Content Five" },
        { id: "tab-6", tabLabel: "Tab Six", tabContent: "Content Six" },
        // { id: "tab-7", tabLabel: "Tab Seven", tabContent: "Content Seven" },
        // { id: "tab-8", tabLabel: "Tab Eight", tabContent: "Content Eight" },
        // { id: "tab-9", tabLabel: "Tab Nine", tabContent: "Content Nine" },
      ],
    };
  },
  methods: {
    increase() {
      //   console.log("increase value");
      const ele = document.getElementsByName("tab-group-1");
      let i;
      for (i = 0; i < ele.length; i++) {
        if (ele[i].checked) {
          if (i === ele.length - 1) {
            return;
          }
          //   console.log(ele[i]);
          ele[i + 1].checked = true;
          const selectedIndex = i+1;
          if (selectedIndex>=5) {
              this.selectedCopy = [];
               for (let index = selectedIndex - 3; index < this.values.length; index++) {
                   this.selectedCopy.push(this.values[index]);
               }
          }
          break;
        }
      }
    },
    decrease() {
      //   console.log("decrease value");
      const ele = document.getElementsByName("tab-group-1");
      let i;
      for (i = 0; i < ele.length; i++) {
        if (ele[i].checked) {
          if (i === 0) {
            return;
          }
          //   console.log(ele[i]);
          ele[i - 1].checked = true;
          break;
        }
      }
    },
  },
  mounted() {
    const ele = document.getElementsByName("tab-group-1");
    ele[0].checked = true;
  console.log(this.selectedCopy);
  },
};
</script>

<style scoped>
.outer {
  width: 411px;
  height: 300px;
  border: 1px solid #0d46ffad;
  overflow-y: auto;
  overflow-x: hidden;
}

.tabs {
  display: grid;
  grid-template-columns: 330px 35px;
  position: relative;
  clear: both;
  margin: 0;
  margin-left: 10px;
  width: calc(100% - 10px);
  height: 100%;
  white-space: nowrap;
  overflow-x: auto;
  overflow-y: hidden;
}

.tab {
  display: inline-block;
  vertical-align: top;
  z-index: 1;
}

.scroll-tab{
    z-index: 2;
}
.tab label {
  background-color: white;
  display: inline-block;
  padding: 12px 10px 10px 10px;
  margin: 0;
  cursor: pointer;
  position: relative;
  /* left: 1px; */
}

.tab [type="radio"] {
  display: none;
}

.tab .content {
  position: absolute;
  white-space: normal;
  top: 41px;
  left: 0px;
  background: white;
  height: 100px;
  right: 0;
  bottom: 0;
  padding: 20px;
  padding-right: 10px;
  width: calc(100% - 42px);
  height: calc(100% - 95px);
  border: 1px solid #ccc;
}

.tab [type="radio"]:checked ~ label {
  background: white;
  color: rgb(3 44 207);
  border-bottom: 2px solid rgb(3 44 207);
  font-weight: bold;
  z-index: 2;
}

.tab [type="radio"]:checked ~ label ~ .content {
  z-index: 1;
}

.seperator {
  display: inline-block;
  height: 12px;
  width: 1px;
  margin-top: 15px;
  margin-right: 1px;
  background-color: gray;
}

.content {
  overflow: auto;
}

.tab-button {
  font-size: 8px;
  width: 13px;
  height: 13px;
  border: 1px solid gray;
  border-radius: 2px;
  padding-left: 0px;
}
/* .tab-scroll-buttons {
        padding-top: 12px;
        width: 13px;
        height: 13px;
    } */
</style>