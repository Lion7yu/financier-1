<template>
  <div>
    <ul class="types">
      <li :class="type === '-' && 'selected'"
      @click="selectType('-')">支出</li>
      <li :class="type === '+' && 'selected'"
      @click="selectType('+')">收入</li>
    </ul>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  import {Component} from 'vue-property-decorator';
  @Component //装饰器
  export default class Types extends Vue{
    type = '-' //'-'表示支出,‘+’表示收入
    selectType(type: string){ //type 只能是'-' 或 '+' 中的一个
      if(type !== '-' && type !== '+'){
        throw new Error('type is unknown')
      }
      this.type = type
    }
  }

</script>

<style lang="scss" scoped>
.types {
  background: #0C78FF;
  display: flex;
  font-size: 24px;
  text-align: center;

  > li {
    width: 50%;
    height: 64px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    color: #fff;

    &.selected {
      //&::after {
      //  content: '';
      //  position: absolute;
      //  bottom: 0;
      //  left: 0;
      //  width: 100%;
      //  height: 8px;
        background: rgb(252, 112, 65);
      //}
    }
  }
}
</style>