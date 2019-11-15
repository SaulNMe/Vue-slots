<template>
  <div class="cotainer" id="counter">
    <div class="notification">
      <h1 class="title" align="center">
          Data with Vuex: 
        {{ count }}
      </h1>
      <h1>
          Local data:
        {{numbers}}
        <input v-model="number" type="number"/>
        <button @click="$emit('number-added', Number(number))">Add number</button>
      </h1>
    </div>
  </div>
</template>
<script>
import { mapState } from "vuex";

export default {
  computed: mapState({
    count: state => state.count
    }),
  props: {
    numbers: Array
  },
  data() {
    return {
      number: 0
      }
  }
}
</script>