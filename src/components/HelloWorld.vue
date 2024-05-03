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
function abc(a: string) :void{
  let b: number = 1;
  let c: number[] = [1, 2, 3];
  let d: object = {};
  let e: any = 123;
  e = "123";
  console.log(a, b, c, d, e);
}
onMounted(() => {
  changeMsg("我改变了！");
  abc("666");
  console.log(abc('777'));
  
});
</script>

<style scoped lang="scss">
.hello {
  color: pink;
  h1 {
    font-size: 48px;
  }
}
</style>
