
<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input type="text" name="input1" v-model.lazy="data1" />
    <input type="password" name="input1" v-model="password" />
    <p v-if="condition">{{ data1 }}</p>
    <p v-else>condition false</p>
    <button v-on:click="method1">change condition</button>
    <ul>
      <li v-for="(item, index) in tabledata" :key="index">{{ item }}  {{ index }}</li>
      
    </ul>
    <form v-for="(check,index) in checkbox" :key="index">
      <input type="checkbox" :id=check :value=check v-model="checkboxvalue">
      <label >{{ check }}</label>
    </form>
    <span>{{ checkboxvalue }}</span>
    
  </div>
</template>


<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      data1 : "data1content",
      password : "password",
      condition : false,
      tabledata: ['data1','data2','data3'],
      checkbox : ['Jack','John','Mike'],
      checkboxvalue : []
    }
  },
  methods: {
    method1(){
      console.log("test mehod1")
      this.condition=!this.condition
    }
  },
  props: {
    msg: String
  }
}
</script>