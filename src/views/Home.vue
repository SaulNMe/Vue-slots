<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <Counter :numbers="numbers" @onClick="addtoToCounter"/><br />
    <div class="columns">
      <div class="column is-11">
        <AddCounter></AddCounter>
      </div>
      <div class="column auto">
        <RemoveCounter></RemoveCounter>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Counter from '@/components/Counter';
import AddCounter from '@/components/AddCounter';
import RemoveCounter from '@/components/RemoveCounter';

export default {
  name: "home",
  components: {
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
    addtoToCounter(n) {
      this.numbers.push(n);
    }
  }
};
</script>
