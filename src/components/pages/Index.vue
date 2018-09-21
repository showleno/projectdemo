<template>
    <div class="index">
            <div class="top">
                <div class="inner edit clearfix">
                        <div class="top_line right clearfix">
                            <div class="my_admin left clearfix">
                                <div class="user_name left">
                                    <span>
                                        <i class="fa fa-user"></i>
                                    </span>
                                    <p class="top_font_color" style="color:">admin</p>
                                </div>
                                <div class="personal_center left">
                                    <a class="top_font_color" style="color:">个人中心
                                        <i class="fa fa-angle-down" style="color:"></i>
                                    </a>
                                    <div class="down_con" style="display: none;">
                                        <ul class="clearfix">
                                            <li>
                                                <a href="">我的社团</a>
                                            </li>
                                            <li>
                                                <a href="">我的帮帮忙</a>
                                            </li>
                                            <li>
                                                <a href="">消息中心</a>
                                            </li>
                                            <li>
                                                <a href="">我的文库</a>
                                            </li>
                                            <li>
                                                <a href="">个人资料</a>
                                            </li>
                                            <li>
                                                <a href="">我的问卷</a>
                                            </li>
                                            <li>
                                                <a href="">我的资源</a>
                                            </li>
                                            <li>
                                                <a href="">我的期刊</a>
                                            </li>
                                            <li>
                                                <a href="">我的圈子</a>
                                            </li>
                                            <li>
                                                <a href="">修改密码</a>
                                            </li>
                                            <li>
                                                <a href="">我的活动</a>
                                            </li>
                                            <li>
                                                <a href="">退出</a>
                                            </li>
                                        </ul>
                                        <i class="blank"></i>
                                    </div>
                                </div>
                                <div class="admin_renovation left">
                                    <a href="" class="top_font_color" style="color:">管理社团</a>
                                    <a href="" class="top_font_color" style="color:">网站装修</a>
                                </div>
                            </div>
                            <div class="top_search left">
                                <form action="" class="clearfix">
                                    <input type="text" placeholder="输入关键词">
                                    <a class="deputy_bg_color" style="background-color:;color:#fff;">
                                        <i class="fa fa-search"></i>
                                    </a>
                                </form>
                            </div>
                            <div class="login left">
                                <a class="deputy_bg_color top_btn_bg" style="background-color:;color:#fff;">登录</a>
                                <a class="deputy_bg_color top_btn_bg" style="background-color:;color:#fff;">注册</a>
                            </div>
                        </div>
                </div>
            </div>
    </div>
</template>
<script>
    export default {
        name: 'Index'
    }
</script>
<style lang="scss">
    .leon-frame {
        .top {
            .my_admin {
                line-height: 30px;
                .user_name {
                    span {
                        width:30px;
                        height:30px;
                        border-radius:50%;
                        border:1px solid #cdcdcd;
                        color:#999;
                        font-size:18px;
                        text-align:center;
                        overflow:hidden;
                    }
                    p {
                        margin-left: 8px;
                    }
                }
                .admin_renovation {
                    a {
                         padding: 0 12px;
                        position: relative;
                        &:before {
                            content: "";
                            width: 1px;
                            height: 12px;
                            background-color: #999;
                            position: absolute;
                            left: 0;
                            top: 4px;
                        }
                    }
                }
                .personal_center {
                    padding: 0 10px;
                    position: relative;
                    a {
                        i.fa {
                            margin-left: 6px;
                        }
                    }
                    .down_con {
                         position: absolute;
                        top: 30px;
                        left: -55px;
                        z-index: 12;
                        padding-top: 6px;
                        display: none;
                        ul {
                            width: 196px;
                            border: 1px solid #ccc;
                            overflow: hidden;
                            background-color: #fff;
                            li {
                                float: left;
                                width: 98px;
                                border-bottom: 1px solid #eee;
                                 a {
                                     display: block;
                                    padding-left: 14px;
                                    &:hover {
                                        background-color: #eee;
                                        color: #000;
                                        font-weight: bold;
                                    }
                                 }
                            }
                            i.blank {
                                 display: block;
                                width: 10px;
                                height: 6px;
                                position: absolute;
                                top: 1px;
                                left: 50%;
                                margin-left: -5px;
                                background: url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAoAAAAGCAYAAAD68A/GAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyJpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMy1jMDExIDY2LjE0NTY2MSwgMjAxMi8wMi8wNi0xNDo1NjoyNyAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNiAoV2luZG93cykiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6RjA5QkVBRjNGOUQ5MTFFN0E3NDdBOUY0REIxQTcwRDMiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6RjA5QkVBRjRGOUQ5MTFFN0E3NDdBOUY0REIxQTcwRDMiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDpGMDlCRUFGMUY5RDkxMUU3QTc0N0E5RjREQjFBNzBEMyIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDpGMDlCRUFGMkY5RDkxMUU3QTc0N0E5RjREQjFBNzBEMyIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PrEzTzsAAABqSURBVHjadM1tCoAgDAZgRYnoQp4u6IMuJqJ4DK/hH9trG4TU4GUyn6lWT2npOecV3Tl38qxxOkIMoa2U0pAY40GziWJxJ9CklHaAWmsPziEEvDrzgrJvJCXYe3+RWRS+GNEn/kMjvgUYAK+XkFXf0HhHAAAAAElFTkSuQmCC") no-repeat;
                            }
                        }
                    }
                }
            }
            .top_search {
                input[type=text] {
                    border: 1px solid #ccc;
                    padding: 0 10px;
                    width: 108px;
                    height: 28px;
                    float: left;
                }
                a {
                    width: 30px;
                    height: 30px;
                    float: left;
                    text-align: center;
                    line-height: 30px;
                }
            }
            .login {
                a {
                    width: 60px;
                    height: 30px;
                    float: left;
                    text-align: center;
                    line-height: 30px;
                    margin-left: 10px;
                    &:first-child {
                        margin-left: 0;
                    }
                }
            }
        }
    }
</style>
