<template>
  <div id="app">
    <input type="text" v-model="text">
    <button @click="tijiao">提交</button>
    <ul>
      <li v-for="(item,index) in arr" @click="remove(index)">{{item}}</li>
    </ul>
  </div>
  
    
</template>

<script>


export default {
  name: 'app',
  data(){
    return {
      text:null
      ,arr:[]
      
    }
  },
  
  methods:{
    tijiao:function(){
      this.arr.push(this.text);
      this.text = ''
    },
    remove:function(index){
      this.arr.splice(index,1)

    }

  }

  
}
</script>

<style>

</style>
