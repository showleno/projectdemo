<template>
        <div class="leftSideBar" :style="{'height': sidebarHeight + 'px' }">
            <div class="operation_panel layout" id="layout">
                <h3><span>所有布局</span></h3>
                <div class="tab_title"><a class="on" tab="0">一行</a><a tab="1">二行</a></div>
                <div class="tab_con">
                    <div class="tab_item">
                        <div class="tab_inner">
                                <ul>
                                    <li data-layout-type="line_1_0">
                                        <table>
                                            <tr><td class="proportion c_c4ddff"></td></tr>
                                        </table>
                                        <p><span><i class="fa fa-plus"></i></span></p>
                                    </li>
                                    <li	data-layout-type="line_1_1" >
                                        <table>
                                            <tr><td class="proportion_2_1 c_75b0fe"></td><td class="proportion_2_2 c_c4ddff"></td></tr>
                                        </table>
                                        <p><span><i class="fa fa-plus"></i></span></p>
                                    </li>
                                    <li  data-layout-type="line_1_2">
                                        <table>
                                            <tr><td class="proportion_3_1 c_c4ddff"></td><td class="proportion_3_2 c_75b0fe"></td><td class="proportion_3_3 c_c4ddff"></td></tr>
                                        </table>
                                        <p><span><i class="fa fa-plus"></i></span></p>
                                    </li>
                                    <li data-layout-type="line_1_3">
                                        <table>
                                            <tr><td class="proportion_4_1 c_c4ddff"></td><td class="proportion_4_2 c_75b0fe"></td><td class="proportion_4_3 c_c4ddff"></td></tr>
                                        </table>
                                        <p><span><i class="fa fa-plus"></i></span></p>
                                    </li>
                                    <li data-layout-type="line_1_4">
                                        <table>
                                            <tr><td class="proportion_5_1 c_75b0fe"></td><td class="proportion_5_2 c_c4ddff"></td></tr>
                                        </table>
                                        <p><span><i class="fa fa-plus"></i></span></p>
                                    </li>
                                    <li data-layout-type="line_1_5">
                                        <table>
                                            <tr><td class="proportion_6_1 c_75b0fe"></td><td class="proportion_6_2 c_c4ddff"></td></tr>
                                        </table>
                                        <p><span><i class="fa fa-plus"></i></span></p>
                                    </li>
                                </ul>
                        </div>
                    </div>
                    <div class="tab_item">
                        <div class="tab_inner">
                                <ul>
                                        <li class="typesetting_alert" data-layout-type="#line_2_one">
                                            <table>
                                                <tr><td class="proportion_2_1 c_75b0fe"></td><td class="proportion_2_2 c_c4ddff"></td></tr>
                                                <tr><td class="proportion_2_1 c_75b0fe borTop10"></td><td class="proportion_2_2 c_c4ddff borTop10"></td></tr>
                                            </table>
                                            <p><span><i class="fa fa-plus"></i></span></p>
                                        </li>
                                        <li class="typesetting_alert" data-layout-type="#line_2_two">
                                            <table>
                                                <tr>
                                                    <td class="proportion_4_1 c_c4ddff" rowspan="2"></td>
                                                    <td class="proportion_4_2 c_75b0fe" rowspan="2"></td>
                                                    <td class="proportion_4_3 c_c4ddff"></td>
                                                </tr>
                                                <tr>
                                                    <td class="proportion_4_3 c_c4ddff borTop10"></td>
                                                </tr>
                                            </table>
                                            <p><span><i class="fa fa-plus"></i></span></p>
                                        </li>
                                        <li class="typesetting_alert" data-layout-type="#line_2_three">
                                            <table>
                                                <tr><td class="proportion_5_1 c_c4ddff" rowspan="2"></td><td class="proportion_5_2 c_75b0fe"></td></tr>
                                                <tr><td class="proportion_5_2 c_75b0fe borTop10"></td></tr>
                                            </table>
                                            <p><span><i class="fa fa-plus"></i></span></p>
                                        </li>
                                </ul>
                        </div>
                    </div>
                </div>
            </div>
            <div class="operation_panel beauty" id="beauty">
                    <h3><span>美化</span></h3>
                    <div class="tab_title"><a class="on" tab="0">外观</a><a tab="1">推荐</a></div>
                    <div class="tab_con">
                            <div class="tab_item">
                                <div class="tab_inner">
                                        <div id="picker" class="picker"></div>
                                        <div class="change_color">
                                            <strong><em>主色</em></strong>
                                            <p><input type="text" value="" class="colorwell color_radio_0"></p>
                                        </div>
                                        <div class="change_color">
                                            <strong><em>副色</em></strong>
                                            <p><input type="text" value="" class="colorwell color_radio_1"></p>
                                        </div>
                                        <div class="change_color column_upload">
                                                <div class="mini_tab"><a class="on">栏目背景</a><a>栏目背景图</a></div>
                                                <div class="mini_tab_item"><p><input type="text" value=""  class="colorwell color_radio_2"></p></div>
                                                <div class="mini_tab_item bgImg_set">
                                                    <div class="up_img clearfix">
                                                        <div class="show_img left"><i class="fa fa-camera"></i></div>
                                                        <div class="up_but left">
                                                            <label><a  class="upload"><i class="fa fa-camera"></i>上传<input type="file" name="filename" accept="image/gif,image/jpeg,image/jpg,image/png"></a></label><a class="eliminate"><i class="fa fa-times"></i>清除</a></div>
                                                    </div>
                                                    <div class="bg_position">
                                                        <h3><span>背景位置</span></h3>
                                                        <div class="location_sele clearfix">
                                                            <a class="posi_top on"><em></em><input type="radio" name="bj_img_posi" ></a>
                                                            <a class="posi_middle"><em></em><input type="radio" name="bj_img_posi" checked></a>
                                                            <a class="posi_bottom"><em></em><input type="radio" name="bj_img_posi"></a>
                                                        </div>
                                                    </div>
                                                    <div class="repeat">
                                                        <el-select v-model="bgPosition" placeholder="请选择">
                                                            <el-option value="不重复">不重复</el-option>
                                                            <el-option value="水平方向重复">水平方向重复</el-option>
                                                            <el-option value="垂直方向重复">垂直方向重复</el-option>
                                                            <el-option value="填充">填充</el-option>
                                                        </el-select>
                                                        <!-- <span><em>不重复</em><i class="fa fa-sort-down"></i></span>
                                                        <ul>
                                                            <li><a class="repeat_btn" data-repeat="no-repeat">不重复</a></li>
                                                            <li><a class="repeat_btn" data-repeat="repeat-x">水平方向重复</a></li>
                                                            <li><a class="repeat_btn" data-repeat="repeat-y">垂直方向重复</a></li>
                                                            <li><a class="repeat_btn" data-repeat="repeat">填充</a></li>
                                                        </ul> -->
                                                        <input type="hidden" value="不重复">
                                                    </div>
                                                </div>
                                        </div>
                                        <div class="change_color">
                                            <strong><em>栏目文字</em></strong>
                                            <p><input type="text" value="" class="colorwell color_radio_3"></p>
                                        </div>
                                        <div class="change_color nav_upload">
                                                <div class="mini_tab"><a class="on">背景颜色</a><a>背景图片</a></div>
                                                <div class="mini_tab_item"><p><input type="text" value=""  class="colorwell color_radio_2"></p></div>
                                                <div class="mini_tab_item bgImg_set">
                                                    <div class="up_img clearfix">
                                                        <div class="show_img left"><i class="fa fa-camera"></i></div>
                                                        <div class="up_but left"><label><a  class="upload"><i class="fa fa-camera"></i>上传<input type="file" name="filename" accept="image/gif,image/jpeg,image/jpg,image/png"></a></label><a class="eliminate"><i class="fa fa-times"></i>清除</a></div>
                                                    </div>
                                                    <div class="bg_position">
                                                        <h3><span>背景位置</span></h3>
                                                        <div class="location_sele clearfix">
                                                            <a class="posi_top on"><em></em><input type="radio" name="bj_img_posi" ></a>
                                                            <a class="posi_middle"><em></em><input type="radio" name="bj_img_posi" checked></a>
                                                            <a class="posi_bottom"><em></em><input type="radio" name="bj_img_posi"></a>
                                                        </div>
                                                    </div>
                                                    <div class="repeat">
                                                        <span><em>不重复</em><i class="fa fa-sort-down"></i></span>
                                                        <ul>
                                                            <li><a class="repeat_btn" data-repeat="no-repeat">不重复</a></li>
                                                            <li><a class="repeat_btn" data-repeat="repeat-x">水平方向重复</a></li>
                                                            <li><a class="repeat_btn" data-repeat="repeat-y">垂直方向重复</a></li>
                                                            <li><a class="repeat_btn" data-repeat="repeat">填充</a></li>
                                                        </ul>
                                                        <input type="hidden" value="不重复">
                                                    </div>
                                                </div>
                                        </div>
                                        <div class="preservation_but"><a>保存</a></div>
                                </div>
                            </div>
                            <div class="tab_item">
                                <div class="tab_inner">
                                    <div class="main_vice">
                                        <ul>
                                            <li>
                                                <label class="on" frontView="#2b2e4a" backgroundColor="#903749">
                                                    <div class="color_block">
                                                        <span class="c_2b2e4a"></span>
                                                        <span class="c_903749"></span>
                                                    </div>
                                                    <div class="color_checked">
                                                        <em>使用中</em>
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                    <input type="radio" name="color_sel" checked>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#38817a" backgroundColor="#56bfb5">
                                                    <div class="color_block">
                                                        <span class="c_38817a"></span>
                                                        <span class="c_56bfb5"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#484cb0" backgroundColor="#526ed0">
                                                    <div class="color_block">
                                                        <span class="c_484cb0"></span>
                                                        <span class="c_526ed0"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#655989" backgroundColor="#de88a5">
                                                    <div class="color_block">
                                                        <span class="c_655989"></span>
                                                        <span class="c_de88a5"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#222831" backgroundColor="#393e46">
                                                    <div class="color_block">
                                                        <span class="c_222831"></span>
                                                        <span class="c_393e46"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#5e1043" backgroundColor="#a13f80">
                                                    <div class="color_block">
                                                        <span class="c_5e1043"></span>
                                                        <span class="c_a13f80"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#c83b4c" backgroundColor="#f75b5b">
                                                    <div class="color_block">
                                                        <span class="c_c83b4c"></span>
                                                        <span class="c_f75b5b"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#1a2634" backgroundColor="#203e5f">
                                                    <div class="color_block">
                                                        <span class="c_1a2634"></span>
                                                        <span class="c_203e5f"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#b42b3f" backgroundColor="#e42f45">
                                                    <div class="color_block">
                                                        <span class="c_b42b3f"></span>
                                                        <span class="c_e42f45"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#a66d53" backgroundColor="#c98c70">
                                                    <div class="color_block">
                                                        <span class="c_a66d53"></span>
                                                        <span class="c_c98c70"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#3f4c48" backgroundColor="#95977a">
                                                    <div class="color_block">
                                                        <span class="c_3f4c48"></span>
                                                        <span class="c_95977a"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#062c80" backgroundColor="#0e6ac7">
                                                    <div class="color_block">
                                                        <span class="c_062c80"></span>
                                                        <span class="c_0e6ac7"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#46265c" backgroundColor="#794d9a">
                                                    <div class="color_block">
                                                        <span class="c_46265c"></span>
                                                        <span class="c_794d9a"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#543d46" backgroundColor="#5da7ae">
                                                    <div class="color_block">
                                                        <span class="c_543d46"></span>
                                                        <span class="c_5da7ae"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#8d0033" backgroundColor="#bd3246">
                                                    <div class="color_block">
                                                        <span class="c_8d0033"></span>
                                                        <span class="c_bd3246"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#2f2342" backgroundColor="#e42f45">
                                                    <div class="color_block">
                                                        <span class="c_2f2342"></span>
                                                        <span class="c_e42f45"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#6f3826" backgroundColor="#b84a39">
                                                    <div class="color_block">
                                                        <span class="c_6f3826"></span>
                                                        <span class="c_b84a39"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#333a7b" backgroundColor="#4b6982">
                                                    <div class="color_block">
                                                        <span class="c_333a7b"></span>
                                                        <span class="c_4b6982"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#266352" backgroundColor="#128061">
                                                    <div class="color_block">
                                                        <span class="c_266352"></span>
                                                        <span class="c_128061"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#0c3c78" backgroundColor="#04879c">
                                                    <div class="color_block">
                                                        <span class="c_0c3c78"></span>
                                                        <span class="c_04879c"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#0066cc" backgroundColor="#0099ff">
                                                    <div class="color_block">
                                                        <span class="c_0066cc"></span>
                                                        <span class="c_0099ff"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#634258" backgroundColor="#6d6087">
                                                    <div class="color_block">
                                                        <span class="c_634258"></span>
                                                        <span class="c_6d6087"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#314357" backgroundColor="#456672">
                                                    <div class="color_block">
                                                        <span class="c_314357"></span>
                                                        <span class="c_456672"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#083d56" backgroundColor="#0e5f76">
                                                    <div class="color_block">
                                                        <span class="c_083d56"></span>
                                                        <span class="c_0e5f76"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#303242" backgroundColor="#394359">
                                                    <div class="color_block">
                                                        <span class="c_303242"></span>
                                                        <span class="c_394359"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#504077" backgroundColor="#924992">
                                                    <div class="color_block">
                                                        <span class="c_504077"></span>
                                                        <span class="c_924992"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>
                                            <li>
                                                <label frontView="#cd4439" backgroundColor="#72b896">
                                                    <div class="color_block">
                                                        <span class="c_cd4439"></span>
                                                        <span class="c_72b896"></span>
                                                    </div>
                                                    <input type="radio" name="color_sel">
                                                    <div class="color_checked">
                                                        <i class="fa fa-check-circle"></i>
                                                    </div>
                                                </label>
                                            </li>

                                        </ul>
                                    </div>
                                </div>
                            </div>
                    </div>
            </div>
        </div>
