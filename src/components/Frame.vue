<template>
  <div class="leon-frame">
    <Header />
    <div class="main clearfix">
        <LeftColumn />
        <CenterColumn />
    </div>
  </div>
</template>

<script>
import Header from './editViews/Header'
import LeftColumn from './editViews/LeftColumn'
import CenterColumn from './editViews/CenterColumn'

export default {
  name: 'Frame',
  components: {
    'Header': Header,
    'LeftColumn': LeftColumn,
    'CenterColumn': CenterColumn
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  .leon-frame {
    .main {
      min-height: 888px;
    }
  }
</style>
