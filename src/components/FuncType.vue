<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script lang="ts" setup>
import { onMounted, ref } from "vue";

const msg = ref("666");
class Person{
  name:string
  constructor(n:string){
    this.name = n
  }
  sayHi():void{
    alert(this.name)
  }
}
onMounted(() => {
  console.log("走这里");
  let a = new Person('zhangsan')
  a.sayHi()
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
