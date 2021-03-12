<template>
  <div class="nav">
    <router-link to="/labels">
    <Icon name="label"/>
      主页
    </router-link>
    |
    <router-link to="/money">
    <Icon name="money"/>
      记账
    </router-link>
    |
    <router-link to="/statistics">
      <Icon name="statistics"/>
      统计
    </router-link>
  </div>
</template>

<script lang="ts">



export default {
  name: 'Nav'
};
</script>

<style lang="scss" scoped>

</style>