<template>
  <div class="about">
    <h1>This is an about page</h1>
    <ParentComponent v-slot="{user}">
      <Header v-bind:user="user"/>
    </ParentComponent>
  </div>
</template>

<script>
import ParentComponent from '@/components/ParentComponent';
//import ChildrenComponent from "@/components/ChildrenComponent";
import Header from '@/components/Header';
export default {
  name: 'About',
  components: {
    ParentComponent,
    //ChildrenComponent,
  Header
  }
}
</script>
