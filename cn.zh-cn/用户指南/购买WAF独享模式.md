# 购买WAF独享模式<a name="waf_01_0248"></a>

如果您的业务服务器部署在华为云上，您可以通过购买WAF独享引擎实例对重要的域名或仅有IP的Web服务进行防护。购买独享引擎实例后，您还需要为实例配置弹性负载均衡，弹性负载均衡可以通过流量分发扩展应用系统对外的服务能力，同时通过消除单点故障提升应用系统的可用性。

独享模式支持按需计费模式，按使用时长收费。

>![](public_sys-resources/icon-notice.gif) **须知：** 
>购买WAF独享模式前，请确认已[提交工单](https://support.huaweicloud.com/usermanual-ticket/zh-cn_topic_0127038618.html)申请开通独享模式。否则，您将无法购买独享模式实例。

## 前提条件<a name="zh-cn_topic_0110861189_section5331623210436"></a>

-   已获取管理控制台的登录帐号（拥有WAF Administrator/WAF FullAccess与BSS Administrator权限）与密码。
-   已成功创建虚拟私有云VPC。

## 约束条件<a name="section1753081119317"></a>

如果WAF独享引擎实例与源站不在同一个VPC中，需要在安全组中设置实例与源站的子网互通。

>![](public_sys-resources/icon-note.gif) **说明：** 
>有关支持购买WAF的区域说明，请参见[Web应用防火墙支持防护哪些区域？](https://support.huaweicloud.com/waf_faq/waf_01_0101.html)。
>原则上，在任何一个区域购买的WAF支持防护所有区域的Web业务。但是为了提高WAF的转发效率，建议您在购买WAF时，根据防护业务的所在区域就近选择购买的WAF区域。

## 规格限制<a name="section13957152112182"></a>

购买独享引擎实例后，实例规格不能修改。

## 应用场景<a name="section1828463910329"></a>

业务服务器部署在华为云上，防护对象为域名或IP。

大型企业网站，具备较大的业务规模且基于业务特性具有制定个性化防护规则的安全需求。

## 操作步骤<a name="section107981217568"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  单击管理控制台左上角的![](figures/icon-region.jpg)，选择区域或项目。
3.  单击页面左上方的![](figures/icon-Service.png)，选择“安全与合规  \>  Web应用防火墙 WAF“。
4.  首次购买WAF时，在界面左侧，单击“立即购买WAF“。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >再次购买WAF时，请在界面右上角，单击“购买WAF/升级规格“。

5.  （可选）在“企业项目“下拉列表中选择您所在的企业项目。

    企业项目针对企业用户使用，只有开通了企业项目的客户，或者权限为企业主帐号的客户才可见。如需使用该功能，请[开通企业管理功能](https://support.huaweicloud.com/usermanual-em/em_am_0008.html)。企业项目是一种云资源管理方式，企业项目管理服务提供统一的云资源按项目管理，以及项目内的资源管理、成员管理。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   “default“为默认企业项目，帐号下原有资源和未选择企业项目的资源均在默认企业项目内。
    >-   只有注册的华为云帐号购买WAF时，“企业项目“下拉列表中才可以选择到“default“。

6.  在“购买Web应用防火墙“界面，选择“独享模式“。
7.  配置WAF实例参数，如[图1](#zh-cn_topic_0110861189_fig5029231715163)所示，相关参数说明如[表1](#zh-cn_topic_0161005736_table4295843716304)所示。

    **图 1**  配置WAF独享引擎实例<a name="zh-cn_topic_0110861189_fig5029231715163"></a>  
    ![](figures/配置WAF独享引擎实例.png "配置WAF独享引擎实例")

    **表 1**  WAF独享引擎实例参数说明

    <a name="zh-cn_topic_0161005736_table4295843716304"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0161005736_row4338993216304"><th class="cellrowborder" valign="top" width="19.139999999999997%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0161005736_p2492361616304"><a name="zh-cn_topic_0161005736_p2492361616304"></a><a name="zh-cn_topic_0161005736_p2492361616304"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="80.86%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0161005736_p554697916304"><a name="zh-cn_topic_0161005736_p554697916304"></a><a name="zh-cn_topic_0161005736_p554697916304"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1135781814514"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="p17358418175111"><a name="p17358418175111"></a><a name="p17358418175111"></a>区域</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p1317112103519"><a name="p1317112103519"></a><a name="p1317112103519"></a>支持购买WAF独享模式的区域说明，请参见<a href="https://support.huaweicloud.com/waf_faq/waf_01_0101.html" target="_blank" rel="noopener noreferrer">Web应用防火墙支持防护哪些区域？</a>。</p>
    <p id="p378413583591"><a name="p378413583591"></a><a name="p378413583591"></a>原则上，在任何一个区域购买的WAF支持防护所有区域的Web业务。但是为了提高WAF的转发效率，建议您在购买WAF时，根据防护业务的所在区域就近选择购买的WAF区域。</p>
    </td>
    </tr>
    <tr id="row16462181515576"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="p1446316152570"><a name="p1446316152570"></a><a name="p1446316152570"></a>可用区</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p34631315145718"><a name="p34631315145718"></a><a name="p34631315145718"></a>选择区域中的可用区。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0161005736_row3896937416304"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0161005736_p43233810163143"><a name="zh-cn_topic_0161005736_p43233810163143"></a><a name="zh-cn_topic_0161005736_p43233810163143"></a>WAF实例名称前缀</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p12396184383010"><a name="p12396184383010"></a><a name="p12396184383010"></a>设置WAF实例名称前缀，购买多个实例时，实例前缀名称相同。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0161005736_row1319658616304"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0161005736_p12055799163143"><a name="zh-cn_topic_0161005736_p12055799163143"></a><a name="zh-cn_topic_0161005736_p12055799163143"></a>WAF实例数量</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p51329357300"><a name="p51329357300"></a><a name="p51329357300"></a>设置购买的WAF实例个数。</p>
    <p id="p597719211531"><a name="p597719211531"></a><a name="p597719211531"></a>建议至少购买2个WAF实例，并将业务分别部署到WAF实例上。当业务部署多个WAF实例时，如果某个WAF实例发生故障时，WAF会自动将流量切换到其它正在运行的WAF实例上，确保业务正常运行。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0161005736_row16837105815489"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0161005736_p29202425163143"><a name="zh-cn_topic_0161005736_p29202425163143"></a><a name="zh-cn_topic_0161005736_p29202425163143"></a>WAF实例规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p958111582086"><a name="p958111582086"></a><a name="p958111582086"></a>选择实例的规格，支持<span class="parmvalue" id="parmvalue15541152162611"><a name="parmvalue15541152162611"></a><a name="parmvalue15541152162611"></a>“WI-500”</span>和<span class="parmvalue" id="parmvalue48169613265"><a name="parmvalue48169613265"></a><a name="parmvalue48169613265"></a>“WI-100”</span> 。</p>
    </td>
    </tr>
    <tr id="row79021927192615"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="p6903142716261"><a name="p6903142716261"></a><a name="p6903142716261"></a>WAF实例创建类别</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p1124092412273"><a name="p1124092412273"></a><a name="p1124092412273"></a>选择实例的资源类型，相关说明如下：</p>
    <a name="ul1065023020287"></a><a name="ul1065023020287"></a><ul id="ul1065023020287"><li>资源租户类<p id="p0632143220285"><a name="p0632143220285"></a><a name="p0632143220285"></a>WAF实例通过弹性网卡接入用户网络，如果使用ELB接入，仅支持独享型ELB。</p>
    </li><li>普通租户类<p id="p6755344285"><a name="p6755344285"></a><a name="p6755344285"></a>WAF实例将直接创建在用户ECS中，您可以在ECS管理控制台查看创建的WAF实例。</p>
    </li></ul>
    </td>
    </tr>
    <tr id="row68111281274"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="p5811828871"><a name="p5811828871"></a><a name="p5811828871"></a>CPU架构</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p98110281073"><a name="p98110281073"></a><a name="p98110281073"></a>选择实例的CPU架构。</p>
    </td>
    </tr>
    <tr id="row1319318472611"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="p7194147968"><a name="p7194147968"></a><a name="p7194147968"></a>ECS规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p191941347363"><a name="p191941347363"></a><a name="p191941347363"></a>选择实例的ECS规格。</p>
    </td>
    </tr>
    <tr id="row195202055162711"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="p45211555102711"><a name="p45211555102711"></a><a name="p45211555102711"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p197501314299"><a name="p197501314299"></a><a name="p197501314299"></a>选择源站所在的VPC。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0161005736_row2550998316304"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0161005736_p5304271416304"><a name="zh-cn_topic_0161005736_p5304271416304"></a><a name="zh-cn_topic_0161005736_p5304271416304"></a>子网</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0161005736_p6040559116304"><a name="zh-cn_topic_0161005736_p6040559116304"></a><a name="zh-cn_topic_0161005736_p6040559116304"></a>选择VPC中已配置的子网。</p>
    </td>
    </tr>
    <tr id="row1513920102816"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="p2013420142819"><a name="p2013420142819"></a><a name="p2013420142819"></a>安全组</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p740123717124"><a name="p740123717124"></a><a name="p740123717124"></a>选择区域中已有的安全组，或者单击<span class="uicontrol" id="uicontrol95163951615"><a name="uicontrol95163951615"></a><a name="uicontrol95163951615"></a>“管理安全组”</span>，跳转到VPC管理控制台创建新的安全组。选择安全组后，该实例将受到该安全组访问规则的保护。</p>
    <div class="notice" id="note1475493351420"><a name="note1475493351420"></a><a name="note1475493351420"></a><span class="noticetitle"> 须知： </span><div class="noticebody"><p id="p8754833121413"><a name="p8754833121413"></a><a name="p8754833121413"></a>如果WAF独享引擎实例与源站不在同一个VPC中，需要在安全组中设置实例与源站的子网互通。</p>
    </div></div>
    </td>
    </tr>
    </tbody>
    </table>

8.  确认参数配置无误后，在页面右下角单击“立即购买“。
9.  确认订单详情无误并阅读《华为云Web应用防火墙免责声明》后，勾选“我已阅读并同意《华为云Web应用防火墙免责声明》“，单击“去支付“，完成购买操作。

1.  进入“付款“页面，选择付款方式进行付款。
2.  成功付款后，单击“返回独享引擎列表“，在独享引擎实例列表界面，可以查看实例的创建情况。

## 生效条件<a name="section493711571450"></a>

创建实例大约需要5分钟。当实例的运行状态为“运行中“时，说明实例已经创建成功。

## 相关操作<a name="section16892426616"></a>

[管理独享引擎](管理独享引擎.md)

创建WAF独享引擎实例后，您可以查看实例信息、查看实例的监控信息、升级实例版本以及删除实例。

## WAF通信安全授权<a name="section55301551102314"></a>

如果业务使用WAF独享模式部署方式，直接访问VPC内的数据需要开通相应的安全组规则，而开通相应的安全组规则需要获取用户授权，此授权过程称为通信安全授权。

成功购买WAF独享引擎后，WAF默认开启通信安全授权，即开通如[表2](#table10347925129)所示的安全组规则。

**表 2**  WAF通信安全授权安全组规则

<a name="table10347925129"></a>
<table><thead align="left"><tr id="row3347112513212"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p9347132517213"><a name="p9347132517213"></a><a name="p9347132517213"></a>协议端口</p>
</th>
<th class="cellrowborder" valign="top" width="24.97%" id="mcps1.2.5.1.2"><p id="p63472253213"><a name="p63472253213"></a><a name="p63472253213"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="25.03%" id="mcps1.2.5.1.3"><p id="p334711257211"><a name="p334711257211"></a><a name="p334711257211"></a>源地址</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p18347102513220"><a name="p18347102513220"></a><a name="p18347102513220"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row33471925825"><td class="cellrowborder" colspan="4" valign="top" headers="mcps1.2.5.1.1 mcps1.2.5.1.2 mcps1.2.5.1.3 mcps1.2.5.1.4 "><p id="p634718258219"><a name="p634718258219"></a><a name="p634718258219"></a><strong id="b1637235551513"><a name="b1637235551513"></a><a name="b1637235551513"></a>入方向规则</strong></p>
</td>
</tr>
<tr id="row5347725224"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p33480251323"><a name="p33480251323"></a><a name="p33480251323"></a>TCP: 22</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p153485254219"><a name="p153485254219"></a><a name="p153485254219"></a>IPv4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p183481925527"><a name="p183481925527"></a><a name="p183481925527"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p123489251128"><a name="p123489251128"></a><a name="p123489251128"></a>WAF远程运维</p>
</td>
</tr>
<tr id="row634892513215"><td class="cellrowborder" colspan="4" valign="top" headers="mcps1.2.5.1.1 mcps1.2.5.1.2 mcps1.2.5.1.3 mcps1.2.5.1.4 "><p id="p43484257210"><a name="p43484257210"></a><a name="p43484257210"></a><strong id="b19970518131610"><a name="b19970518131610"></a><a name="b19970518131610"></a>出方向规则</strong></p>
</td>
</tr>
<tr id="row00104851412"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1194818143"><a name="p1194818143"></a><a name="p1194818143"></a>TCP: 9011</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p812484147"><a name="p812484147"></a><a name="p812484147"></a>IPV4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p18124881417"><a name="p18124881417"></a><a name="p18124881417"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p16184811412"><a name="p16184811412"></a><a name="p16184811412"></a>WAF事件日志上报</p>
</td>
</tr>
<tr id="row9998526142"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1375111445161"><a name="p1375111445161"></a><a name="p1375111445161"></a>TCP: 9012</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p19100185201410"><a name="p19100185201410"></a><a name="p19100185201410"></a>IPV4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p17100175215145"><a name="p17100175215145"></a><a name="p17100175215145"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p5100352111410"><a name="p5100352111410"></a><a name="p5100352111410"></a>WAF事件日志上报</p>
</td>
</tr>
<tr id="row184301249111619"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p9431949201610"><a name="p9431949201610"></a><a name="p9431949201610"></a>TCP: 9013</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p0431114917168"><a name="p0431114917168"></a><a name="p0431114917168"></a>IPV4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p13431749111619"><a name="p13431749111619"></a><a name="p13431749111619"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p4245112616392"><a name="p4245112616392"></a><a name="p4245112616392"></a>WAF事件日志上报</p>
</td>
</tr>
<tr id="row1323093818185"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p123063817186"><a name="p123063817186"></a><a name="p123063817186"></a>TCP: 9018</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p13230438101811"><a name="p13230438101811"></a><a name="p13230438101811"></a>IPV4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p172317385181"><a name="p172317385181"></a><a name="p172317385181"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p72311238201812"><a name="p72311238201812"></a><a name="p72311238201812"></a>WAF策略同步</p>
</td>
</tr>
<tr id="row1838622217206"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p638762212014"><a name="p638762212014"></a><a name="p638762212014"></a>TCP: 9019</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p18387132242011"><a name="p18387132242011"></a><a name="p18387132242011"></a>IPV4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p133878223202"><a name="p133878223202"></a><a name="p133878223202"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p49731436164014"><a name="p49731436164014"></a><a name="p49731436164014"></a>WAF心跳日志上报</p>
</td>
</tr>
<tr id="row1099133214208"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p18991032112019"><a name="p18991032112019"></a><a name="p18991032112019"></a>TCP: 4505</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p119917321204"><a name="p119917321204"></a><a name="p119917321204"></a>IPV4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p1499153215200"><a name="p1499153215200"></a><a name="p1499153215200"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1099133214204"><a name="p1099133214204"></a><a name="p1099133214204"></a>WAF策略同步</p>
</td>
</tr>
<tr id="row834864320202"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p2242164662019"><a name="p2242164662019"></a><a name="p2242164662019"></a>TCP: 4506</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p334814392018"><a name="p334814392018"></a><a name="p334814392018"></a>IPV4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p1234813432208"><a name="p1234813432208"></a><a name="p1234813432208"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p13348174316207"><a name="p13348174316207"></a><a name="p13348174316207"></a>WAF策略同步</p>
</td>
</tr>
<tr id="row208816565203"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1488115602010"><a name="p1488115602010"></a><a name="p1488115602010"></a>TCP: 50051</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p088205692019"><a name="p088205692019"></a><a name="p088205692019"></a>IPV4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p11885562203"><a name="p11885562203"></a><a name="p11885562203"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p178805615207"><a name="p178805615207"></a><a name="p178805615207"></a>WAF性能日志上报</p>
</td>
</tr>
<tr id="row614481716213"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1727494042116"><a name="p1727494042116"></a><a name="p1727494042116"></a>TCP: 443</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p914411171210"><a name="p914411171210"></a><a name="p914411171210"></a>IPV4</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p1151895454216"><a name="p1151895454216"></a><a name="p1151895454216"></a>100.125.0.0/16</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p12735132219426"><a name="p12735132219426"></a><a name="p12735132219426"></a>WAF策略同步</p>
</td>
</tr>
</tbody>
</table>

