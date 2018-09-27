<template>
        <div class="rightSideBar" :style="{'height': sidebarHeight + 'px' }">
                <div class="operation_panel  right_number_0">
                        <h3><span>网站LOGO</span></h3>
                        <div class="tab_item">
                            <div class="tab_inner">
                                    <div class="mini_tab_item bgImg_set">
                                        <div class="up_img clearfix">
                                            <div class="show_img left"><i class="fa fa-camera"></i></div>
                                            <div class="up_but left">
                                                <label><a  class="upload"><i class="fa fa-camera"></i>上传<input type="file" name="filename" accept="image/gif,image/jpeg,image/jpg,image/png"></a></label>
                                                <a class="eliminate"><i class="fa fa-times"></i>清除</a>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="logo_size bgImg_set">
                                        <div class="modify_input clearfix"><p class="left">修改长度：</p><el-input v-model="logo_width" class="width input_text  left" placeholder="宽度(px)"></el-input></div>
                                        <div class="modify_input clearfix"><p class="left">修改高度：</p><el-input v-model="logo_height" class="height input_text left" placeholder="高度(px)"></el-input></div>
                                        <div class="modify_input clearfix">
                                            <p class="left">是否显示：</p>
                                            <div class="isShow left">
                                                <el-switch
                                                        v-model="logo_isShow"
                                                        active-color="#0c6eff"
                                                        inactive-color="#ccc"
                                                        >
                                                </el-switch>
                                                <input type="hidden" class="doesShow" value="">
                                            </div>
                                        </div>
                                    </div>
                            </div>
                            <el-button type="primary" class="preservation_but">保存</el-button>
                        </div>
                </div>
                <div class="operation_panel  right_number_1">
                        <h3><span>网站名称</span></h3>
                        <div class="tab_item">
                            <div class="tab_inner">
                                    <div id="picker2" class="picker"></div>
                                    <div class="change_color">
                                        <strong><em>主色</em></strong>
                                        <p><input type="text" value="" class="colorwell color_radio_0"></p>
                                    </div>
                                    <div class="logo_size bgImg_set">
                                        <div class="modify_input clearfix"><el-input v-model="webName" type="textarea" class="webName" placeholder="网站名称"></el-input></div>
                                        <div class="modify_input clearfix"><p class="left">大小：</p><el-slider  v-model="webName_size" class="webName_size slider_block left"></el-slider></div>
                                        <div class="modify_input clearfix">
                                                        <p class="left">字体：</p>
                                                        <el-select v-model="webName_font" class="webName_font left" placeholder="请选择">
                                                            <el-option value="微软雅黑">微软雅黑</el-option>
                                                            <el-option value="黑体">黑体</el-option>
                                                            <el-option value="宋体">宋体</el-option>
                                                        </el-select>
                                        </div>
                                        <div class="modify_input clearfix">
                                            <p class="left">显示：</p>
                                            <div class="isShow left">
                                                <el-switch
                                                        v-model="webName_isShow"
                                                        class="webName_isShow"
                                                        active-color="#0c6eff"
                                                        inactive-color="#ccc"
                                                        >
                                                </el-switch>
                                            </div>
                                        </div>
                                    </div>
                            </div>
                            <el-button type="primary" class="preservation_but">保存</el-button>
                        </div>
                </div>
                <div class="operation_panel  right_number_2">
                         <h3><span>设置抬头</span></h3>
                         <el-tabs v-model="right_tab_2" class="tab_title">
                              <el-tab-pane label="纯色" name="color">
                                  <div class="tab_item">
                                        <div class="tab_inner">
                                                <div id="picker3" class="picker"></div>
                                                <div class="change_color">
                                                    <strong><em>主色</em></strong>
                                                    <p><input type="text" value="" class="colorwell color_radio_0"></p>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">规格：</p>
                                                        <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                            <el-option value="宽屏">宽屏</el-option>
                                                            <el-option value="窄屏">窄屏</el-option>
                                                        </el-select>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">修改高度：</p>
                                                        <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">下边距(PX)：</p>
                                                        <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                    <p class="left">显示：</p>
                                                    <div class="isShow input_text left">
                                                        <el-switch
                                                                v-model="title_isShow"
                                                                active-color="#0c6eff"
                                                                inactive-color="#ccc"
                                                                >
                                                        </el-switch>
                                                    </div>
                                                </div>
                                                <el-button type="primary" class="preservation_but">保存</el-button>
                                        </div>
                                    </div>
                              </el-tab-pane>
                              <el-tab-pane label="图像" name="img">
                                    <div class="tab_item">
                                        <div class="tab_inner">
                                                <div class="mini_tab_item bgImg_set">
                                                    <div class="up_img clearfix">
                                                        <div class="show_img left"><i class="fa fa-camera"></i></div>
                                                        <div class="up_but left">
                                                            <label><a  class="upload"><i class="fa fa-camera"></i>上传<input type="file" name="filename" accept="image/gif,image/jpeg,image/jpg,image/png"></a></label>
                                                            <a class="eliminate"><i class="fa fa-times"></i>清除</a>
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="bg_position">
                                                    <h3><span>背景位置</span></h3>
                                                    <div class="location_sele clearfix">
                                                        <a class="posi_top on"><em></em><input type="radio" name="bj_img_posi" ></a>
                                                        <a class="posi_middle"><em></em><input type="radio" name="bj_img_posi" checked></a>
                                                        <a class="posi_bottom"><em></em><input type="radio" name="bj_img_posi"></a>
                                                    </div>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">规格：</p>
                                                        <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                            <el-option value="宽屏">宽屏</el-option>
                                                            <el-option value="窄屏">窄屏</el-option>
                                                        </el-select>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">修改高度：</p>
                                                        <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">下边距(PX)：</p>
                                                        <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                    <p class="left">显示：</p>
                                                    <div class="isShow input_text left">
                                                        <el-switch
                                                                v-model="title_isShow"
                                                                active-color="#0c6eff"
                                                                inactive-color="#ccc"
                                                                >
                                                        </el-switch>
                                                    </div>
                                                </div>
                                                <el-button type="primary" class="preservation_but">保存</el-button>
                                        </div>
                                    </div>
                              </el-tab-pane>
                         </el-tabs>
                        <!-- <div class="tab_title"><a class="on" tab="0">纯色</a><a tab="1">图像</a></div>
                        <div class="tab_con">
                            <div class="tab_item">
                                <div class="tab_inner">
                                        <div id="picker3" class="picker"></div>
                                        <div class="change_color">
                                            <strong><em>主色</em></strong>
                                            <p><input type="text" value="" class="colorwell color_radio_0"></p>
                                        </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">规格：</p>
                                                <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                    <el-option value="宽屏">宽屏</el-option>
                                                    <el-option value="窄屏">窄屏</el-option>
                                                </el-select>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">修改高度：</p>
                                                <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">下边距(PX)：</p>
                                                <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                         <div class="modify_input clearfix">
                                            <p class="left">显示：</p>
                                            <div class="isShow input_text left">
                                                <el-switch
                                                        v-model="title_isShow"
                                                        active-color="#0c6eff"
                                                        inactive-color="#ccc"
                                                        >
                                                </el-switch>
                                            </div>
                                        </div>
                                        <el-button type="primary" class="preservation_but">保存</el-button>
                                </div>
                            </div>
                            <div class="tab_item">
                                <div class="tab_inner">
                                        <div class="mini_tab_item bgImg_set">
                                            <div class="up_img clearfix">
                                                <div class="show_img left"><i class="fa fa-camera"></i></div>
                                                <div class="up_but left">
                                                    <label><a  class="upload"><i class="fa fa-camera"></i>上传<input type="file" name="filename" accept="image/gif,image/jpeg,image/jpg,image/png"></a></label>
                                                    <a class="eliminate"><i class="fa fa-times"></i>清除</a>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="bg_position">
                                            <h3><span>背景位置</span></h3>
                                            <div class="location_sele clearfix">
                                                <a class="posi_top on"><em></em><input type="radio" name="bj_img_posi" ></a>
                                                <a class="posi_middle"><em></em><input type="radio" name="bj_img_posi" checked></a>
                                                <a class="posi_bottom"><em></em><input type="radio" name="bj_img_posi"></a>
                                            </div>
                                        </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">规格：</p>
                                                <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                    <el-option value="宽屏">宽屏</el-option>
                                                    <el-option value="窄屏">窄屏</el-option>
                                                </el-select>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">修改高度：</p>
                                                <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">下边距(PX)：</p>
                                                <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                         <div class="modify_input clearfix">
                                            <p class="left">显示：</p>
                                            <div class="isShow input_text left">
                                                <el-switch
                                                        v-model="title_isShow"
                                                        active-color="#0c6eff"
                                                        inactive-color="#ccc"
                                                        >
                                                </el-switch>
                                            </div>
                                        </div>
                                        <el-button type="primary" class="preservation_but">保存</el-button>
                                </div>
                            </div>
                        </div> -->
                </div>
                <div class="operation_panel  right_number_3">
                         <h3><span>底部设置</span></h3>
                         <el-tabs v-model="right_tab_3" class="tab_title">
                             <el-tab-pane label="纯色" name="color">
                                 <div class="tab_item">
                                    <div class="tab_inner">
                                            <div id="picker3" class="picker"></div>
                                            <div class="change_color">
                                                <strong><em>主色</em></strong>
                                                <p><input type="text" value="" class="colorwell color_radio_0"></p>
                                            </div>
                                            <div class="modify_input clearfix">
                                                    <p class="left">规格：</p>
                                                    <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                        <el-option value="宽屏">宽屏</el-option>
                                                        <el-option value="窄屏">窄屏</el-option>
                                                    </el-select>
                                            </div>
                                            <div class="modify_input clearfix">
                                                    <p class="left">修改高度：</p>
                                                    <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                            </div>
                                            <div class="modify_input clearfix">
                                                    <p class="left">下边距(PX)：</p>
                                                    <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                            </div>
                                            <div class="modify_input clearfix">
                                                <p class="left">显示：</p>
                                                <div class="isShow input_text left">
                                                    <el-switch
                                                            v-model="title_isShow"
                                                            active-color="#0c6eff"
                                                            inactive-color="#ccc"
                                                            >
                                                    </el-switch>
                                                </div>
                                            </div>
                                            <el-button type="primary" class="preservation_but">保存</el-button>
                                    </div>
                                </div>
                             </el-tab-pane>
                             <el-tab-pane label="图像" name="img">
                                    <div class="tab_item">
                                        <div class="tab_inner">
                                                <div class="mini_tab_item bgImg_set">
                                                    <div class="up_img clearfix">
                                                        <div class="show_img left"><i class="fa fa-camera"></i></div>
                                                        <div class="up_but left">
                                                            <label><a  class="upload"><i class="fa fa-camera"></i>上传<input type="file" name="filename" accept="image/gif,image/jpeg,image/jpg,image/png"></a></label>
                                                            <a class="eliminate"><i class="fa fa-times"></i>清除</a>
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="bg_position">
                                                    <h3><span>背景位置</span></h3>
                                                    <div class="location_sele clearfix">
                                                        <a class="posi_top on"><em></em><input type="radio" name="bj_img_posi" ></a>
                                                        <a class="posi_middle"><em></em><input type="radio" name="bj_img_posi" checked></a>
                                                        <a class="posi_bottom"><em></em><input type="radio" name="bj_img_posi"></a>
                                                    </div>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">规格：</p>
                                                        <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                            <el-option value="宽屏">宽屏</el-option>
                                                            <el-option value="窄屏">窄屏</el-option>
                                                        </el-select>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">修改高度：</p>
                                                        <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">下边距(PX)：</p>
                                                        <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                    <p class="left">显示：</p>
                                                    <div class="isShow input_text left">
                                                        <el-switch
                                                                v-model="title_isShow"
                                                                active-color="#0c6eff"
                                                                inactive-color="#ccc"
                                                                >
                                                        </el-switch>
                                                    </div>
                                                </div>
                                                <el-button type="primary" class="preservation_but">保存</el-button>
                                        </div>
                                    </div>
                             </el-tab-pane>
                         </el-tabs>
                        <!-- <div class="tab_title"><a class="on" tab="0">纯色</a><a tab="1">图像</a></div>
                        <div class="tab_con">
                            <div class="tab_item">
                                <div class="tab_inner">
                                        <div id="picker3" class="picker"></div>
                                        <div class="change_color">
                                            <strong><em>主色</em></strong>
                                            <p><input type="text" value="" class="colorwell color_radio_0"></p>
                                        </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">规格：</p>
                                                <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                    <el-option value="宽屏">宽屏</el-option>
                                                    <el-option value="窄屏">窄屏</el-option>
                                                </el-select>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">修改高度：</p>
                                                <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">下边距(PX)：</p>
                                                <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                         <div class="modify_input clearfix">
                                            <p class="left">显示：</p>
                                            <div class="isShow input_text left">
                                                <el-switch
                                                        v-model="title_isShow"
                                                        active-color="#0c6eff"
                                                        inactive-color="#ccc"
                                                        >
                                                </el-switch>
                                            </div>
                                        </div>
                                        <el-button type="primary" class="preservation_but">保存</el-button>
                                </div>
                            </div>
                            <div class="tab_item">
                                <div class="tab_inner">
                                        <div class="mini_tab_item bgImg_set">
                                            <div class="up_img clearfix">
                                                <div class="show_img left"><i class="fa fa-camera"></i></div>
                                                <div class="up_but left">
                                                    <label><a  class="upload"><i class="fa fa-camera"></i>上传<input type="file" name="filename" accept="image/gif,image/jpeg,image/jpg,image/png"></a></label>
                                                    <a class="eliminate"><i class="fa fa-times"></i>清除</a>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="bg_position">
                                            <h3><span>背景位置</span></h3>
                                            <div class="location_sele clearfix">
                                                <a class="posi_top on"><em></em><input type="radio" name="bj_img_posi" ></a>
                                                <a class="posi_middle"><em></em><input type="radio" name="bj_img_posi" checked></a>
                                                <a class="posi_bottom"><em></em><input type="radio" name="bj_img_posi"></a>
                                            </div>
                                        </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">规格：</p>
                                                <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                    <el-option value="宽屏">宽屏</el-option>
                                                    <el-option value="窄屏">窄屏</el-option>
                                                </el-select>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">修改高度：</p>
                                                <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">下边距(PX)：</p>
                                                <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                         <div class="modify_input clearfix">
                                            <p class="left">显示：</p>
                                            <div class="isShow input_text left">
                                                <el-switch
                                                        v-model="title_isShow"
                                                        active-color="#0c6eff"
                                                        inactive-color="#ccc"
                                                        >
                                                </el-switch>
                                            </div>
                                        </div>
                                        <el-button type="primary" class="preservation_but">保存</el-button>
                                </div>
                            </div>
                        </div> -->
                </div>
                <div class="operation_panel  right_number_4">
                         <h3><span>选择模块</span></h3>
                         <el-tabs v-model="right_tab_4" class="tab_title">
                            <el-tab-pane label="新闻栏目" name="news">
                                    <div class="tab_item">
                                        <div class="tab_inner">
                                                <div class="mod_all clearfix">
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="news_0"
                                                                    data-name="新闻"
                                                                    data-type="news_0"
                                                                    data-columnId="1"
                                                                ><i></i>新闻模块</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="img_0"
                                                                    data-name="图文"
                                                                    data-type="img_0"
                                                                    data-columnId="1"
                                                                    
                                                                ><i></i>图文模块</label></dt>
                                                                <dd><label><input type="checkbox"
                                                                    data-mod="img_1"
                                                                    data-name="社团动态"
                                                                    data-type="img_1"
                                                                ><i></i>图文模块1</label></dd>
                                                                <dd><label><input type="checkbox"
                                                                    data-mod="img_2"
                                                                    data-name="社团动态"
                                                                    data-type="img_2"
                                                                ><i></i>图文模块2</label></dd>
                                                                <dd><label><input type="checkbox" 
                                                                    data-mod="img_3"
                                                                    data-name="社团动态"
                                                                    data-type="img_3"
                                                                ><i></i>图文模块3</label></dd>
                                                                <dd><label><input type="checkbox"
                                                                    data-mod="img_4"
                                                                    data-name="社团动态"
                                                                    data-type="img_4"
                                                                ><i></i>图文模块4</label></dd>
                                                                <dd><label><input type="checkbox"
                                                                    data-mod="img_5"
                                                                    data-name="社团动态"
                                                                    data-type="img_5"
                                                                ><i></i>图文模块5</label></dd>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_0"
                                                                    data-name="社团动态"
                                                                    data-type="template_0"
                                                                    ><i></i>新添加模块-0</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_1"
                                                                    data-name="社团动态"
                                                                    data-type="template_1"
                                                                    ><i></i>新添加模块-1</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_2"
                                                                    data-name="社团动态"
                                                                    data-type="template_2"
                                                                    ><i></i>新添加模块-2</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_3"
                                                                    data-name="社团动态"
                                                                    data-type="template_3"
                                                                    ><i></i>新添加模块-3</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_4"
                                                                    data-name="社团动态"
                                                                    data-type="template_4"
                                                                    ><i></i>新添加模块-4</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="list_0"
                                                                    data-name="社团动态"
                                                                    data-type="list_0"
                                                                    ><i></i>图标列表模块</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="apply_0"
                                                                    data-name="申请入会"
                                                                    data-type="apply_0"
                                                                    ><i></i>申请入会模块</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="slide_0"
                                                                    data-name="社团动态"
                                                                    data-type="slide_0"
                                                                    ><i></i>轮播图模块</label></dt>
                                                            </dl>
                                                </div>
                                        </div>
                                    </div>
                            </el-tab-pane>
                            <el-tab-pane label="辅助功能" name="support">
                                    <div class="tab_item">
                                        <div class="tab_inner">
                                            <div class="support_method clearfix">
                                                    <div class="mod_line clearfix" >
                                                        <div class="left add_wrap">
                                                                <img src="static/images/mod_icon_1.png" alt="">
                                                                <label>
                                                                        <a class="add" data-mod-link="zydj_0">+ 添加</a>
                                                                        <input type="checkbox" class="isAdd">
                                                                </label>
                                                        </div>
                                                        <div class="left info_wrap">
                                                            <h3>资源对接模块</h3>
                                                            <p>作用：集合社团成员的商业或个人资源，建立社团的供求市场</p>
                                                        </div>
                                                    </div>
                                                    <div class="mod_line clearfix">
                                                        <div class="left add_wrap">
                                                                <img src="static/images/mod_icon_2.png" alt="">
                                                                <label>
                                                                    <a class="add" data-mod-link="help_0">+ 添加</a>
                                                                    <input type="checkbox" class="isAdd">
                                                                </label>
                                                        </div>
                                                        <div class="left info_wrap">
                                                            <h3>帮帮忙-专家模块</h3>
                                                            <p>作用：建立社团
                                                                的专家团队，可
                                                                在线向专家提问
                                                                ,答疑解惑</p>
                                                        </div>
                                                    </div>
                                                    <div class="mod_line clearfix">
                                                        <div class="left add_wrap">
                                                                <img src="static/images/mod_icon_3.png" alt="">
                                                                <label>
                                                                    <a class="add" data-mod-link="quanzi_0">+ 添加</a>
                                                                    <input type="checkbox" class="isAdd">
                                                                </label>
                                                        </div>
                                                        <div class="left info_wrap">
                                                            <h3>圈子</h3>
                                                            <p>作用：建立有相
                                                                同爱好、兴趣联
                                                                系在一起的社群。</p>
                                                        </div>
                                                    </div>
                                                    <div class="mod_line clearfix">
                                                        <div class="left add_wrap">
                                                            <img src="static/images/mod_icon_4.png" alt="">
                                                            <label>
                                                                <a class="add" data-mod-link="wenjuan_0">+ 添加</a>
                                                                <input type="checkbox" class="isAdd">
                                                            </label>
                                                        </div>
                                                        <div class="left info_wrap">
                                                            <h3>调查问卷</h3>
                                                            <p>作用：用于调研
                                                                和投票</p>
                                                        </div>
                                                    </div>
                                                    <div class="mod_line clearfix">
                                                        <div class="left add_wrap">
                                                                <img src="static/images/mod_icon_5.png" alt="">
                                                                <label>
                                                                    <a class="add" data-mod-link="wenku_0">+ 添加</a>
                                                                    <input type="checkbox" class="isAdd">
                                                                </label>
                                                        </div>
                                                        <div class="left info_wrap">
                                                            <h3>文库</h3>
                                                            <p>作用：为社团提
                                                                供资源分享，
                                                                学习园地</p>
                                                        </div>
                                                    </div>
                                                    <div class="mod_line clearfix">
                                                        <div class="left add_wrap">
                                                                <img src="static/images/mod_icon_5.png" alt="">
                                                                <label>
                                                                    <a class="add" data-mod-link="dzqk_0">+ 添加</a>
                                                                    <input type="checkbox" class="isAdd">
                                                                </label>
                                                        </div>
                                                        <div class="left info_wrap">
                                                            <h3>电子期刊</h3>
                                                            <p>作用：在线阅读
                                                                与下载期刊服务</p>
                                                        </div>
                                                    </div>
                                                    <div class="mod_line clearfix">
                                                        <div class="left add_wrap">
                                                                <img src="static/images/mod_icon_5.png" alt="">
                                                                <label>
                                                                    <a class="add" data-mod-link="jz_0">+ 添加</a>
                                                                    <input type="checkbox" class="isAdd" >
                                                                </label>
                                                        </div>
                                                        <div class="left info_wrap">
                                                            <h3>捐赠</h3>
                                                            <p>作用：提供社员
                                                                在线捐赠，捐物
                                                                等</p>
                                                        </div>
                                                    </div>
                                            </div>
                                        </div>
                                    </div>
                            </el-tab-pane>
                        </el-tabs>
                        <!-- <div class="tab_title"><a class="on" tab="0">新闻栏目</a><a tab="1">辅助功能</a></div>
                        <div class="tab_con">
                            <div class="tab_item">
                                <div class="tab_inner">
                                        <div class="mod_all clearfix">
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="news_0"
                                                            data-name="新闻"
                                                            data-type="news_0"
                                                            data-columnId="1"
                                                        ><i></i>新闻模块</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="img_0"
                                                            data-name="图文"
                                                            data-type="img_0"
                                                            data-columnId="1"
                                                            
                                                        ><i></i>图文模块</label></dt>
                                                        <dd><label><input type="checkbox"
                                                            data-mod="img_1"
                                                            data-name="社团动态"
                                                            data-type="img_1"
                                                        ><i></i>图文模块1</label></dd>
                                                        <dd><label><input type="checkbox"
                                                            data-mod="img_2"
                                                            data-name="社团动态"
                                                            data-type="img_2"
                                                        ><i></i>图文模块2</label></dd>
                                                        <dd><label><input type="checkbox" 
                                                            data-mod="img_3"
                                                            data-name="社团动态"
                                                            data-type="img_3"
                                                        ><i></i>图文模块3</label></dd>
                                                        <dd><label><input type="checkbox"
                                                            data-mod="img_4"
                                                            data-name="社团动态"
                                                            data-type="img_4"
                                                        ><i></i>图文模块4</label></dd>
                                                        <dd><label><input type="checkbox"
                                                            data-mod="img_5"
                                                            data-name="社团动态"
                                                            data-type="img_5"
                                                        ><i></i>图文模块5</label></dd>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_0"
                                                            data-name="社团动态"
                                                            data-type="template_0"
                                                            ><i></i>新添加模块-0</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_1"
                                                            data-name="社团动态"
                                                            data-type="template_1"
                                                            ><i></i>新添加模块-1</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_2"
                                                            data-name="社团动态"
                                                            data-type="template_2"
                                                            ><i></i>新添加模块-2</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_3"
                                                            data-name="社团动态"
                                                            data-type="template_3"
                                                            ><i></i>新添加模块-3</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_4"
                                                            data-name="社团动态"
                                                            data-type="template_4"
                                                            ><i></i>新添加模块-4</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="list_0"
                                                            data-name="社团动态"
                                                            data-type="list_0"
                                                            ><i></i>图标列表模块</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="apply_0"
                                                            data-name="申请入会"
                                                            data-type="apply_0"
                                                            ><i></i>申请入会模块</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="slide_0"
                                                            data-name="社团动态"
                                                            data-type="slide_0"
                                                            ><i></i>轮播图模块</label></dt>
                                                    </dl>
                                        </div>
                                </div>
                            </div>
                            <div class="tab_item">
                                <div class="tab_inner">
                                    <div class="support_method clearfix">
                                            <div class="mod_line clearfix" >
                                                <div class="left add_wrap">
                                                        <img src="static/images/mod_icon_1.png" alt="">
                                                        <label>
                                                                <a class="add" data-mod-link="zydj_0">+ 添加</a>
                                                                <input type="checkbox" class="isAdd">
                                                        </label>
                                                </div>
                                                <div class="left info_wrap">
                                                    <h3>资源对接模块</h3>
                                                    <p>作用：集合社团成员的商业或个人资源，建立社团的供求市场</p>
                                                </div>
                                            </div>
                                            <div class="mod_line clearfix">
                                                <div class="left add_wrap">
                                                        <img src="static/images/mod_icon_2.png" alt="">
                                                        <label>
                                                            <a class="add" data-mod-link="help_0">+ 添加</a>
                                                            <input type="checkbox" class="isAdd">
                                                        </label>
                                                </div>
                                                <div class="left info_wrap">
                                                    <h3>帮帮忙-专家模块</h3>
                                                    <p>作用：建立社团
                                                        的专家团队，可
                                                        在线向专家提问
                                                        ,答疑解惑</p>
                                                </div>
                                            </div>
                                            <div class="mod_line clearfix">
                                                <div class="left add_wrap">
                                                        <img src="static/images/mod_icon_3.png" alt="">
                                                        <label>
                                                            <a class="add" data-mod-link="quanzi_0">+ 添加</a>
                                                            <input type="checkbox" class="isAdd">
                                                        </label>
                                                </div>
                                                <div class="left info_wrap">
                                                    <h3>圈子</h3>
                                                    <p>作用：建立有相
                                                        同爱好、兴趣联
                                                        系在一起的社群。</p>
                                                </div>
                                            </div>
                                            <div class="mod_line clearfix">
                                                <div class="left add_wrap">
                                                    <img src="static/images/mod_icon_4.png" alt="">
                                                    <label>
                                                        <a class="add" data-mod-link="wenjuan_0">+ 添加</a>
                                                        <input type="checkbox" class="isAdd">
                                                    </label>
                                                </div>
                                                <div class="left info_wrap">
                                                    <h3>调查问卷</h3>
                                                    <p>作用：用于调研
                                                        和投票</p>
                                                </div>
                                            </div>
                                            <div class="mod_line clearfix">
                                                <div class="left add_wrap">
                                                        <img src="static/images/mod_icon_5.png" alt="">
                                                        <label>
                                                            <a class="add" data-mod-link="wenku_0">+ 添加</a>
                                                            <input type="checkbox" class="isAdd">
                                                        </label>
                                                </div>
                                                <div class="left info_wrap">
                                                    <h3>文库</h3>
                                                    <p>作用：为社团提
                                                        供资源分享，
                                                        学习园地</p>
                                                </div>
                                            </div>
                                            <div class="mod_line clearfix">
                                                <div class="left add_wrap">
                                                        <img src="static/images/mod_icon_5.png" alt="">
                                                        <label>
                                                            <a class="add" data-mod-link="dzqk_0">+ 添加</a>
                                                            <input type="checkbox" class="isAdd">
                                                        </label>
                                                </div>
                                                <div class="left info_wrap">
                                                    <h3>电子期刊</h3>
                                                    <p>作用：在线阅读
                                                        与下载期刊服务</p>
                                                </div>
                                            </div>
                                            <div class="mod_line clearfix">
                                                <div class="left add_wrap">
                                                        <img src="static/images/mod_icon_5.png" alt="">
                                                        <label>
                                                            <a class="add" data-mod-link="jz_0">+ 添加</a>
                                                            <input type="checkbox" class="isAdd" >
                                                        </label>
                                                </div>
                                                <div class="left info_wrap">
                                                    <h3>捐赠</h3>
                                                    <p>作用：提供社员
                                                        在线捐赠，捐物
                                                        等</p>
                                                </div>
                                            </div>
                                    </div>
                                </div>
                            </div>
                        </div> -->
                </div>
                <div class="operation_panel  right_number_5">
                         <h3><span>顶部设置</span></h3>
                         <el-tabs v-model="right_tab_5" class="tab_title">
                            <el-tab-pane label="纯色" name="color">
                                    <div class="tab_item">
                                        <div class="tab_inner">
                                                <div id="picker3" class="picker"></div>
                                                <div class="change_color">
                                                    <strong><em>主色</em></strong>
                                                    <p><input type="text" value="" class="colorwell color_radio_0"></p>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">规格：</p>
                                                        <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                            <el-option value="宽屏">宽屏</el-option>
                                                            <el-option value="窄屏">窄屏</el-option>
                                                        </el-select>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">修改高度：</p>
                                                        <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">下边距(PX)：</p>
                                                        <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                    <p class="left">显示：</p>
                                                    <div class="isShow input_text left">
                                                        <el-switch
                                                                v-model="title_isShow"
                                                                active-color="#0c6eff"
                                                                inactive-color="#ccc"
                                                                >
                                                        </el-switch>
                                                    </div>
                                                </div>
                                                <el-button type="primary" class="preservation_but">保存</el-button>
                                        </div>
                                    </div>
                            </el-tab-pane>
                            <el-tab-pane label="图像" name="img">
                                    <div class="tab_item">
                                        <div class="tab_inner">
                                                <div class="mini_tab_item bgImg_set">
                                                    <div class="up_img clearfix">
                                                        <div class="show_img left"><i class="fa fa-camera"></i></div>
                                                        <div class="up_but left">
                                                            <label><a  class="upload"><i class="fa fa-camera"></i>上传<input type="file" name="filename" accept="image/gif,image/jpeg,image/jpg,image/png"></a></label>
                                                            <a class="eliminate"><i class="fa fa-times"></i>清除</a>
                                                        </div>
                                                    </div>
                                                </div>
                                                <div class="bg_position">
                                                    <h3><span>背景位置</span></h3>
                                                    <div class="location_sele clearfix">
                                                        <a class="posi_top on"><em></em><input type="radio" name="bj_img_posi" ></a>
                                                        <a class="posi_middle"><em></em><input type="radio" name="bj_img_posi" checked></a>
                                                        <a class="posi_bottom"><em></em><input type="radio" name="bj_img_posi"></a>
                                                    </div>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">规格：</p>
                                                        <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                            <el-option value="宽屏">宽屏</el-option>
                                                            <el-option value="窄屏">窄屏</el-option>
                                                        </el-select>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">修改高度：</p>
                                                        <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                        <p class="left">下边距(PX)：</p>
                                                        <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                    <p class="left">显示：</p>
                                                    <div class="isShow input_text left">
                                                        <el-switch
                                                                v-model="title_isShow"
                                                                active-color="#0c6eff"
                                                                inactive-color="#ccc"
                                                                >
                                                        </el-switch>
                                                    </div>
                                                </div>
                                                <el-button type="primary" class="preservation_but">保存</el-button>
                                        </div>
                                    </div>
                            </el-tab-pane>
                        </el-tabs>
                        <!-- <div class="tab_title"><a class="on" tab="0">纯色</a><a tab="1">图像</a></div>
                        <div class="tab_con">
                            <div class="tab_item">
                                <div class="tab_inner">
                                        <div id="picker3" class="picker"></div>
                                        <div class="change_color">
                                            <strong><em>主色</em></strong>
                                            <p><input type="text" value="" class="colorwell color_radio_0"></p>
                                        </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">规格：</p>
                                                <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                    <el-option value="宽屏">宽屏</el-option>
                                                    <el-option value="窄屏">窄屏</el-option>
                                                </el-select>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">修改高度：</p>
                                                <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">下边距(PX)：</p>
                                                <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                         <div class="modify_input clearfix">
                                            <p class="left">显示：</p>
                                            <div class="isShow input_text left">
                                                <el-switch
                                                        v-model="title_isShow"
                                                        active-color="#0c6eff"
                                                        inactive-color="#ccc"
                                                        >
                                                </el-switch>
                                            </div>
                                        </div>
                                        <el-button type="primary" class="preservation_but">保存</el-button>
                                </div>
                            </div>
                            <div class="tab_item">
                                <div class="tab_inner">
                                        <div class="mini_tab_item bgImg_set">
                                            <div class="up_img clearfix">
                                                <div class="show_img left"><i class="fa fa-camera"></i></div>
                                                <div class="up_but left">
                                                    <label><a  class="upload"><i class="fa fa-camera"></i>上传<input type="file" name="filename" accept="image/gif,image/jpeg,image/jpg,image/png"></a></label>
                                                    <a class="eliminate"><i class="fa fa-times"></i>清除</a>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="bg_position">
                                            <h3><span>背景位置</span></h3>
                                            <div class="location_sele clearfix">
                                                <a class="posi_top on"><em></em><input type="radio" name="bj_img_posi" ></a>
                                                <a class="posi_middle"><em></em><input type="radio" name="bj_img_posi" checked></a>
                                                <a class="posi_bottom"><em></em><input type="radio" name="bj_img_posi"></a>
                                            </div>
                                        </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">规格：</p>
                                                <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                    <el-option value="宽屏">宽屏</el-option>
                                                    <el-option value="窄屏">窄屏</el-option>
                                                </el-select>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">修改高度：</p>
                                                <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                        <div class="modify_input clearfix">
                                                <p class="left">下边距(PX)：</p>
                                                <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                         </div>
                                         <div class="modify_input clearfix">
                                            <p class="left">显示：</p>
                                            <div class="isShow input_text left">
                                                <el-switch
                                                        v-model="title_isShow"
                                                        active-color="#0c6eff"
                                                        inactive-color="#ccc"
                                                        >
                                                </el-switch>
                                            </div>
                                        </div>
                                        <el-button type="primary" class="preservation_but">保存</el-button>
                                </div>
                            </div>
                        </div> -->
                </div>
                <div class="operation_panel  right_number_6">
                         <h3><span>轮播图设置</span></h3>
                         <el-tabs v-model="right_tab_6" class="tab_title">
                            <el-tab-pane label="选择轮播图" name="banner_style">
                                    <div class="tab_item">
                                        <div class="tab_inner">
                                                <div class="mod_all clearfix">
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="news_0"
                                                                    data-name="新闻"
                                                                    data-type="news_0"
                                                                    data-columnId="1"
                                                                ><i></i>新闻模块</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="img_0"
                                                                    data-name="图文"
                                                                    data-type="img_0"
                                                                    data-columnId="1"
                                                                    
                                                                ><i></i>图文模块</label></dt>
                                                                <dd><label><input type="checkbox"
                                                                    data-mod="img_1"
                                                                    data-name="社团动态"
                                                                    data-type="img_1"
                                                                ><i></i>图文模块1</label></dd>
                                                                <dd><label><input type="checkbox"
                                                                    data-mod="img_2"
                                                                    data-name="社团动态"
                                                                    data-type="img_2"
                                                                ><i></i>图文模块2</label></dd>
                                                                <dd><label><input type="checkbox" 
                                                                    data-mod="img_3"
                                                                    data-name="社团动态"
                                                                    data-type="img_3"
                                                                ><i></i>图文模块3</label></dd>
                                                                <dd><label><input type="checkbox"
                                                                    data-mod="img_4"
                                                                    data-name="社团动态"
                                                                    data-type="img_4"
                                                                ><i></i>图文模块4</label></dd>
                                                                <dd><label><input type="checkbox"
                                                                    data-mod="img_5"
                                                                    data-name="社团动态"
                                                                    data-type="img_5"
                                                                ><i></i>图文模块5</label></dd>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_0"
                                                                    data-name="社团动态"
                                                                    data-type="template_0"
                                                                    ><i></i>新添加模块-0</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_1"
                                                                    data-name="社团动态"
                                                                    data-type="template_1"
                                                                    ><i></i>新添加模块-1</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_2"
                                                                    data-name="社团动态"
                                                                    data-type="template_2"
                                                                    ><i></i>新添加模块-2</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_3"
                                                                    data-name="社团动态"
                                                                    data-type="template_3"
                                                                    ><i></i>新添加模块-3</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="template_4"
                                                                    data-name="社团动态"
                                                                    data-type="template_4"
                                                                    ><i></i>新添加模块-4</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="list_0"
                                                                    data-name="社团动态"
                                                                    data-type="list_0"
                                                                    ><i></i>图标列表模块</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="apply_0"
                                                                    data-name="申请入会"
                                                                    data-type="apply_0"
                                                                    ><i></i>申请入会模块</label></dt>
                                                            </dl>
                                                            <dl>
                                                                <dt><label><input type="radio" name="chooseMod"
                                                                    data-mod="slide_0"
                                                                    data-name="社团动态"
                                                                    data-type="slide_0"
                                                                    ><i></i>轮播图模块</label></dt>
                                                            </dl>
                                                </div>
                                        </div>
                                    </div>
                            </el-tab-pane>
                            <el-tab-pane label="图像" name="img">
                                    <div class="tab_item">
                                        <div class="tab_inner">
                                            <div class="modify_input clearfix">
                                                    <p class="left">规格：</p>
                                                    <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                        <el-option value="宽屏">宽屏</el-option>
                                                        <el-option value="窄屏">窄屏</el-option>
                                                    </el-select>
                                            </div>
                                            <div class="modify_input clearfix">
                                                    <p class="left">修改高度：</p>
                                                    <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                            </div>
                                            <div class="modify_input clearfix">
                                                    <p class="left">上间距(px)：</p>
                                                    <el-input v-model="title_marTop" class="input_text left" placeholder="上间距(px)"></el-input>
                                            </div>
                                            <div class="modify_input clearfix">
                                                    <p class="left">下间距(PX)：</p>
                                                    <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                                </div>
                                                <div class="modify_input clearfix">
                                                <p class="left">显示：</p>
                                                <div class="isShow input_text left">
                                                    <el-switch
                                                            v-model="title_isShow"
                                                            active-color="#0c6eff"
                                                            inactive-color="#ccc"
                                                            >
                                                    </el-switch>
                                                </div>
                                            </div>
                                            <el-button type="primary" class="preservation_but">保存</el-button>
                                        </div>
                                    </div>
                            </el-tab-pane>
                        </el-tabs>
                        <!-- <div class="tab_title"><a class="on" tab="0">选择轮播图</a><a tab="1">图像</a></div>
                        <div class="tab_con">
                            <div class="tab_item">
                                <div class="tab_inner">
                                        <div class="mod_all clearfix">
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="news_0"
                                                            data-name="新闻"
                                                            data-type="news_0"
                                                            data-columnId="1"
                                                        ><i></i>新闻模块</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="img_0"
                                                            data-name="图文"
                                                            data-type="img_0"
                                                            data-columnId="1"
                                                            
                                                        ><i></i>图文模块</label></dt>
                                                        <dd><label><input type="checkbox"
                                                            data-mod="img_1"
                                                            data-name="社团动态"
                                                            data-type="img_1"
                                                        ><i></i>图文模块1</label></dd>
                                                        <dd><label><input type="checkbox"
                                                            data-mod="img_2"
                                                            data-name="社团动态"
                                                            data-type="img_2"
                                                        ><i></i>图文模块2</label></dd>
                                                        <dd><label><input type="checkbox" 
                                                            data-mod="img_3"
                                                            data-name="社团动态"
                                                            data-type="img_3"
                                                        ><i></i>图文模块3</label></dd>
                                                        <dd><label><input type="checkbox"
                                                            data-mod="img_4"
                                                            data-name="社团动态"
                                                            data-type="img_4"
                                                        ><i></i>图文模块4</label></dd>
                                                        <dd><label><input type="checkbox"
                                                            data-mod="img_5"
                                                            data-name="社团动态"
                                                            data-type="img_5"
                                                        ><i></i>图文模块5</label></dd>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_0"
                                                            data-name="社团动态"
                                                            data-type="template_0"
                                                            ><i></i>新添加模块-0</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_1"
                                                            data-name="社团动态"
                                                            data-type="template_1"
                                                            ><i></i>新添加模块-1</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_2"
                                                            data-name="社团动态"
                                                            data-type="template_2"
                                                            ><i></i>新添加模块-2</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_3"
                                                            data-name="社团动态"
                                                            data-type="template_3"
                                                            ><i></i>新添加模块-3</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="template_4"
                                                            data-name="社团动态"
                                                            data-type="template_4"
                                                            ><i></i>新添加模块-4</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="list_0"
                                                            data-name="社团动态"
                                                            data-type="list_0"
                                                            ><i></i>图标列表模块</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="apply_0"
                                                            data-name="申请入会"
                                                            data-type="apply_0"
                                                            ><i></i>申请入会模块</label></dt>
                                                    </dl>
                                                    <dl>
                                                        <dt><label><input type="radio" name="chooseMod"
                                                            data-mod="slide_0"
                                                            data-name="社团动态"
                                                            data-type="slide_0"
                                                            ><i></i>轮播图模块</label></dt>
                                                    </dl>
                                        </div>
                                </div>
                            </div>
                            <div class="tab_item">
                                <div class="tab_inner">
                                    <div class="modify_input clearfix">
                                            <p class="left">规格：</p>
                                            <el-select v-model="title_size" class="input_text left" placeholder="请选择">
                                                <el-option value="宽屏">宽屏</el-option>
                                                <el-option value="窄屏">窄屏</el-option>
                                            </el-select>
                                    </div>
                                    <div class="modify_input clearfix">
                                            <p class="left">修改高度：</p>
                                            <el-input v-model="title_height" class="input_text left" placeholder="高度(px)"></el-input>
                                    </div>
                                    <div class="modify_input clearfix">
                                            <p class="left">上间距(px)：</p>
                                            <el-input v-model="title_marTop" class="input_text left" placeholder="上间距(px)"></el-input>
                                    </div>
                                    <div class="modify_input clearfix">
                                            <p class="left">下间距(PX)：</p>
                                            <el-input v-model="title_marBot" class="input_text left" placeholder="高度(px)"></el-input>
                                        </div>
                                        <div class="modify_input clearfix">
                                        <p class="left">显示：</p>
                                        <div class="isShow input_text left">
                                            <el-switch
                                                    v-model="title_isShow"
                                                    active-color="#0c6eff"
                                                    inactive-color="#ccc"
                                                    >
                                            </el-switch>
                                        </div>
                                    </div>
                                    <el-button type="primary" class="preservation_but">保存</el-button>
                                </div>
                            </div>
                        </div> -->
                </div>
        </div>
