<template >
  <div>
    <div v-bind:class="isRed?'red':'pink'"></div>
    <div v-bind:class="{red:true,big:true}"> 123456</div>
    <ul>
      <li v-for="stu in stus" v-bind:key="stu" :class="{'A':'red','B':'pink'}[stu.score]">
        {{stu.name}}
      </li>
    </ul>
   </div>
</template>

<script>
export default {
  name: 'Test01',
  data () {
    return {
      isRed: true,
      stus: [{name: 'mj', score: 'A'}, {name: 'psw', score: 'B'}]
    }
  }
}
</script>

<style scoped>
.red
{
  background-color: red;
}
.pink
{
   background-color: pink;
 }
.big
{

  font-size: 25px;
}
</style>
