<template>
  <div>
    <div class="slider-component">
      <div class="slidecontainer">
        <input
          ref="input"
          v-model="currentValue"
          type="range"
          :min="min"
          :max="max"
          class="slider"
          @input="onInput"
        >
        <div class="slidersucces" :style="'width: calc('+ (Math.floor(100 /max) * value)  + '% - 4px'"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
    props: {
        value: {
            type: Number,
            required: true
        },
        min: {
            type: Number,
            required: true
        },
        max: {
            type: Number,
            required: true
        }
    },
    data(){
        return {
            currentValue: this.value
        };
    },
    methods: {
        onInput() {
            // this.currentValue is a string because HTML is weird
            this.$emit('input', parseInt(this.currentValue));
        }
    }
};
</script>
