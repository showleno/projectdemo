<template>
      <div class="center_column ">
          <div class="tab_page">
              <ul class="clearfix">
                  <li class="on"><a href="">首页</a><i class="fa fa-close"></i></li>
                  <li class="on"><a href="">首页</a><i class="fa fa-close"></i></li>
              </ul>
          </div>
            <div class="tab_main clearfix">
                <div class="loadHtml left">
                    <Index />
                </div>
                <RightColumn />
            </div>
      </div>
</template>
<script>
import RightColumn from './RightColumn'
import Index from '../pages/Index'
export default {
    name: 'CenterColumn',
    components: {
        'RightColumn': RightColumn,
        'Index': Index
    }
}
</script>
<style lang="scss">
    @import '../../assets/scss/base.scss';
    .leon-frame {
        .center_column {
            height: 888px;
            width: 100%;
            @include boxSizing();
            padding-left: 100px;
            .tab_page {
                width: 100%;
                background-color: #1d2c42;
                height: 40px;
                ul {
                    width: 100%;
                    height: 40px;
                }
                li {
                    width: 12%;
                    float: left;
                    position: relative;
                    margin-right: 1px;
                    a {
                        display: block;
                        text-align: center;
                        background: url('../../../static/images/bj_b.jpg') repeat-x;
                        width: 100%;
                        height: 40px;
                        line-height: 40px;
                        color: #fff;
                    }
                    i.fa {
                        position: absolute;
                        right: 10px;
                        top: 13px;
                        color: #fff;
                    }
                }
            }
            .tab_main {
                width: 100%;
                position: relative;
            }
            .loadHtml {
                margin-right: -100px;
                padding-right: 100px;
                width: 100%;
                @include boxSizing();
                height: 888px;
                .hell {
                    background: #000;
                    width: 100%;
                }
            }
        }
        
    }
</style>
