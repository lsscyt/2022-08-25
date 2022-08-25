<template>
  <div>
    <ul>
      <li v-for="item in Myli" :key="item">{{ item }}</li>
    </ul>
    <button @click="walk">按钮</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      Myli: ["刘备", "张飞", "关羽"],
    };
  },
  methods: {
    walk() {
      this.Myli.push(this.Myli[0]);
      this.Myli.shift(this.Myli[0]);
    },
  },
};
</script>

<style scoped>
button {
  width: 60px;
  height: 30px;
  background-color: cyan;
}
</style>
