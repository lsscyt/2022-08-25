<template>
  <div>
    <ul>
      <li v-for="(item, index) in num" :key="item">
        {{ item }}&nbsp; &nbsp;&nbsp;<button @click="deleted(index)">
          删除
        </button>
      </li>
    </ul>
    <button @click="add">增加</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: [1, 5, 7],
    };
  },
  methods: {
    deleted(index) {
      this.num.splice(index, 1);
    },
    add() {
      this.num.push(Math.random(0, 1).toFixed(2) * 100);
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
