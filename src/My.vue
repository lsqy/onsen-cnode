<template>
  <v-ons-page>
    <custom-toolbar>首页</custom-toolbar>
    <p style="text-align: center">
      我的详情
    </p>
  </v-ons-page>
</template>

<script>
  import customToolbar from 'customToolbar';
  import home from 'Home';
  export default {
     data() {
      return {
      }
     },
     methods: {
       pop(){
         this.pageStack.pop();
       },
       push() {
         this.pageStack.push(deliver);
       }
     },
     props: ['pageStack'],
     components: { customToolbar }
  }
</script>
