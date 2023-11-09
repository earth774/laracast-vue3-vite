<script setup>
  import {useFlash} from "@/composables/useFlash";
  import {state} from "@/stores/quizStore";

  let {flash} = useFlash();
</script>


<!-- <script>
import flash from '@/mixins/flash';

export default{
  mixins:[flash]
};
</script> -->

 <!-- <script setup>
//import TheWelcome from '../components/TheWelcome.vue' 

// import { onMounted,ref } from 'vue';
// export default{
  // components:{TheWelcome},

  // setup() {
  //   onMounted(() => {
  //     alert("app alraedy");
  //   });

  //   let message = ref("Hello World");

  //   setTimeout(() => {
  //     message.value = "new set";
  //   }, 2000);

  //   return{
  //     message
  //   }
  // }

  // eslint-disable-next-line no-undef
// let message = $ref("Hello World 123");

// setTimeout(() => {
//   message = "new set";
// }, 2000);

// let doYouClick = ()=>{
//   alert('abc');
// };
// };
</script> -->

<template>
  <main>
    <TheWelcome />
    <h1>{{ message }}</h1>
    <h5>{{ state.name }}</h5>
    <button @click="flash('Success!','Hello World')">Click</button>
  </main>
</template>
