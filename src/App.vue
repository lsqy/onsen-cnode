<template id="main">
  <v-ons-page>
    <v-ons-tabbar position="auto"
      :tabs="tabs"
      :visible="true"
      :index="activeIndex"
      @update="activeIndex = $event"
    >
    </v-ons-tabbar>
  </v-ons-page>
</template>
<style lang="less">
.tabbar__button {
  border: none;
}
</style>
<script>
  import home from 'Home';
  import my from 'My';
  import message from 'Message';
  import deliver from 'Deliver';

  export default {
    data() {
      return {
      activeIndex: 0,
      tabs: [
        {
          icon: this.md() ? null : 'ion-home',
          label: '首页',
          page: home
        },
        {
          icon: this.md() ? null : 'ion-ios-bell',
          label: '消息',
          page: message,
          badge: 7
        },
        {
          icon: this.md() ? null : 'ion-ios-settings',
          label: '发表',
          page: deliver
        },
        {
          icon: this.md() ? null : 'md-face',
          label: '我的',
          page: my
        }
      ]
      }
    },
    methods: {
      md() {
        return this.$ons.platform.isAndroid();
      },
      add() {
        this.tabs[1].badge++;
      }
    },
    computed: {
      title() {
        return this.tabs[this.activeIndex].label;
      }
    }
  }
</script>
