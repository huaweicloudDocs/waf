# 添加防护网站（ELB模式）<a name="waf_01_0287"></a>

如果您的业务服务器部署在华为云，您可以使用ELB模式将网站的域名或IP添加到WAF，使网站流量切入WAF进行防护。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果您已开通企业项目，您可以在“企业项目“下拉列表中选择您所在的企业项目，在该企业项目下添加防护网站。

## 前提条件<a name="section2256777914731"></a>

-   已购买WAF的云模式。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   ELB模式需要[提交工单](https://support.huaweicloud.com/usermanual-ticket/zh-cn_topic_0127038618.html)申请开通后才能使用，支持使用的Region请参考[功能总览](https://support.huaweicloud.com/function-waf/index.html)。
    >-   购买了云模式标准版、专业版或铂金版后，同时可以使用ELB模式，域名、QPS、规则扩展包的配额与云模式共用。

-   已购买独享型负载均衡，且“规格“为“应用型（HTTP/HTTPS）“，详见[创建独享型负载均衡器](https://support.huaweicloud.com/usermanual-elb/elb_lb_000006.html)。

## 约束限制<a name="section17619121118252"></a>

仅支持与独享型ELB配套使用，且“规格“必须为“应用型（HTTP/HTTPS）“，不支持“网络型（TCP/UDP）“的独享型的ELB。

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
</tbody>
</table>

## 操作步骤<a name="section1188181654517"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  单击管理控制台左上角的![](figures/icon-region-82.jpg)，选择区域或项目。
3.  单击页面左上方的![](figures/icon-Service-83.png)，选择“安全与合规  \>  Web应用防火墙 WAF“。
4.  在网站列表左上角，单击“添加防护网站“。
5.  选择“ELB模式“后，在页面配置域名基本信息，如[图1](#fig175731754141418)所示，相关参数说明如[表2](#table7692122554811)所示。

    **图 1**  配置防护网站基本信息<a name="fig175731754141418"></a>  
    ![](figures/配置防护网站基本信息.png "配置防护网站基本信息")

    **表 2**  基本信息参数说明

    <a name="table7692122554811"></a>
    <table><thead align="left"><tr id="row1068752517484"><th class="cellrowborder" valign="top" width="20.71%" id="mcps1.2.4.1.1"><p id="p768742524817"><a name="p768742524817"></a><a name="p768742524817"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="58.5%" id="mcps1.2.4.1.2"><p id="p1168782534812"><a name="p1168782534812"></a><a name="p1168782534812"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.79%" id="mcps1.2.4.1.3"><p id="p12687162544815"><a name="p12687162544815"></a><a name="p12687162544815"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row86189206236"><td class="cellrowborder" valign="top" width="20.71%" headers="mcps1.2.4.1.1 "><p id="p161822018235"><a name="p161822018235"></a><a name="p161822018235"></a>ELB（负载均衡器）</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.5%" headers="mcps1.2.4.1.2 "><p id="p1015244710509"><a name="p1015244710509"></a><a name="p1015244710509"></a>在下拉框中选择ELB。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.79%" headers="mcps1.2.4.1.3 "><p id="p461892052313"><a name="p461892052313"></a><a name="p461892052313"></a>elb-waf-test</p>
    </td>
    </tr>
    <tr id="row139372527235"><td class="cellrowborder" valign="top" width="20.71%" headers="mcps1.2.4.1.1 "><p id="p7132125622311"><a name="p7132125622311"></a><a name="p7132125622311"></a>ELB监听器</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.5%" headers="mcps1.2.4.1.2 "><a name="ul1040253919257"></a><a name="ul1040253919257"></a><ul id="ul1040253919257"><li><span class="parmvalue" id="parmvalue2036192417264"><a name="parmvalue2036192417264"></a><a name="parmvalue2036192417264"></a>“所有监听器”</span></li><li><span class="parmvalue" id="parmvalue101061627182619"><a name="parmvalue101061627182619"></a><a name="parmvalue101061627182619"></a>“指定监听器”</span>，在下拉框中选择指定的监听器。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="20.79%" headers="mcps1.2.4.1.3 "><p id="p199371452102312"><a name="p199371452102312"></a><a name="p199371452102312"></a>所有监听器</p>
    </td>
    </tr>
    <tr id="row19309057618"><td class="cellrowborder" valign="top" width="20.71%" headers="mcps1.2.4.1.1 "><p id="p2179125255914"><a name="p2179125255914"></a><a name="p2179125255914"></a>网站名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.5%" headers="mcps1.2.4.1.2 "><p id="p191791952195918"><a name="p191791952195918"></a><a name="p191791952195918"></a>网站的名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.79%" headers="mcps1.2.4.1.3 "><p id="p617945225915"><a name="p617945225915"></a><a name="p617945225915"></a>-</p>
    </td>
    </tr>
    <tr id="row1368718254486"><td class="cellrowborder" valign="top" width="20.71%" headers="mcps1.2.4.1.1 "><p id="p368762516486"><a name="p368762516486"></a><a name="p368762516486"></a>防护域名</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.5%" headers="mcps1.2.4.1.2 "><p id="p168710252489"><a name="p168710252489"></a><a name="p168710252489"></a>防护的域名或IP，域名支持单域名和泛域名。</p>
    <a name="ul9206119142513"></a><a name="ul9206119142513"></a><ul id="ul9206119142513"><li>单域名：输入防护的单域名。例如：www.example.com。</li><li>泛域名<div class="note" id="waf_01_0250_note149522717141"><a name="waf_01_0250_note149522717141"></a><a name="waf_01_0250_note149522717141"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="waf_01_0250_p949632718144"><a name="waf_01_0250_p949632718144"></a><a name="waf_01_0250_p949632718144"></a>WAF不支持添加带有下划线（_）的泛域名。</p>
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
    <tr id="row999016126617"><td class="cellrowborder" valign="top" width="20.71%" headers="mcps1.2.4.1.1 "><p id="p738462712012"><a name="p738462712012"></a><a name="p738462712012"></a>网站备注</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.5%" headers="mcps1.2.4.1.2 "><p id="p193849271909"><a name="p193849271909"></a><a name="p193849271909"></a>网站补充信息。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.79%" headers="mcps1.2.4.1.3 "><p id="p1638418275018"><a name="p1638418275018"></a><a name="p1638418275018"></a>-</p>
    </td>
    </tr>
    <tr id="row1192175711538"><td class="cellrowborder" valign="top" width="20.71%" headers="mcps1.2.4.1.1 "><p id="p131926571535"><a name="p131926571535"></a><a name="p131926571535"></a>策略配置</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.5%" headers="mcps1.2.4.1.2 "><p id="p1919275714537"><a name="p1919275714537"></a><a name="p1919275714537"></a>默认为<span class="parmvalue" id="parmvalue4588521113112"><a name="parmvalue4588521113112"></a><a name="parmvalue4588521113112"></a>“系统自动生成策略”</span>，您也可以选择已创建的防护策略或在域名接入后根据防护需求配置防护规则。</p>
    <p id="p18562141019311"><a name="p18562141019311"></a><a name="p18562141019311"></a>系统自动生成的策略说明如下：</p>
    <a name="ul25621710153112"></a><a name="ul25621710153112"></a><ul id="ul25621710153112"><li>Web基础防护（<span class="parmname" id="parmname35621410143113"><a name="parmname35621410143113"></a><a name="parmname35621410143113"></a>“仅记录”</span>模式、常规检测）<p id="p0562110143116"><a name="p0562110143116"></a><a name="p0562110143116"></a>仅记录SQL注入、XSS跨站脚本、远程溢出攻击、文件包含、Bash漏洞攻击、远程命令执行、目录遍历、敏感文件访问、命令/代码注入等攻击行为。</p>
    </li><li>网站反爬虫（<span class="parmname" id="parmname205621210183119"><a name="parmname205621210183119"></a><a name="parmname205621210183119"></a>“仅记录”</span>模式、扫描器）<p id="p1562810123119"><a name="p1562810123119"></a><a name="p1562810123119"></a>仅记录漏洞扫描、病毒扫描等Web扫描任务，如OpenVAS、Nmap的爬虫行为。</p>
    </li></ul>
    <div class="note" id="note155627106319"><a name="note155627106319"></a><a name="note155627106319"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p25626108314"><a name="p25626108314"></a><a name="p25626108314"></a><span class="parmname" id="parmname75623105311"><a name="parmname75623105311"></a><a name="parmname75623105311"></a>“仅记录”</span>模式：发现攻击行为后WAF只记录攻击事件不阻断攻击。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="20.79%" headers="mcps1.2.4.1.3 "><p id="p619275765317"><a name="p619275765317"></a><a name="p619275765317"></a>系统自动生成策略</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“确认“，防护网站添加成功。

    您可在防护网站列表中查看已添加防护网站。

## 生效条件<a name="section144961343101710"></a>

防护网站的初始“接入状态“为“未接入“，当访问请求到达该网站的WAF时，该防护网站的接入状态将自动切换为“已接入“。

