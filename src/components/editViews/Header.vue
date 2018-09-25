<template>
    <div class="header clearfix">
            <div class="left logo">
                    <img src="static/images/logo.png" alt="" />
            </div>
            <div class="header_btn clearfix">
                <div class="left table_tab">
                    <ul class="clearfix">
                        <li class="active"><a><i class="fa fa-laptop"></i>PC端</a></li>
                        <li><a><i class="fa fa-mobile"></i>手机端</a></li>
                    </ul>
                </div>
                <div class="left btn_group">
                    <ul class="clearfix">
                        <li><a><i class="fa fa-floppy-o"></i>保存</a></li>
                        <li><a><i class="fa fa-eye"></i>预览</a></li>
                        <li><a><i class="fa fa-refresh"></i>发布</a></li>
                    </ul>
                </div>
                <div class="right">
                    <el-button type="primary" class="exit_btn"><i class="fa fa-external-link"></i>退出</el-button>
                </div>
            </div>
    </div>
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style lang="scss">
    @import '../../assets/scss/base.scss';
    .leon-frame {
        .header {
            width: 100%;
            background-color: #142335;
            height: 70px;
            .logo {
                width: 166px;
                height: 70px;
            }
            .header_btn {
                width: 100%;
                height: 70px;
                @include boxSizing();
                padding: 20px 20px 20px 196px;
                .table_tab {
                    border: 1px solid #303e4c;
                    box-shadow: 0 5px 5px #182d66;
                    border-radius: 4px;
                    margin-right: 18px;
                    li {
                        float: left;
                        height: 28px;
                        line-height: 28px;
                        padding: 0 20px;
                        @include boxSizing();
                        border-right: 1px solid #303e4c;
                        text-align: center;
                        &:last-child {
                            border-right: 0;
                        }
                        &.active {
                            background-color: #303e4c;
                        }
                        a {
                            display: inline-block;
                            color: #fff;
                            position: relative;
                            top: -2px;
                            i.fa {
                                font-size: 25px;
                                position: relative;
                                top: 4px;
                                margin-right: 10px;
                                color: #357ff8;
                            }
                        }
                    }
                }
                .btn_group {
                    border: 1px solid #303e4c;
                    box-shadow: 0 5px 5px #182d66;
                    border-radius: 4px;
                    li {
                        float: left;
                        height: 28px;
                        line-height: 28px;
                        a {
                            color: #fff;
                            border-right: 1px solid #303e4c;
                            padding: 0 16px;
                            i.fa {
                                margin-right: 10px;
                                color: #357ff8;
                            }
                            &:hover {
                                text-decoration: underline;
                            }
                        }
                        &:last-child {
                            a {
                                border-right: 0;
                            }
                        }
                    }
                }
                .exit_btn {
                    background-color: #303e4f;
                    text-align: center;
                    height: 28px;
                    line-height: 28px;
                    padding: 0;
                    width: 90px;
                    border: 0;
                    &:hover {
                        text-decoration: underline;
                    }
                    i.fa {
                        margin-right: 10px;
                    }
                }
            }
        }
    }
</style>
