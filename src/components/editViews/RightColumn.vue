<template>
      <div class="right_column" :style="{'height': sidebarHeight + 'px' }">
            <div class="toggle_btn">
                <a class="btn"><i class="fa fa-chevron-up"></i>页面区</a>
            </div>
            <div class="func_module">
                <a href=""><em></em>首页</a>
                <a href=""><em></em>简介</a>
            </div>
      </div>
</template>
<script>
    export default {
        name: 'RightColumn',
        props: ['sidebarHeight'],
    }
</script>
<style lang="scss">
    @import '../../assets/scss/base.scss';
        .leon-frame {
            .right_column {
                width: 100px;
                min-height: 848px;
                position: absolute;
                right: 0;
                top: 0;
                background-color: #1c2d40;
                .toggle_btn {
                    a {
                        display: block;
                        height: 40px;
                        line-height: 40px;
                        text-align: center;
                        background-color: #431ded;
                        color:  #fff;
                    }
                }
                .func_module {
                    a {
                        width: 100px;
                        height: 40px;
                        display: block;
                        line-height: 40px;
                        position: relative;
                        color: #fff;
                        @include boxSizing();
                        padding-left: 32px;
                        em {
                            width: 12px;
                            height: 12px;
                            background-color: #2f91e3;
                            position: absolute;
                            left: 10px;
                            top: 14px;
                            border-radius: 50%;
                            box-shadow: 0 5px 13px #2045d7;
                            &:after {
                                content: "";
                                width: 4px;
                                height: 4px;
                                background-color: #1dc7ff;
                                border-radius: 50%;
                                display: block;
                                margin: 4px auto;
                            }
                        }
                    }
                }
            }
        }
</style>
