import Vue from 'vue/dist/vue.esm.js';
<template>
  <div id="app">
    <div @click="count_10_hide" style="color:blue; background:red; display:inline-block; height:95px; width:95px; border-radius:50%;"></div>
    <h1 v-if="viewed">Count:{{count}}</h1>
    </div>
</template>



  <script src="https://unpkg.com/vue@2.0.3/dist/vue.js"></script>
  <script>
    var App = new Vue({
      el: '#app',
      data: {
        //message: 'Is it working',
        count: 0,
		viewed:false
      },
      methods: {
      count_10_hide: function() {
      this.count  +=  1
      if(this.count==10){
      this.count=0;
			this.viewed=false;}
      else{
      this.viewed=true;}
      }}
    })
  </script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
