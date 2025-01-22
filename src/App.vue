<template>
  <div id="app">
    <van-notice-bar>请 fork 此示例，并重现你的问题</van-notice-bar>
    <van-count-down :time="time" millisecond @finish="test" />
    <van-count-down :time="time2" millisecond @finish="test2" />
    <p>{{ name }}</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      time: "",
      time2: "",
      show: false,
      name: "测试",
    };
  },
  mounted() {
    setTimeout(() => {
      this.time = 6 * 1000;
      this.time2 = 6 * 1000;
    }, 2000);
  },
  methods: {
    test() {
      console.log(1111);
    },
    test2() {
      console.log(1111);
    },
  },
};
</script>

<style>
.my-button {
  margin: 15px;
}
</style>
