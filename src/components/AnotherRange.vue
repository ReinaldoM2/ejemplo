<template>
  <div>
    <input type="email" name id>
    <vue-range-slider
      :tooltip-dir="['bottom','bottom']"
      :use-keyboard="true"
      :enable-cross="false"
      :slider-style="[{backgroundColor: 'white'}]"
      :bg-style="{backgroundColor: '#B0BEC5'}"
      :process-style="{backgroundColor: '#B0BEC5'}"
      :tooltip-style="[{backgroundColor: '#283593'}, {backgroundColor: '#283593'}]"
      :formatter="(value)=> `${value} M`"
      :real-time="true"
      :min="1"
      :max="1000"
      style="padding-top: 50px"
      ref="slider"
      v-model="value"
    ></vue-range-slider>
  </div>
</template>
<script>
import VueRangeSlider from "vue-range-component";
export default {
  data() {
    return {
      value: [1, 100]
    };
  },
  components: {
    VueRangeSlider
  }
};
</script>

