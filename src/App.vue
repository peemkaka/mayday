
<template>
  <img alt="Vue logo" class="mx-auto" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <div class="container">
    <div class="inner-container">
      <form action="">
        <div>
          <h2 class="heading">How was your Vue.js experience?</h2>
          <label class="label" for="name">Your Name</label>
          <input class="input" :class="{'bg-red-50':invalidName}"
            id="name" type="text" v-model.trim="enteredName" >
            <p v-if="invalidName" class="text-red-600">Please enter your name!</p>
        </div>
        <div>
          <h2 class="heading">My learning experience was...</h2>
          <div>
            <input class="radio" id="rating-poor" type="radio" >
            <label class="label" for="rating-poor">Poor</label>
            
          </div>
          <div>
            <input class="radio" id="rating-average" type="radio" >
            <label class="label" for="rating-average">average</label>
            
          </div>
          <div>
            <input class="radio" id="rating-great" type="radio" >
            <label class="label" for="rating-great">great</label>
            
          </div>
        </div>
        <button class="btn">
          Submit
        </button>
      </form>
    </div>
  </div>
</template>




<script>
import HelloWorld from './components/HelloWorld.vue'
export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return{
      invalidName : false,
      invalidRating : false,
      enteredName : '',
      rating : null
    }
  },
  methods:{
    submitForm(){
      if(this.enteredName===''){this.invalidName = true;}else{this.invalidName = false;}
      if(this.rating===null){this.invalidRating=true;}else{this.invalidRating=false;}
    }
  }
}
</script>

