<template>
  <div>
    <h1>I'm Learning Vue</h1>
    <input type="text" placeholder="Filter Search" v-model="query" />
    <p>{{query}}</p>
    <button @click="reset">Reset</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup(){
    const query = ref("");

    const reset = (evt) =>{
      query.value = "";
    }
    return {
      query,
      reset,
    };
  }
}
</script>
