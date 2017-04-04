<template>
  <v-ons-page>
    <custom-toolbar>发表</custom-toolbar>
    <p style="text-align: center">发表页面</p>
  </v-ons-page>
</template>

<script>
  import customToolbar from 'customToolbar';
  import app from 'App';

  export default {
    methods: {
      pop() {
        this.pageStack.pop();
      }
    },
    props: ['pageStack'],
    components: { customToolbar }
  }
</script>
