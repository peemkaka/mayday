<template>
  <div class="container">
    <div class="inner-container">
      <form action="">
        <div>
          <h2 class="heading">How was your Vue.js experience?</h2>
          <label class="label" for="name">Your Name</label>
          <input class="input" id="name" type="text">
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
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

