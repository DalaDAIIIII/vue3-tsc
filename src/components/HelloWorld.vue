<template>
  <div id="counter">Counter: {{ counter }}</div>
  <div>
    <button :disabled="flag" @click="del">-</button>
    <button @click="count">+</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0,
      flag: false,
    };
  },
  methods: {
    count() {
      this.counter++;
      this.flag = false;
    },
    del() {
      if (this.counter) {
        this.counter--;
      } else {
        this.flag = true;
      }
    },
  },
  // mounted() {
  //   setInterval(()=>{
  //     this.counter++;
  //   },1000)
  // },
};
</script>

<style></style>
