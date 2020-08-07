<template>
  <div id="app">
<UseCheckbox />
<hr>
<UseOptionButton />
<hr>
<UseCombobox />
<hr>
<UseTextBox />
<hr>
<UseCommandButton />
<hr>
<UseSpinButton />
<hr>
<UseListBox />
<hr>
<testSpinButton />
<hr>
<UseToggleButton />
<hr>
<UseScrollBar />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import UseCheckbox from './components/UseCheckbox.vue';
import UseCombobox from './components/UseCombobox.vue';
import UseCommandButton from './components/UseCommandButton.vue';
import UseListBox from './components/UseListBox.vue';
import UseOptionButton from './components/UseOptionButton.vue';
import UseTextBox from './components/UseTextBox.vue';
import UseSpinButton from './components/UseSpinButton.vue';
import testSpinButton from './components/testSpinButton.vue';
import UseToggleButton from './components/UseToggleButton.vue';
import UseScrollBar from './components/UseScrollBar.vue'


@Component({
  components: {
    UseCheckbox,
    UseCombobox,
    UseCommandButton,
    UseListBox,
    UseOptionButton,
    UseTextBox,
    UseSpinButton,
    testSpinButton,
    UseToggleButton,
    UseScrollBar
  },
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
