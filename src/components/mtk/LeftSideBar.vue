<template>
        <div class="leftSideBar" :style="{'height': sidebarHeight + 'px' }">
            <div class="operation_panel layout" id="layout">
                <h3><span>所有布局</span></h3>
                <el-tabs v-model="left_tab_layout" class="tab_title">
                    <el-tab-pane label="一行" name="line_1">
                            <div class="tab_item" id="layout_iscroll_1">
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
                    </el-tab-pane>
                    <el-tab-pane label="二行" name="line_2">
                            <div class="tab_item" id="layout_iscroll_2">
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
                    </el-tab-pane>
                </el-tabs>
                <!-- <div class="tab_title"><a class="on" tab="0">一行</a><a tab="1">二行</a></div>
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
                </div> -->
            </div>
            <div class="operation_panel beauty" id="beauty">
                    <h3><span>美化</span></h3>
                    <el-tabs v-model="left_tab_beauty" class="tab_title">
                        <el-tab-pane label="外观" name="style">
                            <div class="tab_item" id="beauty_iscroll_1">
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
                                                        <el-select v-model="bgPosition" placeholder="请选择">
                                                            <el-option value="不重复">不重复</el-option>
                                                            <el-option value="水平方向重复">水平方向重复</el-option>
                                                            <el-option value="垂直方向重复">垂直方向重复</el-option>
                                                            <el-option value="填充">填充</el-option>
                                                        </el-select>
                                                        <input type="hidden" value="不重复">
                                                    </div>
                                                </div>
                                        </div>
                                        <el-button type="primary" class="preservation_but">保存</el-button>
                                        <!-- <div class="preservation_but"><a>保存</a></div> -->
                                </div>
                            </div>
                        </el-tab-pane>
                        <el-tab-pane label="推荐" name="recommend">
                                <div class="tab_item" id="beauty_iscroll_2">
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
                        </el-tab-pane>
                    </el-tabs>
            </div>
        </div>
</template>
<script>
    export default {
        name: 'LeftSideBar',
        props: ['sidebarHeight'],
        data() {
            return {
                bgPosition: '',
                left_tab_beauty: 'style',
                left_tab_layout: 'line_1',
            }
        },
        mounted() {
            var beauty_iscroll_1 = new IScroll('#beauty_iscroll_1', { mouseWheel: true });
            var beauty_iscroll_2 = new IScroll('#beauty_iscroll_2', { mouseWheel: true });
            var layout_iscroll_1 = new IScroll('#layout_iscroll_1', { mouseWheel: true });
            var layout_iscroll_2 = new IScroll('#layout_iscroll_2', { mouseWheel: true });
        },
    }
</script>
<style lang="scss">
    @import '../../assets/scss/base.scss';
    .leon-frame {
        .leftSideBar {
            position: fixed;
            left: -220px;
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
            .beauty {
                .tab_item {
                    height: 750px;
                    float: left;
                    position: relative;
                    margin-right: 20px;
                    width: 192px;
                    overflow: hidden;
                    .main_vice {
                        li {
                            margin-top:10px;
                            &:first-child {
                                margin-top: 0;
                            }
                            .on {
                                background-color:#182839;
                               .color_checked {
                                   i {
                                       color:#2fa0ff;
                                       text-shadow:0 5px 13px #2045d7;
                                   }
                                }
                            }
                            label {
                                width:100%;
                                height:40px;
                                background-color:#3a4f63;
                                display:block;
                                cursor:pointer;
                                &:hover {
                                    background-color:#1c2d41;
                                    &:before {
                                        animation: hovercolor 0.8s;
                                        -moz-animation: hovercolor 0.8s; /* Firefox */
                                        -webkit-animation: hovercolor 0.8s;  /* Safari 和 Chrome */
                                        -o-animation: hovercolor 0.8s;   /* Opera */
                                        -webkit-animation-fill-mode:forwards;
                                    }
                                }
                                &:before {
                                    content:"";
                                    width:10px;
                                    height:40px;
                                    background:url("../../../static/images/color_hover_img.png") no-repeat;
                                    float:left;
                                    margin-left:-10px;
                                }
                                input {
                                    -khtml-opacity:0;
                                    -moz-opacity:0;
                                    filter:alpha(opacity=0);
                                    opacity:0; 
                                    filter: progid:DXImageTransform.Microsoft.Alpha(opacity=0);/*兼容ie8及以下*/
                                }
                                .color_block {
                                    float:left;
                                    margin:10px 0;
                                    span {
                                        width:18px;
                                        height:18px;
                                        border:1px solid #fff;
                                        float:left;
                                        margin-left:10px;
                                    }
                                }
                                .color_checked {
                                    float:right;
                                    margin:9px 10px 9px 0;
                                    em {
                                        color:#3b8efe;
                                        float:left;
                                    }
                                    i {
                                        color:#617d98;
                                        font-size:20px;
                                        margin-left:10px;
                                    }
                                }
                            }
                        }
                    }
                }
            }
        }
    }
</style>
