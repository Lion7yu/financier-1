<template>
  <div class="nav">
    <router-link to="/labels">主页</router-link>
    |
    <router-link to="/money">记账</router-link>
    |
    <router-link to="/statistics">统计</router-link>
  </div>
</template>

<script lang="ts">
export default {
  name: 'Nav'
};
</script>

<style lang="scss" scoped>

</style>