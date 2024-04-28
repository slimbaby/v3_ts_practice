<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div>1111111</div>
  </div>
</template>

<script lang="ts" setup>
import { onMounted, ref } from "vue";

const msg = ref("666");
function changeMsg(str: string) {
  msg.value = str;
}
onMounted(() => {
  changeMsg("我改变了！");
});
</script>

<style scoped lang="scss">
.hello{
  color: pink;
  h1{
    font-size: 48px;
  }
}
</style>
