# 配置Web基础防护规则<a name="waf_01_0008"></a>

Web基础防护开启后，可防范SQL注入、XSS跨站脚本、远程溢出攻击、文件包含、Bash漏洞攻击、远程命令执行、目录遍历、敏感文件访问、命令/代码注入等常规的Web攻击，以及可支持Webshell检测、深度反逃逸检测等Web基础防护。

您也可以参考[Web基础防护功能最佳实践](https://support.huaweicloud.com/bestpractice-waf/waf_06_0014.html)了解更多Web基础防护规则的配置信息。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果您已开通企业项目，您可以在“企业项目“下拉列表中选择您所在的企业项目，为该企业项目下域名配置防护策略。

## 前提条件<a name="section5903171661012"></a>

已添加防护网站。

## 约束条件<a name="section3393202511516"></a>

-   Web基础防护支持“拦截“和“仅记录“模式，检测版仅支持“仅记录“模式。
-   添加或修改防护规则后，规则生效需要几分钟。规则生效后，您可以在“防护事件“页面查看防护效果。
-   当Web基础防护设置为“拦截“模式时，您可以设置攻击惩罚。设置攻击惩罚后，如果访问者的IP、Cookie或Params恶意请求被拦截时，WAF将根据攻击惩罚设置的拦截时长来封禁访问者。有关配置攻击惩罚的详细操作，请参见[配置攻击惩罚标准](配置攻击惩罚标准.md)。

## 操作步骤<a name="section61533550183130"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入防护策略配置入口，如[图1](#fig089771664710)所示。

    **图 1**  防护策略配置入口<a name="fig089771664710"></a>  
    ![](figures/防护策略配置入口.png "防护策略配置入口")

3.  在“Web基础防护“配置框中，用户可根据自己的需要参照[表1](#table42360431192825)更改Web基础防护的“状态“和“模式“，如[图2](#fig193788379)所示。

    **图 2**  Web基础防护配置框<a name="fig193788379"></a>  
    ![](figures/Web基础防护配置框.png "Web基础防护配置框")

    **表 1**  防护动作参数说明

    <a name="table42360431192825"></a>
    <table><thead align="left"><tr id="row66262481192825"><th class="cellrowborder" valign="top" width="22.49%" id="mcps1.2.3.1.1"><p id="p54075445192825"><a name="p54075445192825"></a><a name="p54075445192825"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="77.51%" id="mcps1.2.3.1.2"><p id="p18034950192825"><a name="p18034950192825"></a><a name="p18034950192825"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row8899732153112"><td class="cellrowborder" valign="top" width="22.49%" headers="mcps1.2.3.1.1 "><p id="p189011132173111"><a name="p189011132173111"></a><a name="p189011132173111"></a>状态</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.51%" headers="mcps1.2.3.1.2 "><p id="p11901832163110"><a name="p11901832163110"></a><a name="p11901832163110"></a>Web应用防护攻击的状态。</p>
    <a name="ul115452316468"></a><a name="ul115452316468"></a><ul id="ul115452316468"><li><a name="image1945111441539"></a><a name="image1945111441539"></a><span><img id="image1945111441539" src="figures/icon-enable.png"></span>：开启状态。</li><li><a name="image1195117112509"></a><a name="image1195117112509"></a><span><img id="image1195117112509" src="figures/icon-disable.png"></span>：关闭状态。</li></ul>
    </td>
    </tr>
    <tr id="row28096830192825"><td class="cellrowborder" valign="top" width="22.49%" headers="mcps1.2.3.1.1 "><p id="p10384205820363"><a name="p10384205820363"></a><a name="p10384205820363"></a>模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.51%" headers="mcps1.2.3.1.2 "><a name="ul946621183715"></a><a name="ul946621183715"></a><ul id="ul946621183715"><li>拦截：发现攻击行为后立即阻断并记录。</li><li>仅记录：发现攻击行为后只记录不阻断攻击。</li></ul>
    <div class="notice" id="note054144775412"><a name="note054144775412"></a><a name="note054144775412"></a><span class="noticetitle"> 须知： </span><div class="noticebody"><p id="p1054184719544"><a name="p1054184719544"></a><a name="p1054184719544"></a>检测版仅支持<span class="parmname" id="parmname06802226556"><a name="parmname06802226556"></a><a name="parmname06802226556"></a>“仅记录”</span>模式。</p>
    </div></div>
    </td>
    </tr>
    </tbody>
    </table>

4.  在“Web基础防护“配置框中，单击“高级设置“，进入“Web基础防护“界面。
5.  选择“防护配置“页签，根据您的业务场景，开启合适的防护功能，如[图3](#fig17347539113910)所示，检测项说明如[表2](#table1054818371898)所示。

    **图 3**  Web基础防护<a name="fig17347539113910"></a>  
    ![](figures/Web基础防护.png "Web基础防护")

    >![](public_sys-resources/icon-notice.gif) **须知：** 
    >当“模式“设置为“拦截“时，您可以根据需要选择配置的攻击惩罚。

    **表 2**  检测项说明

    <a name="table1054818371898"></a>
    <table><thead align="left"><tr id="row25491137297"><th class="cellrowborder" valign="top" width="25.28%" id="mcps1.2.3.1.1"><p id="p1854915379911"><a name="p1854915379911"></a><a name="p1854915379911"></a>检测项</p>
    </th>
    <th class="cellrowborder" valign="top" width="74.72%" id="mcps1.2.3.1.2"><p id="p8549737894"><a name="p8549737894"></a><a name="p8549737894"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row354983713918"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p35498371299"><a name="p35498371299"></a><a name="p35498371299"></a>常规检测</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p125497371397"><a name="p125497371397"></a><a name="p125497371397"></a>防护SQL注入、XSS跨站脚本、远程溢出攻击、文件包含、Bash漏洞攻击、远程命令执行、目录遍历、敏感文件访问、命令/代码注入等攻击。</p>
    <div class="note" id="note66541414413"><a name="note66541414413"></a><a name="note66541414413"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p86559124115"><a name="p86559124115"></a><a name="p86559124115"></a>开启<span class="parmname" id="parmname6748631164118"><a name="parmname6748631164118"></a><a name="parmname6748631164118"></a>“常规检测”</span>后，WAF将根据内置规则对常规检测项进行检测。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row5549123715914"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p754913375913"><a name="p754913375913"></a><a name="p754913375913"></a>Webshell检测</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p1754993711914"><a name="p1754993711914"></a><a name="p1754993711914"></a>防护通过上传接口植入网页木马。</p>
    <div class="note" id="note19915165154218"><a name="note19915165154218"></a><a name="note19915165154218"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1591614514423"><a name="p1591614514423"></a><a name="p1591614514423"></a>开启<span class="parmname" id="parmname6555219164311"><a name="parmname6555219164311"></a><a name="parmname6555219164311"></a>“Webshell检测”</span>后，WAF将对通过上传接口植入的网页木马进行检测。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row837585613435"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p17376556194316"><a name="p17376556194316"></a><a name="p17376556194316"></a>深度检测</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p16868294452"><a name="p16868294452"></a><a name="p16868294452"></a>防护同形字符混淆、通配符变形的命令注入、UTF7、Data URI Scheme等深度反逃逸。</p>
    <div class="note" id="note825125516470"><a name="note825125516470"></a><a name="note825125516470"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1425155154718"><a name="p1425155154718"></a><a name="p1425155154718"></a>开启<span class="parmname" id="parmname1622619445528"><a name="parmname1622619445528"></a><a name="parmname1622619445528"></a>“深度检测”</span>后，WAF将对深度反逃逸进行检测防护。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row124533351015"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p122469331102"><a name="p122469331102"></a><a name="p122469331102"></a>header全检测</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p1714019071217"><a name="p1714019071217"></a><a name="p1714019071217"></a>默认关闭。关闭状态下WAF会检测常规存在注入点的header字段。</p>
    <div class="note" id="note6982930171110"><a name="note6982930171110"></a><a name="note6982930171110"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p20983730201118"><a name="p20983730201118"></a><a name="p20983730201118"></a>开启<span class="parmname" id="parmname179831730161111"><a name="parmname179831730161111"></a><a name="parmname179831730161111"></a>“header全检测”</span>后，WAF将对请求里header中所有字段进行攻击检测。</p>
    </div></div>
    </td>
    </tr>
    </tbody>
    </table>

    1.  防护等级设置。

        在页面上方，选择防护等级，Web基础防护设置了三种防护等级：“宽松“、“中等“、“严格“，默认情况下，选择“中等“。

        **表 3**  防护等级说明

        <a name="table4686152913388"></a>
        <table><thead align="left"><tr id="zh-cn_topic_0165951356_row257619443717"><th class="cellrowborder" valign="top" width="28.849999999999998%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0165951356_p2576844573"><a name="zh-cn_topic_0165951356_p2576844573"></a><a name="zh-cn_topic_0165951356_p2576844573"></a>防护等级</p>
        </th>
        <th class="cellrowborder" valign="top" width="71.15%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0165951356_p95761144176"><a name="zh-cn_topic_0165951356_p95761144176"></a><a name="zh-cn_topic_0165951356_p95761144176"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="zh-cn_topic_0165951356_row2576644570"><td class="cellrowborder" valign="top" width="28.849999999999998%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0165951356_p7576844572"><a name="zh-cn_topic_0165951356_p7576844572"></a><a name="zh-cn_topic_0165951356_p7576844572"></a>宽松</p>
        </td>
        <td class="cellrowborder" valign="top" width="71.15%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0165951356_p15576174416714"><a name="zh-cn_topic_0165951356_p15576174416714"></a><a name="zh-cn_topic_0165951356_p15576174416714"></a>防护粒度较粗，只拦截攻击特征比较明显的请求。</p>
        <p id="zh-cn_topic_0165951356_p7903127245"><a name="zh-cn_topic_0165951356_p7903127245"></a><a name="zh-cn_topic_0165951356_p7903127245"></a>当误报情况较多的场景下，建议选择<span class="parmvalue" id="zh-cn_topic_0165951356_parmvalue335511196917"><a name="zh-cn_topic_0165951356_parmvalue335511196917"></a><a name="zh-cn_topic_0165951356_parmvalue335511196917"></a>“宽松”</span>模式。</p>
        </td>
        </tr>
        <tr id="zh-cn_topic_0165951356_row18576344378"><td class="cellrowborder" valign="top" width="28.849999999999998%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0165951356_p20576044476"><a name="zh-cn_topic_0165951356_p20576044476"></a><a name="zh-cn_topic_0165951356_p20576044476"></a>中等</p>
        </td>
        <td class="cellrowborder" valign="top" width="71.15%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0165951356_p2910122920245"><a name="zh-cn_topic_0165951356_p2910122920245"></a><a name="zh-cn_topic_0165951356_p2910122920245"></a>默认为<span class="parmvalue" id="zh-cn_topic_0165951356_parmvalue88535815254"><a name="zh-cn_topic_0165951356_parmvalue88535815254"></a><a name="zh-cn_topic_0165951356_parmvalue88535815254"></a>“中等”</span>防护模式，满足大多数场景下的Web防护需求。</p>
        </td>
        </tr>
        <tr id="zh-cn_topic_0165951356_row857616441575"><td class="cellrowborder" valign="top" width="28.849999999999998%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0165951356_p1857694417714"><a name="zh-cn_topic_0165951356_p1857694417714"></a><a name="zh-cn_topic_0165951356_p1857694417714"></a>严格</p>
        </td>
        <td class="cellrowborder" valign="top" width="71.15%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0165951356_p55766441379"><a name="zh-cn_topic_0165951356_p55766441379"></a><a name="zh-cn_topic_0165951356_p55766441379"></a>防护粒度最精细，可以拦截具有复杂的绕过特征的攻击请求。</p>
        <p id="zh-cn_topic_0165951356_p42472517104"><a name="zh-cn_topic_0165951356_p42472517104"></a><a name="zh-cn_topic_0165951356_p42472517104"></a>当需要更严格地防护SQL注入、跨站脚本、命令注入等攻击行为时，建议使用<span class="parmvalue" id="zh-cn_topic_0165951356_parmvalue14814484117"><a name="zh-cn_topic_0165951356_parmvalue14814484117"></a><a name="zh-cn_topic_0165951356_parmvalue14814484117"></a>“严格”</span>模式。</p>
        </td>
        </tr>
        </tbody>
        </table>

    2.  防护检测类型设置。

        默认开启“常规检测“防护检测，用户可根据业务需要，参照[表2](#table1054818371898)开启其他需要防护的检测类型。

6.  选择“防护规则“页签，查看Web基础防护规则的详细信息，如[图4](#fig8837434185019)所示，相关参数说明如[表4](#table19135226105218)所示。

    **图 4**  查看防护规则<a name="fig8837434185019"></a>  
    ![](figures/查看防护规则.png "查看防护规则")

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >单击![](figures/icon-paixu.png)，您可以根据“CVE编号“、“危险等级“、“应用类型“或“防护类型“，搜索指定规则。

    **表 4**  防护规则说明

    <a name="table19135226105218"></a>
    <table><thead align="left"><tr id="row1813682605214"><th class="cellrowborder" valign="top" width="25.28%" id="mcps1.2.3.1.1"><p id="p913602645217"><a name="p913602645217"></a><a name="p913602645217"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="74.72%" id="mcps1.2.3.1.2"><p id="p19136126125217"><a name="p19136126125217"></a><a name="p19136126125217"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row171361526115216"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p11136122615218"><a name="p11136122615218"></a><a name="p11136122615218"></a>规则ID</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p21367263523"><a name="p21367263523"></a><a name="p21367263523"></a>防护规则的ID，由系统自动生成。</p>
    </td>
    </tr>
    <tr id="row678613065320"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p96722675319"><a name="p96722675319"></a><a name="p96722675319"></a>规则描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p15672156185319"><a name="p15672156185319"></a><a name="p15672156185319"></a>防护规则对应的攻击详细描述。</p>
    </td>
    </tr>
    <tr id="row1213782612529"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p16137112665214"><a name="p16137112665214"></a><a name="p16137112665214"></a>CVE编号</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p15816113315363"><a name="p15816113315363"></a><a name="p15816113315363"></a>防护规则对应的CVE（Common Vulnerabilities &amp; Exposures，通用漏洞披露）编号。对于非CVE漏洞，显示为--。</p>
    </td>
    </tr>
    <tr id="row10137226195213"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p11137326165210"><a name="p11137326165210"></a><a name="p11137326165210"></a>危险等级</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p113732613525"><a name="p113732613525"></a><a name="p113732613525"></a>防护规则防护漏洞的危险等级，包括：</p>
    <a name="ul17258349201"></a><a name="ul17258349201"></a><ul id="ul17258349201"><li>高危</li><li>中危</li><li>低危</li></ul>
    </td>
    </tr>
    <tr id="row1137122612524"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p7137426165217"><a name="p7137426165217"></a><a name="p7137426165217"></a>应用类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p2137526125219"><a name="p2137526125219"></a><a name="p2137526125219"></a>防护规则对应的应用类型，例如，WordPress。</p>
    </td>
    </tr>
    <tr id="row8138122611524"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p1113892675219"><a name="p1113892675219"></a><a name="p1113892675219"></a>防护类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p3138202610529"><a name="p3138202610529"></a><a name="p3138202610529"></a>防护规则的类型，例如，命令注入。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 防护效果<a name="section1773143201419"></a>

假如已添加域名“www.example.com“，且已开启了Web基础防护的“常规检测“，防护模式为“拦截“。您可以参照以下步骤验证WAF防护效果：

1.  清理浏览器缓存，在浏览器中输入防护域名，测试网站域名是否能正常访问。
    -   不能正常访问，参照[步骤三：域名接入配置](步骤三-域名接入配置.md)章节重新完成域名接入。
    -   能正常访问，执行[2](#li2057953372517)。

2.  <a name="li2057953372517"></a>清理浏览器缓存，在浏览器中输入“http://www.example.com?id=1%27%20or%201=1“模拟SQL注入攻击。
3.  返回Web应用防火墙控制界面，在左侧导航树中，单击“防护事件“，进入“防护事件“页面，查看防护域名拦截日志，您也可以[下载防护事件数据](下载防护事件数据.md)。

## 配置示例-拦截SQL注入攻击<a name="section1358382112810"></a>

模拟SQL攻击，查看WAF是否拦截该请求。

在Web主机上执行以下命令，模拟SQL注入查看是否拦截该请求。

**curl -kv "http://www.example.com?id=1 or 1=1"**

如果WAF拦截成功，拦截页面如下所示，返回状态码：418。

![](figures/最佳实践11.png)

