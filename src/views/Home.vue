<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <Counter :numbers="numbers" @number-added="alertAny"/><br />
    <div class="columns">
      <div class="column is-11">
        <AddCounter></AddCounter>
      </div>
      <div class="column auto">
        <RemoveCounter></RemoveCounter>
      </div>
    </div>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  </div>
</template>

<script>
// @ is an alias to /src
import Counter from '@/components/Counter';
import AddCounter from '@/components/AddCounter';
import RemoveCounter from '@/components/RemoveCounter';
//import HelloWorld from "@/components/HelloWorld";

export default {
  name: "home",
  components: {
    //HelloWorld,
    Counter,
    AddCounter,
    RemoveCounter
  },
  data() {
    return {
        numbers : [1,2,3,4]
    }
  },
  methods: {
    alertAny(n) {
      this.numbers.push(n);
    }
  }
};
</script>
