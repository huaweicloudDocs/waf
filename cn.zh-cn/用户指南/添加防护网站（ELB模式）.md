# 添加防护网站（ELB模式）<a name="waf_01_0287"></a>

如果您的业务服务器部署在华为云上，您可以将网站的域名或IP添加到WAF，使网站流量切入WAF。

>![](public_sys-resources/icon-notice.gif) **须知：** 
>当前仅“华北-北京二“区域支持ELB模式。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果您已开通企业项目，您可以在“企业项目“下拉列表中选择您所在的企业项目，在该企业项目下添加防护网站。

## 前提条件<a name="section2256777914731"></a>

已购买ELB模式实例。

## 操作步骤<a name="section1188181654517"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入网站设置页面入口，如[图1](#waf_01_0002_fig172535820151)所示。

    **图 1**  网站设置入口<a name="waf_01_0002_fig172535820151"></a>  
    ![](figures/网站设置入口.png "网站设置入口")

3.  在网站列表左上角，单击“添加防护网站“。
4.  选择“ELB模式“后，在页面配置域名基本信息，如[图2](#fig175731754141418)所示，相关参数说明如[表1](#table7692122554811)所示。

    **图 2**  配置防护网站基本信息<a name="fig175731754141418"></a>  
    ![](figures/配置防护网站基本信息.png "配置防护网站基本信息")

    **表 1**  基本信息参数说明

    <a name="table7692122554811"></a>
    <table><thead align="left"><tr id="row1068752517484"><th class="cellrowborder" valign="top" width="15%" id="mcps1.2.4.1.1"><p id="p768742524817"><a name="p768742524817"></a><a name="p768742524817"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="64.21%" id="mcps1.2.4.1.2"><p id="p1168782534812"><a name="p1168782534812"></a><a name="p1168782534812"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.79%" id="mcps1.2.4.1.3"><p id="p12687162544815"><a name="p12687162544815"></a><a name="p12687162544815"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1368718254486"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.1 "><p id="p368762516486"><a name="p368762516486"></a><a name="p368762516486"></a>防护域名</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.21%" headers="mcps1.2.4.1.2 "><p id="p168710252489"><a name="p168710252489"></a><a name="p168710252489"></a>防护的域名或IP，域名支持单域名和泛域名。</p>
    <a name="ul9206119142513"></a><a name="ul9206119142513"></a><ul id="ul9206119142513"><li>单域名：输入防护的单域名。例如：www.example.com。</li><li>泛域名<div class="note" id="waf_01_0250_note149522717141"><a name="waf_01_0250_note149522717141"></a><a name="waf_01_0250_note149522717141"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="waf_01_0250_p949632718144"><a name="waf_01_0250_p949632718144"></a><a name="waf_01_0250_p949632718144"></a>泛域名不支持下划线（_）。</p>
    </div></div>
    <a name="waf_01_0250_ul776103520251"></a><a name="waf_01_0250_ul776103520251"></a><ul id="waf_01_0250_ul776103520251"><li>如果各子域名对应的服务器IP地址相同：输入防护的泛域名。例如：子域名a.example.com，b.example.com和c.example.com对应的服务器IP地址相同，可以直接添加泛域名*.example.com。</li><li>如果各子域名对应的服务器IP地址不相同：请将子域名按<span class="parmname" id="waf_01_0250_parmname13761925124915"><a name="waf_01_0250_parmname13761925124915"></a><a name="waf_01_0250_parmname13761925124915"></a>“单域名”</span>方式逐条添加。</li></ul>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="20.79%" headers="mcps1.2.4.1.3 "><p id="p1268714259482"><a name="p1268714259482"></a><a name="p1268714259482"></a>单域名：www.example.com</p>
    <p id="p176877251487"><a name="p176877251487"></a><a name="p176877251487"></a>泛域名：*.example.com</p>
    <p id="p107202112593"><a name="p107202112593"></a><a name="p107202112593"></a>IP：</p>
    <p id="p1054310920596"><a name="p1054310920596"></a><a name="p1054310920596"></a>XXX.XXX.1.1</p>
    </td>
    </tr>
    <tr id="row116884252488"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.1 "><p id="p468762516482"><a name="p468762516482"></a><a name="p468762516482"></a>端口</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.21%" headers="mcps1.2.4.1.2 "><p id="p154752625510"><a name="p154752625510"></a><a name="p154752625510"></a>可选参数。必须与 ELB 上配置的监听器端口保持一致。</p>
    <p id="p8687182544810"><a name="p8687182544810"></a><a name="p8687182544810"></a>当您需要配置除<span class="parmvalue" id="parmvalue36632110559"><a name="parmvalue36632110559"></a><a name="parmvalue36632110559"></a>“80”</span>/<span class="parmvalue" id="parmvalue18661121195514"><a name="parmvalue18661121195514"></a><a name="parmvalue18661121195514"></a>“443”</span>标准端口以外的端口时，勾选<span class="parmname" id="parmname15687162544812"><a name="parmname15687162544812"></a><a name="parmname15687162544812"></a>“非标准端口”</span>进行配置。取值范围为1~65535。</p>
    <div class="note" id="note10406184721615"><a name="note10406184721615"></a><a name="note10406184721615"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p162413442720"><a name="p162413442720"></a><a name="p162413442720"></a>如果配置了非标准端口，访问网站时，需要在网址后面增加非标准端口进行访问，否则访问网站时会出现<a href="https://support.huaweicloud.com/waf_faq/waf_01_0066.html#section0" target="_blank" rel="noopener noreferrer">404错误</a>。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="20.79%" headers="mcps1.2.4.1.3 "><p id="p86881725164816"><a name="p86881725164816"></a><a name="p86881725164816"></a>81</p>
    </td>
    </tr>
    <tr id="row1192175711538"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.1 "><p id="p131926571535"><a name="p131926571535"></a><a name="p131926571535"></a>实例组</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.21%" headers="mcps1.2.4.1.2 "><p id="p1919275714537"><a name="p1919275714537"></a><a name="p1919275714537"></a>选择防护网站绑定的实例组。您可以单击创建实例组，新建新的实例组，有关创建实例组的详细操作，请参见<a href="创建实例组.md">创建实例组</a>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.79%" headers="mcps1.2.4.1.3 "><p id="p619275765317"><a name="p619275765317"></a><a name="p619275765317"></a>waf</p>
    </td>
    </tr>
    </tbody>
    </table>

5.  单击“确定“，防护网站添加成功。

    您可在防护网站列表中查看已添加防护网站。


## 生效条件<a name="section144961343101710"></a>

防护网站的初始“接入状态“为“未接入“，当访问请求到达该网站的WAF时，该防护网站的接入状态将自动切换为“已接入“。

