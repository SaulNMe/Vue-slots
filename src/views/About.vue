<template>
  <div class="about">
    <h1>This is an about page</h1>
    <ParentComponent v-slot="{data}">
      <Header v-bind:data="data"/>
    </ParentComponent>
  </div>
</template>

<script>
import ParentComponent from '@/components/ParentComponent';
import Header from '@/components/Header';

export default {
  name: 'About',
  components: {
    ParentComponent,
    Header
  }
}
</script>
