# 配置IP黑白名单规则<a name="waf_01_0012"></a>

IP地址默认全部放行，您可以通过配置黑白名单规则，阻断、仅记录或放行指定IP地址/IP地址段的访问请求。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果您已开通企业项目，您需要在“企业项目“下拉列表中选择您所在的企业项目并确保已开通操作权限，才能为该企业项目下域名配置防护策略。

## 前提条件<a name="section5903171661012"></a>

已添加防护网站。

## 约束条件<a name="section17458916115210"></a>

-   检测版不支持该功能。
-   WAF支持批量导入黑白名单，如果您需要配置多个IP/IP地址段规则，请添加地址组，详细操作请参见[添加黑白名单IP地址组](添加黑白名单IP地址组.md)。
-   添加或修改防护规则后，规则生效需要等待几分钟。规则生效后，您可以在“防护事件“页面查看防护效果。
-   WAF黑白名单规则不支持配置0.0.0.0/0 IP地址段，且白名单规则优先级高于黑名单规则。如果您需要放行某个网段指定的IP并拦截某个网段其他所有IP，请先添加黑名单规则，拦截将该网段的所有IP，然后添加白名单规则，放行指定IP。

    >![](public_sys-resources/icon-notice.gif) **须知：** 
    >如果您需要拦截所有来源IP或仅允许指定IP访问防护网站，请参见[拦截所有来源IP或仅允许指定IP访问防护网站，如何配置？](https://support.huaweicloud.com/waf_faq/waf_01_0312.html)进行配置。

-   当黑白名单规则的“防护动作“设置为“拦截“时，您可以[配置攻击惩罚标准](配置攻击惩罚标准.md)。配置攻击惩罚后，如果访问者的IP、Cookie或Params恶意请求被拦截时，WAF将根据攻击惩罚设置的拦截时长来封禁访问者。

## 规格限制<a name="section1268362217284"></a>

-   云模式各版本、独享模式和ELB模式支持创建的IP黑白名单规则条数请参见[服务版本差异](https://support.huaweicloud.com/productdesc-waf/waf_01_0106.html#section1)。
-   如果您购买了云模式，当前版本的IP黑白名单防护规则条数不能满足要求时，您可以通过购买规则扩展包或升级云模式版本增加IP黑白名单防护规则条数，以满足的防护配置需求。

    一个规则扩展包包含10条IP黑白名单防护规则。有关升级规则的详细操作，请参见[升级WAF云模式版本和规格](https://support.huaweicloud.com/usermanual-waf/waf_01_0114.html)。


## 系统影响<a name="section298020596537"></a>

将IP或IP地址段配置为黑名单/白名单后，来自该IP或IP地址段的访问，WAF将不会做任何检测，直接拦截/放行。

## 操作步骤<a name="section61533550183130"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入防护策略配置入口，如[图1](#waf_01_0008_fig089771664710)所示。

    **图 1**  防护策略配置入口<a name="waf_01_0008_fig089771664710"></a>  
    ![](figures/防护策略配置入口.png "防护策略配置入口")

3.  在“黑白名单设置“配置框中，用户可根据自己的需要更改“状态“，单击“自定义黑白名单设置规则“，进入黑白名单设置规则页面，如[图2](#fig0358162863015)所示。

    **图 2**  黑白名单配置框<a name="fig0358162863015"></a>  
    ![](figures/黑白名单配置框.png "黑白名单配置框")

4.  在“黑白名单“设置规则页面左上角，单击“添加规则“。
5.  在弹出的对话框中，添加黑白名单规则，如[图3](#fig1810352211544)和[图4](#fig1936217171553)所示，参数说明如[表1](#table147241231818)所示。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   将IP配置为仅记录后，来自该IP的访问，WAF将根据防护规则进行检测并记录该IP的防护事件数据。
    >-   其他的IP将根据配置的WAF防护规则进行检测。

    **图 3**  添加单个IP/IP地址段黑白名单规则<a name="fig1810352211544"></a>  
    ![](figures/添加单个IP-IP地址段黑白名单规则.png "添加单个IP-IP地址段黑白名单规则")

    **图 4**  批量添加IP/IP地址段黑白名单规则<a name="fig1936217171553"></a>  
    ![](figures/批量添加IP-IP地址段黑白名单规则.png "批量添加IP-IP地址段黑白名单规则")

    **表 1**  黑白名单参数说明

    <a name="table147241231818"></a>
    <table><thead align="left"><tr id="row167071221814"><th class="cellrowborder" valign="top" width="18.81188118811881%" id="mcps1.2.4.1.1"><p id="p1770171261818"><a name="p1770171261818"></a><a name="p1770171261818"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="35.913591359135914%" id="mcps1.2.4.1.2"><p id="p1770131241814"><a name="p1770131241814"></a><a name="p1770131241814"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="45.274527452745275%" id="mcps1.2.4.1.3"><p id="p177012124180"><a name="p177012124180"></a><a name="p177012124180"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row17828105919582"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.4.1.1 "><p id="p1231110155913"><a name="p1231110155913"></a><a name="p1231110155913"></a>规则名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.913591359135914%" headers="mcps1.2.4.1.2 "><p id="p922513376589"><a name="p922513376589"></a><a name="p922513376589"></a>用户自定义黑白名单规则的名字。</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.274527452745275%" headers="mcps1.2.4.1.3 "><p id="p1722516371587"><a name="p1722516371587"></a><a name="p1722516371587"></a>waftest</p>
    </td>
    </tr>
    <tr id="row188736565586"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.4.1.1 "><p id="p1123191065914"><a name="p1123191065914"></a><a name="p1123191065914"></a>IP/IP段或地址组</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.913591359135914%" headers="mcps1.2.4.1.2 "><p id="p3231410125919"><a name="p3231410125919"></a><a name="p3231410125919"></a>支持添加黑白名单规则的方式，<span class="parmvalue" id="parmvalue03165378511"><a name="parmvalue03165378511"></a><a name="parmvalue03165378511"></a>“IP/IP段”</span>或<span class="parmvalue" id="parmvalue19756041656"><a name="parmvalue19756041656"></a><a name="parmvalue19756041656"></a>“地址组”</span>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.274527452745275%" headers="mcps1.2.4.1.3 "><p id="p1235109594"><a name="p1235109594"></a><a name="p1235109594"></a>IP/IP段</p>
    </td>
    </tr>
    <tr id="row671212161816"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.4.1.1 "><p id="p17351152520596"><a name="p17351152520596"></a><a name="p17351152520596"></a>IP/IP段</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.913591359135914%" headers="mcps1.2.4.1.2 "><p id="p185931910191212"><a name="p185931910191212"></a><a name="p185931910191212"></a>当<span class="parmname" id="parmname16518131212124"><a name="parmname16518131212124"></a><a name="parmname16518131212124"></a>“IP/IP段或地址组”</span> 选择<span class="parmvalue" id="parmvalue334154621215"><a name="parmvalue334154621215"></a><a name="parmvalue334154621215"></a>“IP/IP段”</span>时需要设置该参数。</p>
    <p id="p123164594811"><a name="p123164594811"></a><a name="p123164594811"></a>支持IPv4和IPv6格式的IP地址或IP地址段。</p>
    <a name="ul16332155911817"></a><a name="ul16332155911817"></a><ul id="ul16332155911817"><li>IP地址：添加黑名单或者白名单的IP地址。</li><li>IP地址段：IP地址与子网掩码。</li></ul>
    <div class="notice" id="note3522103392412"><a name="note3522103392412"></a><a name="note3522103392412"></a><span class="noticetitle"> 须知： </span><div class="noticebody"><p id="waf_01_0002_p9994853161215"><a name="waf_01_0002_p9994853161215"></a><a name="waf_01_0002_p9994853161215"></a>仅专业版（原企业版）和铂金版（原旗舰版）支持IPv6防护，且当前仅<span class="parmname" id="waf_01_0002_parmname29569543318"><a name="waf_01_0002_parmname29569543318"></a><a name="waf_01_0002_parmname29569543318"></a>“华东”</span>和<span class="parmname" id="waf_01_0002_parmname585285171111"><a name="waf_01_0002_parmname585285171111"></a><a name="waf_01_0002_parmname585285171111"></a>“华北”</span>区域支持IPv4/IPv6双栈和NAT64。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="45.274527452745275%" headers="mcps1.2.4.1.3 "><a name="ul20137241191011"></a><a name="ul20137241191011"></a><ul id="ul20137241191011"><li>IPv4格式：<a name="ul2071625551110"></a><a name="ul2071625551110"></a><ul id="ul2071625551110"><li>192.168.2.3</li><li>10.1.1.0/24</li></ul>
    </li><li>IPv6格式：1050:0:0:0:5:600:300c:326b</li></ul>
    </td>
    </tr>
    <tr id="row2935529135819"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.4.1.1 "><p id="p20936142916581"><a name="p20936142916581"></a><a name="p20936142916581"></a>选择地址组</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.913591359135914%" headers="mcps1.2.4.1.2 "><p id="p189361029145813"><a name="p189361029145813"></a><a name="p189361029145813"></a>当<span class="parmname" id="parmname228581865"><a name="parmname228581865"></a><a name="parmname228581865"></a>“IP/IP段或地址组”</span> 选择<span class="parmvalue" id="parmvalue852762015610"><a name="parmvalue852762015610"></a><a name="parmvalue852762015610"></a>“地址组”</span>时需要设置该参数，在下拉列表框中选择已添加的地址组。您也可以单击<span class="uicontrol" id="uicontrol128675020117"><a name="uicontrol128675020117"></a><a name="uicontrol128675020117"></a>“添加地址组”</span>创建新的地址组，详细操作请参见<a href="添加黑白名单IP地址组.md">添加黑白名单IP地址组</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.274527452745275%" headers="mcps1.2.4.1.3 "><p id="p19936229205811"><a name="p19936229205811"></a><a name="p19936229205811"></a>groupwaf</p>
    </td>
    </tr>
    <tr id="row127111201815"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.4.1.1 "><p id="p12711312181819"><a name="p12711312181819"></a><a name="p12711312181819"></a>防护动作</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.913591359135914%" headers="mcps1.2.4.1.2 "><a name="ul14238171916485"></a><a name="ul14238171916485"></a><ul id="ul14238171916485"><li>拦截：IP地址或IP地址段设置的是黑名单且需要拦截，则选择<span class="parmvalue" id="parmvalue6397121214419"><a name="parmvalue6397121214419"></a><a name="parmvalue6397121214419"></a>“拦截”</span>。</li><li>放行：IP地址或IP地址段设置的是白名单，则选择<span class="parmvalue" id="parmvalue54671933741"><a name="parmvalue54671933741"></a><a name="parmvalue54671933741"></a>“放行”</span>。</li><li>仅记录：需要观察的IP地址或IP地址段，可选择<span class="parmvalue" id="parmvalue17429739153"><a name="parmvalue17429739153"></a><a name="parmvalue17429739153"></a>“仅记录”</span>。再根据<a href="下载防护事件数据.md">防护事件数据</a>判断该IP地址或IP地址段是黑名单还是白名单。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="45.274527452745275%" headers="mcps1.2.4.1.3 "><p id="p371181215184"><a name="p371181215184"></a><a name="p371181215184"></a>拦截</p>
    </td>
    </tr>
    <tr id="row145743412307"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.4.1.1 "><p id="p957518413304"><a name="p957518413304"></a><a name="p957518413304"></a>攻击惩罚</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.913591359135914%" headers="mcps1.2.4.1.2 "><p id="p8575441133012"><a name="p8575441133012"></a><a name="p8575441133012"></a>当<span class="parmname" id="parmname4871820183218"><a name="parmname4871820183218"></a><a name="parmname4871820183218"></a>“防护动作”</span>设置为<span class="parmvalue" id="parmvalue12385102333213"><a name="parmvalue12385102333213"></a><a name="parmvalue12385102333213"></a>“拦截”</span>时，您可以设置攻击惩罚标准。设置攻击惩罚后，当访问者的IP、Cookie或Params恶意请求被拦截时，WAF将根据惩罚标准设置的拦截时长来封禁访问者。</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.274527452745275%" headers="mcps1.2.4.1.3 "><p id="p105756414304"><a name="p105756414304"></a><a name="p105756414304"></a>长时间IP拦截</p>
    </td>
    </tr>
    <tr id="row147241221818"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.2.4.1.1 "><p id="p171712171819"><a name="p171712171819"></a><a name="p171712171819"></a>规则描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="35.913591359135914%" headers="mcps1.2.4.1.2 "><p id="p37161201817"><a name="p37161201817"></a><a name="p37161201817"></a>可选参数，设置该规则的备注信息。</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.274527452745275%" headers="mcps1.2.4.1.3 "><p id="p20711122182"><a name="p20711122182"></a><a name="p20711122182"></a>--</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  输入完成后，单击“确认添加“，添加的黑白名单展示在黑白名单规则列表中。

    **图 5**  黑白名单规则列表<a name="fig1737424924319"></a>  
    ![](figures/黑白名单规则列表.png "黑白名单规则列表")

    -   规则添加成功后，默认的“规则状态“为“已开启“，若您暂时不想使该规则生效，可在目标规则所在行的“操作“列，单击“关闭“。
    -   若需要修改添加的黑白名单规则时，可单击待修改的黑白名单IP规则所在行的“修改“，修改黑白名单规则。
    -   若需要删除添加的黑白名单规则时，可单击待删除的黑白名单IP规则所在行的“删除“，删除黑白名单规则。


## 配置示例-放行指定IP<a name="section15908758104916"></a>

假如防护域名“www.example.com“已接入WAF，您可以参照以下操作步骤验证放行指定IP防护效果。

1.  添加以下2条黑白名单规则，拦截所有来源IP。

    **图 6**  拦截1.0.0.0/1 IP地址段<a name="fig134723543536"></a>  
    ![](figures/拦截1-0-0-0-1-IP地址段.png "拦截1-0-0-0-1-IP地址段")

    **图 7**  拦截128.0.0.0/1 IP地址段<a name="fig13996155195418"></a>  
    ![](figures/拦截128-0-0-0-1-IP地址段.png "拦截128-0-0-0-1-IP地址段")

    您也可以通过添加一条精准访问防护规则，拦截所有访问请求，如[图8](#fig489116305597)所示。

    **图 8**  拦截所有访问请求<a name="fig489116305597"></a>  
    ![](figures/拦截所有访问请求.png "拦截所有访问请求")

    有关配置精准访问防护规则的详细介绍，请参见[配置精准访问防护规则](https://support.huaweicloud.com/usermanual-waf/waf_01_0010.html)。

2.  <a name="li839632265215"></a>参照[图9](#fig5519155016115)示例添加黑白名单规则，放行指定IP，例如，XXX.XXX.2.3。

    **图 9**  放行指定IP<a name="fig5519155016115"></a>  
    ![](figures/放行指定IP.png "放行指定IP")

3.  开启黑白名单防护规则。

    **图 10**  黑白名单配置框<a name="fig17586343102616"></a>  
    ![](figures/黑白名单配置框.png "黑白名单配置框")

4.  清理浏览器缓存，在浏览器中访问“http://www.example.com“页面。

    当访问者的源IP不属于[2](#li839632265215)中设置的放行IP地址时，WAF将拦截该访问请求，拦截页面示例如[图11](#fig11778435913)所示。

    **图 11**  WAF拦截攻击请求<a name="fig11778435913"></a>  
    ![](figures/WAF拦截攻击请求.png "WAF拦截攻击请求")

5.  返回Web应用防火墙管理控制台，在左侧导航树中，单击“防护事件“，进入“防护事件“页面，您可以查看该防护事件。

