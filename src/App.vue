<template>
  <div id="app">
    <cube-tab-bar v-model="tabString" :data="tabs" @change="changeHandler"></cube-tab-bar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tabString: '待使用',
      tabs: [
        {
          label: '全部',
          icon: ''
        },
        {
          label: '待付款'
        },
        {
          label: '待使用'
        },
        {
          label: '待评价'
        },
        {
          label: '退货/退款'
        }
      ]
    };
  },
  methods: {
    changeHandler() {}
  }
};
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  .cube-tab {
    // flex-basis: auto;
  }
}

#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
