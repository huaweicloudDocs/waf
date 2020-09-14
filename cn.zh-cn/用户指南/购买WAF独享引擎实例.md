# 购买WAF独享引擎实例<a name="waf_01_0248"></a>

如果您的业务服务器部署在华为云上，您可以通过购买WAF独享引擎实例对重要的域名或仅有IP的Web服务进行防护。

WAF独享引擎支持按需计费模式，按使用时长收费。独享引擎实例规格不能修改。

>![](public_sys-resources/icon-notice.gif) **须知：** 
>创建实例大约需要5分钟。当实例的运行状态为“运行中“时，说明实例已经创建成功。

## 前提条件<a name="zh-cn_topic_0110861189_section5331623210436"></a>

已获取管理控制台的登录账号（拥有WAF Administrator与BSS Administrator权限）与密码。

## 操作步骤<a name="section107981217568"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入立即购买入口，如[图1](#zh-cn_topic_0110861189_fig1521873317493)所示。

    **图 1**  立即购买入口-独享模式<a name="zh-cn_topic_0110861189_fig1521873317493"></a>  
    ![](figures/立即购买入口-独享模式.png "立即购买入口-独享模式")

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >[图1](#zh-cn_topic_0110861189_fig1521873317493)为首次购买WAF独享引擎实例入口。当您重新购买WAF独享引擎实例时，请参照以下步骤进入购买入口：
    >1.  单击页面左上方的![](figures/icon-Service.png)，选择“安全  \>  Web应用防火墙 WAF“。
    >2.  在界面右上角，单击“购买独享引擎“。

3.  在“购买Web应用防火墙“界面，配置WAF实例参数，如[图2](#zh-cn_topic_0110861189_fig5029231715163)所示，相关参数说明如[表1](#zh-cn_topic_0161005736_table4295843716304)所示。

    **图 2**  配置WAF独享引擎实例<a name="zh-cn_topic_0110861189_fig5029231715163"></a>  
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
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p690274525910"><a name="p690274525910"></a><a name="p690274525910"></a>支持购买WAF的区域：华东-上海二、华北-北京一、华北-北京四、华南-广州、亚太-香港、亚太-曼谷。</p>
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
    </td>
    </tr>
    <tr id="zh-cn_topic_0161005736_row16837105815489"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0161005736_p29202425163143"><a name="zh-cn_topic_0161005736_p29202425163143"></a><a name="zh-cn_topic_0161005736_p29202425163143"></a>规格</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p958111582086"><a name="p958111582086"></a><a name="p958111582086"></a>选择实例的规格。</p>
    </td>
    </tr>
    <tr id="row195202055162711"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="p45211555102711"><a name="p45211555102711"></a><a name="p45211555102711"></a>虚拟私有云</p>
    </td>
    <td class="cellrowborder" valign="top" width="80.86%" headers="mcps1.2.3.1.2 "><p id="p197501314299"><a name="p197501314299"></a><a name="p197501314299"></a>选择源站所在的VPC。</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0161005736_row2550998316304"><td class="cellrowborder" valign="top" width="19.139999999999997%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0161005736_p5304271416304"><a name="zh-cn_topic_0161005736_p5304271416304"></a><a name="zh-cn_topic_0161005736_p5304271416304"></a>业务网卡</p>
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

4.  确认参数配置无误后，在页面右下角单击“立即购买“。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >如果您对价格有疑问，可以单击页面左下角的“了解计费详情“了解产品价格。

5.  确认订单详情无误并阅读《华为云Web应用防火墙免责声明》后，勾选“我已阅读并同意《华为云Web应用防火墙免责声明》“，单击“去支付“，完成购买操作。

1.  进入“付款“页面，选择付款方式进行付款。
2.  成功付款后，单击“返回独享引擎列表“，在独享引擎实例列表界面，可以查看实例的创建情况。

    创建实例大约需要5分钟。当实例的运行状态为“运行中“时，说明实例已经创建成功。