</template>
<script>
    export default {
        name: 'LeftSideBar',
        props: ['sidebarHeight'],
        data() {
            return {
                bgPosition: ''
            }
        }
    }
</script>
<style lang="scss">
    @import '../../assets/scss/base.scss';
    .leon-frame {
        .leftSideBar {
            position: fixed;
            left: 100px;
            top: 70px;
            background-color: #283c50;
            overflow: hidden;
            z-index: 15;
            .c_c4ddff {
                background-color: #c4ddff;
            }
            .c_75b0fe {
                background-color: #75b0fe;
            }
            .layout {
                display: none;
                .tab_con {
                    .tab_item {
                        li {
                            position: relative;
                            margin-bottom: 30px;
                            border-radius: 4px;
                            border: 3px solid #fff;
                            cursor: pointer;
                            p {
                                position:absolute;
                                bottom:0;
                                left:50%;
                                display:none;
                                background:url("data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyJpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMy1jMDExIDY2LjE0NTY2MSwgMjAxMi8wMi8wNi0xNDo1NjoyNyAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNiAoV2luZG93cykiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6NDJERTU4RDlEOTlBMTFFNzkyMzlDRDk1Q0EzRTlDMkYiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6NDJERTU4REFEOTlBMTFFNzkyMzlDRDk1Q0EzRTlDMkYiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDo0MkRFNThEN0Q5OUExMUU3OTIzOUNEOTVDQTNFOUMyRiIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDo0MkRFNThEOEQ5OUExMUU3OTIzOUNEOTVDQTNFOUMyRiIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/Pq5lqG0AAAAPSURBVHjaYmBgYDAGCDAAADgANJK9jDAAAAAASUVORK5CYII=");
                                margin-left:-18px;
                                margin-bottom:-18px;
                                padding:3px;
                                border-radius:50%;
                                span {
                                    line-height:30px;
                                    display:block;
                                    width:30px;
                                    height:30px;
                                    border-radius:50%;
                                    color:#ff422c;
                                    font-size:18px;
                                    text-align:center;
                                    background-color:#fff;
                                }
                            }
                            &:hover {
                                border-color: #0e61db;
                                box-shadow: 0 0 18px #0e61db;
                                p {
                                    display: block;
                                }
                            }
                        }
                        table {
                            width:100%;
                            height:77px;
                            border:7px solid #fff;
                            border-collapse: collapse;
                            border-spacing: 0;
                             .proportion_2_1 {
                                 width: 110px;
                             }
                              .proportion_2_2 {
                                  border-left:10px solid #fff;
                              }
                              .proportion_3_1, 
                              .proportion_3_2, 
                              .proportion_3_3 {
                                  width:46px;
                              }
                              .proportion_3_2,
                              .proportion_4_2 {
                                  border-left:11px solid #fff;
                                 border-right:11px solid #fff;
                              }
                              .proportion_4_1 {
                                  width:40px;
                              }
                              .proportion_5_1,
                              .proportion_5_2 {
                                  width:75px;
                              }
                              .proportion_5_2 {
                                  border-left:11px solid #fff;
                              }
                              .proportion_6_1 {
                                  width:120px;
                              }
                              .proportion_6_2 {
                                  width:30px;
                                  border-left:10px solid #fff;
                              }
                              .proportion_7_1 {
                                  width: 40px;
                              }
                              .proportion_7_2 {
                                 width:98px;
                                 border-left:10px solid #fff;
                              }
                        }
                    }
                }
            }
            .beauty {
                .tab_con {
                    .tab_item {
                        float: left;
                        position: relative;
                        margin-right: 20px;
                        width: 192px;
                        overflow-x: hidden;
                        .picker {
                            display: none;
                            height: 180px;
                            margin-bottom: 20px;
                        }
                        .change_color {
                            margin-bottom: 20px;
                            strong {
                                background-color: #142336;
                                font-size: 14px;
                                font-weight: normal;
                                width: 90px;
                                display: block;
                                padding-left: 20px;
                                position: relative;
                                padding-top: 6px;
                                em {
                                    position: relative;
                                    bottom: -2px;
                                    color: #fff;
                                }
                                &:after {
                                        content: "";
                                        width: 10px;
                                        height: 26px;
                                        display: block;
                                        background-image: url('../../../static/images/pic.png');
                                        background-repeat: no-repeat;
                                        background-size: 10px 26px;
                                        position: absolute;
                                        right: -10px;
                                        top: 0;
                                }
                            }
                            p {
                                background-color: #142336;
                                text-align: center;
                                padding: 10px 0;
                                input {
                                    text-align: center;
                                    height: 28px;
                                    line-height: 28px;
                                    width: 170px;
                                    border: 1px solid #171a1f;
                                }
                            }
                        }
                        .bgImg_set {
                            padding: 0 10px 10px;
                            .up_img {
                                height: 80px;
                                padding-bottom: 10px;
                                .show_img {
                                    width: 76px;
                                    height: 76px;
                                    border: 2px solid #0066ff;
                                    background-color: #fff;
                                    border-radius: 5px;
                                    text-align: center;
                                    line-height: 76px;
                                    position: relative;
                                    i.fa {
                                        color: #ccc;
                                        font-size: 36px;
                                        position: absolute;
                                        left: 50%;
                                        top: 50%;
                                        margin: -18px 0 0 -19px;
                                    }
                                    .img {
                                        width: 100%;
                                        max-width: 100%;
                                    }
                                }
                                .up_but {
                                    margin-left: 10px;
                                    a {
                                        display: block;
                                        width: 82px;
                                        height: 35px;
                                        line-height: 35px;
                                        color: #fff;
                                        text-align: center;
                                        border-radius: 3px;
                                        &.upload {
                                            background: url(../../../static/images/bj_b.jpg);
                                            position: relative;
                                            input[type=file] {
                                                position: absolute;
                                                top: 0;
                                                left: 0;
                                                width: 100%;
                                                height: 100%;
                                                z-index: -1;
                                                font-size: 0;
                                                filter: progid:DXImageTransform.Microsoft.Alpha(opacity=0);
                                                -khtml-opacity: 0;
                                                -moz-opacity: 0;
                                                filter: alpha(opacity=0);
                                                opacity: 0;
                                            }
                                        }
                                        i.fa {
                                            margin-right: 4px;
                                        }
                                        &.eliminate {
                                            background: #3a4f63;
                                            margin-top: 10px;
                                        }
                                    }
                                }
                            }
                            .bg_position {
                                margin-bottom: 20px;
                                > h3 {
                                    line-height: 30px;
                                    text-align: center;
                                    font-size: 14px;
                                    font-weight: normal;
                                    position: relative;
                                    span {
                                        position: relative;
                                        z-index: 10;
                                        background-color: #142336;
                                        padding: 0px 14px;
                                        color:#444;
                                    }
                                    &:after {
                                        content: "";
                                        width: 100%;
                                        height: 2px;
                                        position: absolute;
                                        top: 16px;
                                        left: 0;
                                        background: url('data:image/jpeg;base64,/9j/4QAYRXhpZgAASUkqAAgAAAAAAAAAAAAAAP/sABFEdWNreQABAAQAAABkAAD/4QMraHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLwA8P3hwYWNrZXQgYmVnaW49Iu+7vyIgaWQ9Ilc1TTBNcENlaGlIenJlU3pOVGN6a2M5ZCI/PiA8eDp4bXBtZXRhIHhtbG5zOng9ImFkb2JlOm5zOm1ldGEvIiB4OnhtcHRrPSJBZG9iZSBYTVAgQ29yZSA1LjMtYzAxMSA2Ni4xNDU2NjEsIDIwMTIvMDIvMDYtMTQ6NTY6MjcgICAgICAgICI+IDxyZGY6UkRGIHhtbG5zOnJkZj0iaHR0cDovL3d3dy53My5vcmcvMTk5OS8wMi8yMi1yZGYtc3ludGF4LW5zIyI+IDxyZGY6RGVzY3JpcHRpb24gcmRmOmFib3V0PSIiIHhtbG5zOnhtcD0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLyIgeG1sbnM6eG1wTU09Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9tbS8iIHhtbG5zOnN0UmVmPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvc1R5cGUvUmVzb3VyY2VSZWYjIiB4bXA6Q3JlYXRvclRvb2w9IkFkb2JlIFBob3Rvc2hvcCBDUzYgKFdpbmRvd3MpIiB4bXBNTTpJbnN0YW5jZUlEPSJ4bXAuaWlkOkU0NTdGRjlCRTBBQjExRTc5MzI2OUJCRjJEMUVFQUM3IiB4bXBNTTpEb2N1bWVudElEPSJ4bXAuZGlkOkU0NTdGRjlDRTBBQjExRTc5MzI2OUJCRjJEMUVFQUM3Ij4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6RTQ1N0ZGOTlFMEFCMTFFNzkzMjY5QkJGMkQxRUVBQzciIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6RTQ1N0ZGOUFFMEFCMTFFNzkzMjY5QkJGMkQxRUVBQzciLz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz7/7gAOQWRvYmUAZMAAAAAB/9sAhAABAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAgICAgICAgICAgIDAwMDAwMDAwMDAQEBAQEBAQIBAQICAgECAgMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwP/wAARCAACAAEDAREAAhEBAxEB/8QATAABAAAAAAAAAAAAAAAAAAAACgEBAAAAAAAAAAAAAAAAAAAABhABAQAAAAAAAAAAAAAAAAAAAJkRAQEAAAAAAAAAAAAAAAAAAACV/9oADAMBAAIRAxEAPwAldLDa2HR3/9k=');
                                    }
                                }
                                .location_sele {
                                    height: 30px;
                                    a {
                                        @include boxSizing();
                                        overflow: hidden;
                                        float:left;
                                        width:20%;
                                        height:28px;
                                        border:2px solid #0066ff;
                                        margin-left:20%;
                                        border-radius:5px;
                                        text-align:center;
                                        background-color:#fff;
                                        position:relative;
                                        cursor: pointer;
                                        em {
                                                width: 20px;
                                                height: 20px;
                                                background-image: url(../../../static/images/bj_b.jpg);
                                                display: inline-block;
                                                background-size: 100%;
                                                filter: progid:DXImageTransform.Microsoft.AlphaImageLoader( src='../../newpc/images/bj_b.jpg', sizingMethod='scale');
                                                -ms-filter: progid:DXImageTransform.Microsoft.AlphaImageLoader( src='../../newpc/images/bj_b.jpg', sizingMethod='scale');
                                        }
                                        input {
                                            position: absolute;
                                            top: 0;
                                            left: 0;
                                            width: 100%;
                                            height: 100%;
                                            -khtml-opacity: 0;
                                            -moz-opacity: 0;
                                            filter: alpha(opacity=0);
                                            opacity: 0;
                                            filter: progid:DXImageTransform.Microsoft.Alpha(opacity=0);
                                        }
                                        &:first-child {
                                            margin-left:0;
                                        }
                                        &:hover , &.on {
                                            border-color:#f75b5b;
                                        }
                                    }
                                    .posi_middle {
                                        em {
                                            margin:2px 0;
                                        }
                                    }
                                    .posi_bottom {
                                        em {
                                            margin-top:8px;
                                        }
                                    }
                                }
                            }
                        }
                        .column_upload, .nav_upload {
                            background-color: #142336;
                        }
                        .mini_tab {
                            height: 40px;
                            a {
                                float: left;
                                width: 50%;
                                line-height: 40px;
                                text-align: center;
                                color: #fff;
                                position: relative;
                                &.on {
                                    color: #3b8efe;
                                    &:before {
                                        content: "";
                                        width: 100%;
                                        height: 2px;
                                        background-color: #0066ff;
                                        position: absolute;
                                        top: 0;
                                        left: 0;
                                    }
                                }
                                &:first-child:after {
                                    content:"";
                                    width:2px;
                                    height:13px;
                                    position:absolute;
                                    right:0;
                                    top:50%;
                                    margin-top:-6px;
                                    background:url("data:image/jpeg;base64,/9j/4QAYRXhpZgAASUkqAAgAAAAAAAAAAAAAAP/sABFEdWNreQABAAQAAABkAAD/4QMraHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLwA8P3hwYWNrZXQgYmVnaW49Iu+7vyIgaWQ9Ilc1TTBNcENlaGlIenJlU3pOVGN6a2M5ZCI/PiA8eDp4bXBtZXRhIHhtbG5zOng9ImFkb2JlOm5zOm1ldGEvIiB4OnhtcHRrPSJBZG9iZSBYTVAgQ29yZSA1LjMtYzAxMSA2Ni4xNDU2NjEsIDIwMTIvMDIvMDYtMTQ6NTY6MjcgICAgICAgICI+IDxyZGY6UkRGIHhtbG5zOnJkZj0iaHR0cDovL3d3dy53My5vcmcvMTk5OS8wMi8yMi1yZGYtc3ludGF4LW5zIyI+IDxyZGY6RGVzY3JpcHRpb24gcmRmOmFib3V0PSIiIHhtbG5zOnhtcD0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLyIgeG1sbnM6eG1wTU09Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9tbS8iIHhtbG5zOnN0UmVmPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvc1R5cGUvUmVzb3VyY2VSZWYjIiB4bXA6Q3JlYXRvclRvb2w9IkFkb2JlIFBob3Rvc2hvcCBDUzYgKFdpbmRvd3MpIiB4bXBNTTpJbnN0YW5jZUlEPSJ4bXAuaWlkOjJFNjE3NjJGREJERjExRTdBNDVFQjIwNzIxMzdCRkEzIiB4bXBNTTpEb2N1bWVudElEPSJ4bXAuZGlkOjJFNjE3NjMwREJERjExRTdBNDVFQjIwNzIxMzdCRkEzIj4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9InhtcC5paWQ6MkU2MTc2MkREQkRGMTFFN0E0NUVCMjA3MjEzN0JGQTMiIHN0UmVmOmRvY3VtZW50SUQ9InhtcC5kaWQ6MkU2MTc2MkVEQkRGMTFFN0E0NUVCMjA3MjEzN0JGQTMiLz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz7/7gAOQWRvYmUAZMAAAAAB/9sAhAABAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAgICAgICAgICAgIDAwMDAwMDAwMDAQEBAQEBAQIBAQICAgECAgMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwMDAwP/wAARCAABAAIDAREAAhEBAxEB/8QATAABAAAAAAAAAAAAAAAAAAAACgEBAAAAAAAAAAAAAAAAAAAABhABAQAAAAAAAAAAAAAAAAAAANkRAQEAAAAAAAAAAAAAAAAAAADV/9oADAMBAAIRAxEAPwAldLDa2HR3/9k=");
                                }
                                &:hover {
                                    text-decoration: underline;
                                }
                            }
                        }
                    }
                }
            }
        }
    }
</style>
