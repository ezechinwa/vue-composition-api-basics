<!-- <script setup>
</script> -->

<template>
  <div class="home">
     <section class="homenav flex justify-between space-x-5 p-4 mt-5">
        <button class="bg-green-500 px-6  py-2 border-radius-5 text-bold text-2xl" @click="increaseCounter">+</button>
        <span class="text-4xl text-white text-bold"> {{counter}} </span>
        <button class="bg-red-500 px-6  py-2 border-radius-5 text-bold text-2xl" @click="decreaseCounter">-</button>
       
     </section>
  

  </div>
</template>

<!-- Composition API recommended approach -->
<script setup>
  import { ref } from 'vue'
    const counter = ref(0)
    const decreaseCounter = ()  =>{
      counter.value--
    }
    const increaseCounter  = () =>{
      counter.value++
    }

</script>

<!-- Composition API -->
<!-- <script>
  import { ref } from 'vue'
export default {
  setup() {
    const counter = ref(0)
    const decreaseCounter = ()  =>{
      counter.value--
    }
    const increaseCounter  = () =>{
      counter.value++
    }

    
    return {
      counter,decreaseCounter,increaseCounter
    }
  },
}
</script> -->


<!--Vue Options API -->
<!-- 
<script>
  export default {
    data(){
      return {
        counter: 0
      }
    },
    methods: {
      decreaseCounter(){
        this.counter-- 
      },
      increaseCounter(){
        this.counter++
      }
    }
  }

</script> -->