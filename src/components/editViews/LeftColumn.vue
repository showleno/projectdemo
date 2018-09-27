<template>
      <div class="left_column" :style="{'height': sidebarHeight + 'px' }">
          <div class="toggle_btn">
              <a class="btn"><i class="fa fa-align-justify"></i>功能区</a>
          </div>
          <div class="func_module">
              <div class="layout_btn mod btn clearfix">
                  <span>布局</span>
                  <p><i class="fa fa-table"></i></p>
              </div>
              <div class="beauty_btn mod btn clearfix">
                  <span>美化</span>
                  <p><i class="fa fa-magic"></i></p>
              </div>
              <div class="module_btn mod btn clearfix">
                  <span>模块</span>
                  <p><i class="fa fa-tasks"></i></p>
              </div>
              <div class="plugin_btn mod btn clearfix">
                  <span>插件</span>
                  <p><i class="fa fa-star-half-empty"></i></p>
              </div>
              <div class="plugin_btn mod btn clearfix">
                  <span>引导</span>
                  <p><i class="fa fa-compass"></i></p>
              </div>
          </div>
      </div>
</template>
<script>
    export default {
        name: 'LeftColumn',
        props: ['sidebarHeight'],
    }
</script>
<style lang="scss">
    @import '../../assets/scss/base.scss';
    .leon-frame {
        .toggle_btn {
            a {
                display: block;
                line-height: 40px;
                background-color: #142335;
                width: 100px;
                height: 40px;
                text-align: center;
                i.fa {
                    margin-right: 8px;
                }
            }
        }
        .left_column {
            width: 100px;
            background-color: #1c2d41;
            color: #fff;
            position: absolute;
            left: 0;
            top: 0;
            .func_module {
                .mod {
                    margin: 10px 0;
                    position: relative;
                    left: -4px;
                    cursor: pointer;
                    border-radius: 0 20px 20px 0;
                    border: 3px solid #142335;
                    background: url('../../../static/images/b.png') no-repeat bottom right #142335;
                    box-shadow: 0 5px 5px #182d66;
                    width: 84px;
                    height: 65px;
                    @include boxSizing();
                    color: #c2c4c7;
                    padding: 10px 0 10px 10px;
                    span {
                        width: 20px;
                        text-align: center;
                        float: left;
                    }
                    p {
                        float: left;
                        margin-left: 10px;
                        i.fa {
                            font-size: 24px;
                            line-height: 38px;
                            color: #2f91e3;
                            box-shadow: 0 0 8px #19327f;
                        }
                    }
                    &:hover {
                        border: 3px solid #3b8efe;
                        box-shadow: 0 5px 13px #2045d7;
                        background-image: none;
                        span {
                            color: #fff;
                        }
                        i.fa {
                            color: #0d6fff;
                        }
                    }
                }
            }
        }
    }
</style>
