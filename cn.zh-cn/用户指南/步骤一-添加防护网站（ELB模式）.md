# 步骤一：添加防护网站（ELB模式）<a name="waf_01_0287"></a>

如果您的业务服务器部署在华为云上，您可以将网站的域名或IP添加到WAF，使网站流量切入WAF。

>![](public_sys-resources/icon-notice.gif) **须知：** 
>当前“华北-北京二“和“华北-北京四“区域支持ELB模式。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果您已开通企业项目，您可以在“企业项目“下拉列表中选择您所在的企业项目，在该企业项目下添加防护网站。

## 前提条件<a name="section2256777914731"></a>

已购买ELB模式实例。

## 约束条件<a name="section1044320443914"></a>

请确保防护域名经过ICP备案，未备案域名将无法正常使用WAF。

## 收集防护域名/IP的配置信息<a name="section12606124331017"></a>

在添加防护域名/IP前，请获取防护域名/IP如[表1](#table1252463519439)所示相关信息。

**表 1**  准备防护域名/IP相关信息

<a name="table1252463519439"></a>
<table><thead align="left"><tr id="row17524133512433"><th class="cellrowborder" valign="top" width="20.14%" id="mcps1.2.4.1.1"><p id="p10524135174313"><a name="p10524135174313"></a><a name="p10524135174313"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="45.98%" id="mcps1.2.4.1.2"><p id="p127760511629"><a name="p127760511629"></a><a name="p127760511629"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="33.879999999999995%" id="mcps1.2.4.1.3"><p id="p149321743162415"><a name="p149321743162415"></a><a name="p149321743162415"></a>示例</p>
</th>
</tr>
</thead>
<tbody><tr id="row165241835174314"><td class="cellrowborder" valign="top" width="20.14%" headers="mcps1.2.4.1.1 "><p id="p20512145819416"><a name="p20512145819416"></a><a name="p20512145819416"></a>域名/IP</p>
</td>
<td class="cellrowborder" valign="top" width="45.98%" headers="mcps1.2.4.1.2 "><a name="ul6619122055017"></a><a name="ul6619122055017"></a><ul id="ul6619122055017"><li>域名：由一串用点分隔的英文字母组成（以字符串的形式来表示服务器IP），用户通过域名来访问网站。</li><li>IP：访问网站所使用的IP地址。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="33.879999999999995%" headers="mcps1.2.4.1.3 "><p id="p16933943172410"><a name="p16933943172410"></a><a name="p16933943172410"></a>www.example.com</p>
</td>
</tr>
<tr id="row93691515163314"><td class="cellrowborder" valign="top" width="20.14%" headers="mcps1.2.4.1.1 "><p id="p20512958541"><a name="p20512958541"></a><a name="p20512958541"></a>标准端口/非标准端口</p>
</td>
<td class="cellrowborder" valign="top" width="45.98%" headers="mcps1.2.4.1.2 "><p id="p81411753417"><a name="p81411753417"></a><a name="p81411753417"></a>需要防护的域名对应的业务端口。</p>
<a name="ul214111516416"></a><a name="ul214111516416"></a><ul id="ul214111516416"><li>标准端口<a name="ul514195848"></a><a name="ul514195848"></a><ul id="ul514195848"><li>80：HTTP对外协议默认使用端口</li><li>443：HTTPS对外协议默认使用端口</li></ul>
</li><li>非标准端口<p id="p141411159416"><a name="p141411159416"></a><a name="p141411159416"></a>80/443以外的端口，ELB上配置的监听器端口保持一致</p>
<div class="notice" id="note131421058410"><a name="note131421058410"></a><a name="note131421058410"></a><span class="noticetitle"> 须知： </span><div class="noticebody"><p id="p814215514415"><a name="p814215514415"></a><a name="p814215514415"></a>如果防护域名使用非标准端口，请查看<a href="https://support.huaweicloud.com/waf_faq/waf_01_0032.html" target="_blank" rel="noopener noreferrer">WAF支持哪些非标准端口？</a>，确保购买的WAF版本支持防护该非标准端口。</p>
</div></div>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="33.879999999999995%" headers="mcps1.2.4.1.3 "><p id="p63591324133318"><a name="p63591324133318"></a><a name="p63591324133318"></a>80</p>
</td>
</tr>
</tbody>
</table>

## 操作步骤<a name="section1188181654517"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入网站设置页面入口，如[图1](#waf_01_0002_fig172535820151)所示。

    **图 1**  网站设置入口<a name="waf_01_0002_fig172535820151"></a>  
    ![](figures/网站设置入口.png "网站设置入口")

3.  在网站列表左上角，单击“添加防护网站“。
4.  选择“ELB模式“后，在页面配置域名基本信息，如[图2](#fig175731754141418)所示，相关参数说明如[表2](#table7692122554811)所示。

    **图 2**  配置防护网站基本信息<a name="fig175731754141418"></a>  
    ![](figures/配置防护网站基本信息.png "配置防护网站基本信息")

    **表 2**  基本信息参数说明

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
    <td class="cellrowborder" valign="top" width="64.21%" headers="mcps1.2.4.1.2 "><p id="p154752625510"><a name="p154752625510"></a><a name="p154752625510"></a>可选参数。必须与ELB上配置的监听器端口保持一致。</p>
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

5.  选择“策略配置“，默认为“系统自动生成策略“。

    您也可以选择已创建的防护策略或在域名接入后根据防护需求配置防护规则。

    系统自动生成的策略说明如下：

    -   Web基础防护（“仅记录“模式、常规检测）

        仅记录SQL注入、XSS跨站脚本、远程溢出攻击、文件包含、Bash漏洞攻击、远程命令执行、目录遍历、敏感文件访问、命令/代码注入等攻击行为。

    -   网站反爬虫（“仅记录“模式、扫描器）

        仅记录漏洞扫描、病毒扫描等Web扫描任务，如OpenVAS、Nmap的爬虫行为。


    >![](public_sys-resources/icon-note.gif) **说明：** 
    >“仅记录“模式：发现攻击行为后WAF只记录攻击事件不阻断攻击。

6.  单击“确定“，防护网站添加成功。

    您可在防护网站列表中查看已添加防护网站。


## 生效条件<a name="section144961343101710"></a>

防护网站的初始“接入状态“为“未接入“，当访问请求到达该网站的WAF时，该防护网站的接入状态将自动切换为“已接入“。