</template>
<script>
    export default {
        name: 'RightSideBar',
        props: ['sidebarHeight'],
        data() {
            return {
                logo_width: '',
                logo_height: '',
                logo_isShow: '',
                webName: '',
                webName_size: '',
                webName_font: '',
                webName_isShow: '',
                title_size: '',
                title_height: '',
                title_marBot: '',
                title_marTop: '',
                title_isShow: '',
                right_tab_2: 'color',
                right_tab_3: 'color',
                right_tab_4: 'news',
                right_tab_5: 'color',
                right_tab_6: 'banner_style',
            }
        },
        mounted() {
        },
    }
</script>
<style lang="scss">
    @import '../../assets/scss/base.scss';
    .leon-frame {
        .rightSideBar {
            position: fixed;
            right: -220px;
            top: 70px;
            background-color: #283c50;
            overflow: hidden;
            z-index: 15;
            .webName_font {
                width: 112px;
                margin-left: 20px;
            }
             .slider_block {
                position: relative;
                top: 10px;
                width: 106px;
                margin-left: 25px;
            }
            .tab_item {
                .bg_position {
                    > h3 {
                        span {
                            background-color: #283c50;
                            color: #fff;
                        }
                    }
                }
            }
        }
        .right_number_6,
        .right_number_4 {
            .support_method {
                .mod_line {
                    background: none;
                    padding-bottom:18px;
                    border-bottom: 1px solid #3a4e62;
                    padding-top: 10px;
                }
                img {
                    margin-bottom: 8px; 
                }
                label {
                    position: relative;
                    display: block; 
                }
                .isAdd {
                    position: absolute;
                    left: 0;
                    top: 0;
                    width: 62px;
                    height: 36px;
                    z-index: -1;
                    filter: progid:DXImageTransform.Microsoft.Alpha(opacity=0);/*兼容ie8及以下*/ 
                    -khtml-opacity:0;
                    -moz-opacity:0;
                    filter:alpha(opacity=0);
                    opacity:0;
                }
                .add {
                    display: block;
                    border-radius: 4px;
                    line-height: 36px;
                    text-align: center;
                    background: url(../../../static/images/bj_b.jpg);
                    color: #fff;
                    width: 62px;
                    height: 36px;
                }
                .info_wrap {
                    width: 116px;
                    padding-left: 8px;
                    h3 {
                        font-size: 14px;
                        margin-bottom: 10px;
                        color: #fff;
                    }
                    p {
                        font-size: 14px;
                        color: #cdcdcd;
                    }
                }
            }
            .mod_all {
                background-color:#3a4f63;
                color:#fff;
                label {
                    height:30px;
                    display:block;
                    line-height:30px;
                    position:relative;
                    i {
                        background:url("../../../static/images/checkbox_img.png");
                        width:16px;
                        height:16px;
                        float:left;
                        margin:6px 14px 0 10px;
                    }
                    input {
                        position:absolute;
                        left:0;
                        top:0; 
                        filter: progid:DXImageTransform.Microsoft.Alpha(opacity=0);/*兼容ie8及以下*/ 
                        -khtml-opacity:0;
                        -moz-opacity:0;
                        filter:alpha(opacity=0); 
                        opacity:0;
                        &:checked {
                            i {
                                background-position:-18px 0px;
                            }
                            &:disabled {
                                i {
                                    background-position:-36px 0px;
                                }
                            }
                        }
                    }
                    
                }
                dl {
                        dd {
                            position:relative;
                            label {
                                padding-left: 30px;
                            }
                            &:before {
                                content:"";
                                border-left:1px dashed #617d98;
                                position:absolute;
                                left:18px;
                                top:0;
                                display: block;
                                width:1px;
                                height:100%;
                            }
                            &:after {
                                content:"";
                                background:url("../../../static/images/checked_left.png");
                                width:10px;
                                height:14px;
                                display:block;
                                position:absolute;
                                left:18px;
                                top:6px;
                            }
                        }
                    }
            }
        }
       .right_number_5,
       .right_number_6,
       .right_number_3,
       .right_number_2 {
           .tab_item {
               .modify_input {
                   p {
                       width: 44%;
                       text-align: right;
                   }
                    .input_text {
                        width: 50%;
                        margin-left: 10px;
                    }
               }
           }
       }
        .right_number_0,
        .right_number_2,
        .right_number_4,
        .right_number_5,
        .right_number_6,
        .right_number_1 {
            display: none;
        }
    }
</style>
