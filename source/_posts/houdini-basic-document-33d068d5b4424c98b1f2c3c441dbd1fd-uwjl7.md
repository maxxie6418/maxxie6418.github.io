<h1>Houdini基础文档 33d068d5b4424c98b1f2c3c441dbd1fd</h1>
<h1>Houdini基础文档</h1>
<h1>一、基础操作</h1>
<h2>1.快捷键：</h2>
<ol>
<li>四视图切换——【B】</li>
<li>透视图【1】、顶底视图【2】、前后视图【3】、左右视图【4】、UV窗口视图【5】</li>
<li>创建节点——【Tab】</li>
<li>进入模型选择模式【s】、选物体模式【1】、选点模式【2】、选线模式【3】、选面模式【4】</li>
<li>数值复位【Ctrl+鼠标中键】</li>
<li>切除连线【长按Y键】</li>
<li>整理节点排列【L】，滑动指向排列【在节点上按A，点住鼠标左键滑动】</li>
<li>整体移动【选中节点后按住shift拖动】</li>
<li>线段上增加定位点【Alt+鼠标左键】</li>
<li>切换线条显示模式【Shift+S】</li>
<li>切换节点级别，返回父级【U】，进入子级【i】</li>
<li>居中显示【空格+H】</li>
<li>显示设置【D】</li>
<li>添加关键帧【Alt+鼠标左键】、移除关键帧【Ctrl+鼠标左键】</li>
<li>打开曲线面板【Shift+鼠标左键】，最大化显示【空格+H】</li>
<li>时间轴控制：播放暂停【↑】、退回第一帧【Ctrl+↑】、左右移动一帧【←、→】、上一关键帧【Ctrl+←】、下一关键帧【Ctrl+→】</li>
<li>修改节点连线样式：【Shift+S】</li>
</ol>
<h2>2.基础操作：</h2>
<p>1.节点介绍</p>
<p><img src="assets/Untitled-20231014000634-0q43701.png" alt="Untitled" /></p>
<p>左1为跳过当前节点【快捷键Q】</p>
<p>左2为锁定属性，父级节点的属性设置无效，仅启用节点本身的属性设置</p>
<p>右1为线框预览【快捷键E】</p>
<p>右2为预览显示，Ctrl点击变紫色时，表示渲染显示【快捷键R】</p>
<p>2.当前节点创建相机：按住Ctrl点击相机图标</p>
<h2>3.其他备注：</h2>
<p>1.UI存储路径：我的文档\houdini19.0\desktop</p>
<h1>二、节点</h1>
<p>![Untitled](assets/Untitled 1-20231014000634-gde381i.png)</p>
<h2>1.<a href="https://www.sidefx.com/docs/houdini/nodes/sop/index.html">基础节点</a></h2>
<ol>
<li>
<p>Geometry-多边形</p>
</li>
<li>
<p>Transform-位移</p>
</li>
<li>
<p>Polybevel-倒角</p>
<ol>
<li>Distance：倒角大小(倒角距离)</li>
<li>Divisions：细分</li>
<li>Convexity：凸出，决定倒角圆弧朝向</li>
<li>//选中节点后敲击回车可进入鼠标选择模式</li>
</ol>
</li>
<li>
<p>Blast-删除</p>
</li>
<li>
<p>Polyextrude-挤压</p>
<ol>
<li>Divide into：修改挤出类型，独立挤出还是合并挤出</li>
</ol>
</li>
<li>
<p>Merge：合并</p>
</li>
<li>
<p>Polybridge：桥接</p>
</li>
<li>
<p>Subdivide：细分</p>
</li>
<li>
<p>PolyReduce：减面</p>
</li>
<li>
<p>Polyfill：补面</p>
</li>
<li>
<p>Hole：挖洞</p>
</li>
<li>
<p>Boolean：布尔</p>
</li>
<li>
<p>Obejct_merge：对象合并</p>
</li>
<li>
<p>Clip：裁切</p>
</li>
<li>
<p>Intersection Analysis：交叉监测（只能输入三角面或曲线）</p>
</li>
<li>
<p>Intersection Stitch：交叉缝合</p>
</li>
<li>
<p>Boolean：布尔</p>
</li>
<li>
<p>Explodedview：炸开</p>
</li>
<li>
<p>Scatter：撒点</p>
</li>
<li>
<p>Attribute Paint：属性绘图，直接在几何图形上绘制</p>
</li>
<li>
<p>Attribute Create：属性创建，添加或编辑用户定义的属性。</p>
</li>
<li>
<p>Copy to Points：复制到点，将第一个输入中的几何复制到第二个输入的点上。（被复制体的Z轴会对齐目标的法线）</p>
</li>
<li>
<p>Copy Stamp：复制，可复制到目标，也可不需要目标</p>
</li>
<li>
<p>Group Combine：组合并，类似组的布尔功能</p>
</li>
<li>
<p>Group Delete：组删除</p>
</li>
<li>
<p>Group Copy：组复制</p>
</li>
<li>
<p>Group Expand：组扩张</p>
</li>
<li>
<p>Convert：转换为几何模型</p>
</li>
<li>
<p>********：在两个模型之间传递顶点、点、基本体和/或细节属性。</p>
</li>
<li>
<p>****：重命名属性</p>
</li>
<li>
<p><a href="https://www.sidefx.com/docs/houdini/nodes/sop/labs--sweep_geometry.html"><strong>Labs Sweep Geometry</strong></a>：沿路径扫描几何体，可以做到模型扭曲和接缝合并。</p>
</li>
<li>
<p>********：沿曲线计算方向</p>
</li>
<li>
<p>Assign Material：材质分配</p>
</li>
<li>
<p>mtlxextract2</p>
</li>
</ol>
<h2>2.节点拓展笔记</h2>
<h1>三、表达式与函数</h1>
<h2>1.几何体属性</h2>
<table>
<thead>
<tr>
<th>名称</th>
<th>数据类型</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr>
<td>P</td>
<td>vector</td>
<td>位置</td>
</tr>
<tr>
<td>N</td>
<td>vector</td>
<td>法线</td>
</tr>
<tr>
<td>name</td>
<td>string</td>
<td>名称属性</td>
</tr>
<tr>
<td>up</td>
<td>vector</td>
<td>向上矢量</td>
</tr>
<tr>
<td>orient</td>
<td>vector4</td>
<td>四元数表示的方位属性</td>
</tr>
<tr>
<td>v</td>
<td>vector</td>
<td>速度</td>
</tr>
<tr>
<td>pscale</td>
<td>float</td>
<td>尺寸属性</td>
</tr>
</tbody>
</table>
<h2>2.全局变量</h2>
<ol>
<li>$T-时间</li>
<li>$F-帧</li>
<li>$SO-</li>
</ol>
<h1>四、软件配置</h1>
<p>**窗口配置文件地址：**Administrator\Documents\houdini19.0\desktop</p>
<p>![Untitled](assets/Untitled 2-20231014000634-2hvpw5z.png)</p>
<p>**设置默认启动界面：**Edit-Preferences-General User Interface</p>
<p>![Untitled](assets/Untitled 3-20231014000634-y5zh2d1.png)</p>
<p>**Houdini的环境配置：**修改houdini.env文件</p>
<p><a href="https://www.sidefx.com/docs/houdini/basics/config_env.html">https://www.sidefx.com/docs/houdini/basics/config_env.html</a></p>
<ul>
<li>修改帮助文档使用系统默认浏览器打开
<ul>
<li>HOUDINI_EXTERNAL_HELP_BROWSER = 1</li>
</ul>
</li>
</ul>
<h1>五、文章剪藏</h1>
<h2>基础</h2>
<p><a href="https://www.sidefx.com/docs/houdini/network/organize.html">Organizing, customizing, and annotating nodes and networks --- 组织、定制和注释节点和网络 (sidefx.com)</a></p>
<h2>地形</h2>
<p><a href="https://www.sidefx.com/docs/houdini/model/heightfields.html">Building terrain with height fields --- 使用高度场构建地形 (sidefx.com)</a></p>
<p><a href="https://www.sidefx.com/docs/houdini/model/terrain_workflow.html">Realistic terrain with heightfields --- 具有高度场的真实地形 (sidefx.com)</a></p>
<p>噪声类型 <a href="https://www.sidefx.com/docs/houdini/nodes/vop/unifiednoise.html">Unified Noise --- 统一噪声 (sidefx.com)</a></p>
<h2>技巧</h2>
