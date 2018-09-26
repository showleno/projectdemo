<template>
  <div class="leon-frame">
    <Header />
    <div class="main clearfix">
        <LeftColumn :sidebarHeight=sidebarHeight />
        <RightColumn :sidebarHeight=sidebarHeight />
        <CenterColumn :mainHeight=mainHeight />
    </div>
    <LeftSideBar :sidebarHeight=sidebarHeight />
    <RightSideBar :sidebarHeight=sidebarHeight />
  </div>
</template>

<script>
import Header from './editViews/Header'
import LeftColumn from './editViews/LeftColumn'
import RightColumn from './editViews/RightColumn'
import CenterColumn from './editViews/CenterColumn'
import LeftSideBar from './mtk/LeftSideBar'
import RightSideBar from './mtk/RightSideBar'

export default {
  name: 'Frame',
  components: {
    'Header': Header,
    'LeftColumn': LeftColumn,
    'CenterColumn': CenterColumn,
    'RightColumn': RightColumn,
    'LeftSideBar': LeftSideBar,
    'RightSideBar': RightSideBar,
  },
  data () {
    return {
            mainHeight: null,
            sidebarHeight: null
    }
  },
  mounted () {
      this.computHeight();
  },
  methods : {
      computHeight: function() {
          var height = document.body.clientHeight || document.documentElement.clientHeight;
          this.sidebarHeight = height - 70;
          this.mainHeight = height - 110;
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
  .leon-frame {
    .main {
      min-height: 888px;
      position: relative;
    }
  }
</style>
