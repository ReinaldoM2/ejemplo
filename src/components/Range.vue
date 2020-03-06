<template>
  <div>
    <div>
      <input type="text">
      <input type="text">
      <vue-slider
        v-model="value"
        :min="1"
        :max="1000"
        :tooltip="'always'"
        :tooltip-formatter="formater1"
        :enable-cross="false"
        :tooltip-placement="['bottom', 'right']"
        style="padding-top: 15px;"
        :process="false"
        :tooltipStyle="{backgroundColor: '#283593', color: 'white', borderColor:'#283593'}"
        :processStyle="{backgroundColor: 'red'}"
      ></vue-slider>
    </div>
  </div>
</template>
<script>
import VueSlider from "vue-slider-component";

export default {
  data() {
    return {
      value: [15, 50],
      formater1: "{value} M"
    };
  },
  components: {
    VueSlider
  }
};
</script>
