<template>
  <v-ons-page>
    <custom-toolbar>首页</custom-toolbar>
    <p style="text-align: center">
      这是首页
    </p>
    <v-ons-button>改变消息数目</v-ons-button>
  </v-ons-page>
</template>

<script>
  import customToolbar from 'customToolbar';
  import deliver from 'Deliver';
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
       },
       add() {

       }
     },
     props: ['pageStack'],
     components: { customToolbar }
  }
</script>
