# 配置Web基础防护规则<a name="waf_01_0008"></a>

该章节指导您通过Web应用防火墙服务灵活配置Web基础防护策略。Web基础防护开启后，可防范SQL注入、XSS跨站脚本、远程溢出攻击、文件包含、Bash漏洞攻击、远程命令执行、目录遍历、敏感文件访问、命令/代码注入等常规的Web攻击，以及可支持Webshell检测、搜索引擎、扫描器、脚本工具、其它爬虫等Web基础防护。

您也可以参考[Web基础防护功能最佳实践](https://support.huaweicloud.com/bestpractice-waf/waf_06_0014.html)了解更多Web基础防护规则的配置信息。

## 前提条件<a name="section2256777914731"></a>

-   已获取管理控制台的账号和密码。
-   已添加防护域名。

## 操作步骤<a name="section61533550183130"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入防护配置入口，如[图1](#fig089771664710)所示。

    **图 1**  防护配置入口<a name="fig089771664710"></a>  
    ![](figures/防护配置入口.png "防护配置入口")

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
    <a name="ul115452316468"></a><a name="ul115452316468"></a><ul id="ul115452316468"><li><a name="image3674828111315"></a><a name="image3674828111315"></a><span><img id="image3674828111315" src="figures/icon-open.png"></span>：开启状态。</li><li><a name="image041610818166"></a><a name="image041610818166"></a><span><img id="image041610818166" src="figures/icon-close.png"></span>：关闭状态。</li></ul>
    </td>
    </tr>
    <tr id="row28096830192825"><td class="cellrowborder" valign="top" width="22.49%" headers="mcps1.2.3.1.1 "><p id="p10384205820363"><a name="p10384205820363"></a><a name="p10384205820363"></a>模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.51%" headers="mcps1.2.3.1.2 "><a name="ul946621183715"></a><a name="ul946621183715"></a><ul id="ul946621183715"><li>拦截：发现攻击行为后立即阻断并记录。</li><li>仅记录：发现攻击行为后只记录不阻断攻击。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

4.  在“Web基础防护“配置框中，单击“高级设置“，进入“Web基础防护“界面，根据您的业务场景，开启合适的防护功能，如[图3](#fig17347539113910)所示，检测项说明如[表2](#table1054818371898)所示。

    **图 3**  Web基础防护<a name="fig17347539113910"></a>  
    ![](figures/Web基础防护.png "Web基础防护")

    默认开启“常规检测“和“扫描器“防护检测，用户可根据业务需要，开启其他需要防护的检测类型。

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
    <tr id="row85491637993"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p185491637293"><a name="p185491637293"></a><a name="p185491637293"></a>搜索引擎</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p45491337791"><a name="p45491337791"></a><a name="p45491337791"></a>搜索引擎执行页面内容爬取任务，如Googlebot、Baiduspider。</p>
    <div class="note" id="note117305214214"><a name="note117305214214"></a><a name="note117305214214"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p11751152172118"><a name="p11751152172118"></a><a name="p11751152172118"></a>如果不开启<span class="parmname" id="parmname253669157"><a name="parmname253669157"></a><a name="parmname253669157"></a>“搜索引擎”</span>，WAF针对谷歌和百度爬虫不会拦截，如果您希望拦截百度爬虫的POST请求，可参照<a href="#section1978194713716">配置示例</a>进行配置。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row2549203710913"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p185492371894"><a name="p185492371894"></a><a name="p185492371894"></a>扫描器</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p14549133716913"><a name="p14549133716913"></a><a name="p14549133716913"></a>执行漏洞扫描、病毒扫描等Web扫描任务，如OpenVAS、Nmap。</p>
    <div class="note" id="note848811414446"><a name="note848811414446"></a><a name="note848811414446"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p144891441134419"><a name="p144891441134419"></a><a name="p144891441134419"></a>开启<span class="parmname" id="parmname984110107454"><a name="parmname984110107454"></a><a name="parmname984110107454"></a>“扫描器”</span>后，WAF将对扫描器爬虫，如OpenVAS、Nmap等进行检测。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row165491737295"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p195495371592"><a name="p195495371592"></a><a name="p195495371592"></a>脚本工具</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p1754912371891"><a name="p1754912371891"></a><a name="p1754912371891"></a>用于执行自动化任务、程序脚本等，如httpclient、okhttp、python程序等。</p>
    <div class="note" id="note18101191317159"><a name="note18101191317159"></a><a name="note18101191317159"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p810271317156"><a name="p810271317156"></a><a name="p810271317156"></a>如果您的应用程序中使用了httpclient、okhttp、python程序等脚本工具，建议您关闭<span class="parmname" id="parmname1810823171716"><a name="parmname1810823171716"></a><a name="parmname1810823171716"></a>“脚本工具”</span>，否则，WAF会将使用了httpclient、okhttp、python程序等脚本工具当成恶意爬虫，拦截该应用程序。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row155491737693"><td class="cellrowborder" valign="top" width="25.28%" headers="mcps1.2.3.1.1 "><p id="p154913372917"><a name="p154913372917"></a><a name="p154913372917"></a>其他爬虫</p>
    </td>
    <td class="cellrowborder" valign="top" width="74.72%" headers="mcps1.2.3.1.2 "><p id="p115498372912"><a name="p115498372912"></a><a name="p115498372912"></a>各类用途的爬虫程序，如站点监控、访问代理、网页分析等。</p>
    <div class="note" id="note685819034715"><a name="note685819034715"></a><a name="note685819034715"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p208591209475"><a name="p208591209475"></a><a name="p208591209475"></a>开启<span class="parmname" id="parmname81318974718"><a name="parmname81318974718"></a><a name="parmname81318974718"></a>“其他爬虫”</span>后，WAF将对各类用途的爬虫程序进行检测。</p>
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

        默认开启“常规检测“和“扫描器“防护检测，用户可根据业务需要，参照[表2](#table1054818371898)开启其他需要防护的检测类型。



## 防护效果<a name="section1773143201419"></a>

假如已添加域名“www.example.com“，且已开启了Web基础防护的“常规检测“，防护模式为“拦截“。您可以参照以下步骤验证WAF防护效果：

1.  清理浏览器缓存，在浏览器中输入防护域名，测试网站域名是否能正常访问。
    -   不能正常访问，参照[域名接入](域名接入.md)章节重新完成域名接入。
    -   能正常访问，执行[2](#li2057953372517)。

2.  <a name="li2057953372517"></a>清理浏览器缓存，在浏览器中输入“http://www.example.com?id=1%20or%201%20=1“模拟SQL注入攻击。
3.  返回Web应用防火墙控制界面，在左侧导航树中，单击“防护事件“，进入“防护事件“页面，查看防护域名拦截日志，您也可以[下载防护事件数据](下载防护事件数据.md)。

## 配置示例<a name="section1978194713716"></a>

放行百度或者谷歌的搜索引擎，同时拦截百度的POST请求。

1.  参照[操作步骤](#section61533550183130)将“搜索引擎“设置为放行，即将“搜索引擎“的“状态“设置为![](figures/icon-close.png)。
2.  参照[配置精准访问防护规则](配置精准访问防护规则.md)配置如[图4 ](#fig1439052051516)的规则。

    **图 4**  拦截POST请求<a name="fig1439052051516"></a>  
    ![](figures/拦截POST请求.png "拦截POST请求")


