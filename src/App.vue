<template>
  <div id="app">
    <Lightbulb :isOn="currentValue"/>
    <div>
      <p>Simple usage</p>
      <div>
        <RockerSwitch :size="0.9" :value="currentValue" @change="isOn => (currentValue = isOn)"/>
      </div>
      <code>{{ currentValue }}</code>
    </div>
  </div>
</template>

<script>
import Lightbulb from "./Lightbulb";
import RockerSwitch from "vue-rocker-switch";
import "vue-rocker-switch/dist/vue-rocker-switch.css";

export default {
  name: "App",
  components: {
    RockerSwitch,
    Lightbulb
  },
  data() {
    return {
      currentValue: true
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
