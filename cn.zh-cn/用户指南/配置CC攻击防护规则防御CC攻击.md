# 配置CC攻击防护规则防御CC攻击<a name="waf_01_0009"></a>

CC攻击防护规则支持通过限制单个IP/Cookie/Referer访问者对防护网站上源端的访问频率，同时支持策略限速（同一策略下对应的所有域名请求次数合并限速）、域名限速（每个域名单独统计总请求次数）和URL限速（每个URL请求单独统计请求次数），精准识别CC攻击以及有效缓解CC攻击；当您配置完CC攻击防护规则并开启CC攻击防护后（即“CC攻击防护“配置框的“状态“为![](figures/icon-enable-28.png)），WAF才能根据您配置的CC攻击防护规则进行CC攻击防护。

CC攻击防护规则可以添加引用表，引用表防护规则对所有防护域名都生效，即所有防护域名都可以使用CC攻击防护规则的引用表。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果您已开通企业项目，您需要在“企业项目“下拉列表中选择您所在的企业项目并确保已开通操作权限，才能为该企业项目下域名配置防护策略。

## 前提条件<a name="section5903171661012"></a>

-   已添加防护网站。
    -   云模式的接入方式参见[网站接入WAF（云模式）](网站接入WAF（云模式）.md)章节。
    -   独享模式的接入方式参见[网站接入WAF（独享模式）](网站接入WAF（独享模式）.md)章节。

-   如果使用独享WAF，确保独享引擎已升级到最新版本，具体的操作请参见[升级独享引擎实例](管理独享引擎.md)。

## 约束条件<a name="section687472033111"></a>

-   添加或修改防护规则后，规则生效需要等待几分钟。规则生效后，您可以在“防护事件“页面查看防护效果。
-   当“逻辑“关系选择“包含任意一个“、“不包含所有“、“等于任意一个“、“不等于所有“、“前缀为任意一个“、“前缀不为所有“、“后缀为任意一个“或者“后缀不为所有“时，需要选择引用表，创建引用表的详细操作请参见[创建引用表对防护指标进行批量配置](创建引用表对防护指标进行批量配置.md)。
-   入门版和标准版不支持引用表管理功能。
-   仅云模式支持配置“全局计数“。
-   使用云模式WAF时，如果WAF前使用了高防、CDN（Content Delivery Network，内容分发网络）、云加速等代理时，建议“限速模式“选择“源限速  \>  用户限速“，并勾选“全局计数“。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果网站在接入WAF前，已经使用了CDN、高防等其他代理服务，WAF收到的访问IP会被分散到各个WAF节点进行流量转发，WAF默认为WAF节点单独计数。因此，WAF针对单个Web访问者的访问次数的计数会分散，所以“限速频率“中访问次数的设置原则如下：
>-   云模式：该模式支持“全局计数“，即支持将已经标识的请求在一个或多个WAF节点上的计数聚合，因此，配置时勾选“全局计数“即可。
>-   独享模式：该模式暂不支持“全局计数“，因此配置“限速频率“中访问次数应配置为：允许单个Web访问者在限速周期内访问网站的次数/MIN\(WAF前使用的代理服务总数：WAF节点数\)。
>    例如，WAF前已使用3个代理服务，WAF节点数（防护该网站的独享引擎实例数）为2，则取其最小值为2，如果您想当单个Web访问者在限速周期内访问网站的次数不能超过1000次，则“限速频率“中访问次数应配置为1000除以2，500。

## 操作步骤<a name="section91607252919"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  单击管理控制台左上角的![](figures/icon-region-29.jpg)，选择区域或项目。
3.  单击页面左上方的![](figures/icon-Service-30.png)，选择“安全与合规  \>  Web应用防火墙 WAF“。
4.  在左侧导航树中，选择“防护策略“，进入“防护策略“页面。
5.  单击目标策略名称，进入目标策略的防护配置页面。
6.  在“CC攻击防护“配置框中，用户可根据自己的需要更改“状态“，单击“自定义CC攻击防护规则“，进入CC防护规则配置页面。

    **图 1**  CC防护规则配置框<a name="fig102851827142620"></a>  
    ![](figures/CC防护规则配置框.png "CC防护规则配置框")

7.  在“CC攻击防护“规则配置页面左上角，单击“添加规则“。
8.  在弹出的对话框中，根据[表1](#table480817611214)配置CC防护规则。

    例如，通过配置CC攻击防护规则实现以下功能：根据Cookie标识的用户字段（例如name），当WAF识别到同一name值的用户在60秒内访问您域名下的URL（例如，/admin\*）页面超过10次时，封禁该用户访问目标网址600秒。

    **图 2**  添加CC防护规则<a name="fig1083929152617"></a>  
    ![](figures/添加CC防护规则.png "添加CC防护规则")

    **表 1**  CC防护规则参数说明

    <a name="table480817611214"></a>
    <table><thead align="left"><tr id="row28091661216"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.4.1.1"><p id="p5809666219"><a name="p5809666219"></a><a name="p5809666219"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="54.26%" id="mcps1.2.4.1.2"><p id="p1280916182114"><a name="p1280916182114"></a><a name="p1280916182114"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.740000000000002%" id="mcps1.2.4.1.3"><p id="p780915622110"><a name="p780915622110"></a><a name="p780915622110"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row77451636203015"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p37451136113010"><a name="p37451136113010"></a><a name="p37451136113010"></a>规则名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p13745153643013"><a name="p13745153643013"></a><a name="p13745153643013"></a>自定义规则名称。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p7745236163017"><a name="p7745236163017"></a><a name="p7745236163017"></a>waftest</p>
    </td>
    </tr>
    <tr id="row1578403212304"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p112857448140"><a name="p112857448140"></a><a name="p112857448140"></a>规则描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p343853654512"><a name="p343853654512"></a><a name="p343853654512"></a>可选参数，设置该规则的备注信息。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p1438193610452"><a name="p1438193610452"></a><a name="p1438193610452"></a>--</p>
    </td>
    </tr>
    <tr id="row41141352143411"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1711445283417"><a name="p1711445283417"></a><a name="p1711445283417"></a>限速模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><a name="ul7245174819362"></a><a name="ul7245174819362"></a><ul id="ul7245174819362"><li><span class="parmname" id="parmname1867058103618"><a name="parmname1867058103618"></a><a name="parmname1867058103618"></a>“源限速”</span>：对源端限速，如某IP（或用户）的访问频率超过限速频率，就会对该IP（或用户）的访问限速。<a name="ul250441619524"></a><a name="ul250441619524"></a><ul id="ul250441619524"><li><span class="parmvalue" id="parmvalue18738773536"><a name="parmvalue18738773536"></a><a name="parmvalue18738773536"></a>“IP限速”</span>：根据IP区分单个Web访问者。</li><li><span class="parmvalue" id="parmvalue1591281325311"><a name="parmvalue1591281325311"></a><a name="parmvalue1591281325311"></a>“用户限速”</span>：根据Cookie键值或者Header区分单个Web访问者。</li><li><span class="parmvalue" id="parmvalue16809169535"><a name="parmvalue16809169535"></a><a name="parmvalue16809169535"></a>“其他”</span>：根据Referer（自定义请求访问的来源）字段区分单个Web访问者。</li></ul>
    <div class="note" id="note68761329135514"><a name="note68761329135514"></a><a name="note68761329135514"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p15876122911551"><a name="p15876122911551"></a><a name="p15876122911551"></a>选择<span class="parmvalue" id="parmvalue1187642914555"><a name="parmvalue1187642914555"></a><a name="parmvalue1187642914555"></a>“其他”</span>时，<span class="parmvalue" id="parmvalue087682995517"><a name="parmvalue087682995517"></a><a name="parmvalue087682995517"></a>“Referer”</span>对应的<span class="parmvalue" id="parmvalue6876192910555"><a name="parmvalue6876192910555"></a><a name="parmvalue6876192910555"></a>“内容”</span>填写为包含域名的完整URL链接，仅支持前缀匹配和精准匹配的逻辑，<span class="parmvalue" id="parmvalue587710296559"><a name="parmvalue587710296559"></a><a name="parmvalue587710296559"></a>“内容”</span>里不能含有连续的多条斜线的配置，如<span class="parmvalue" id="parmvalue14877142910556"><a name="parmvalue14877142910556"></a><a name="parmvalue14877142910556"></a>“///admin”</span>，WAF引擎会将<span class="parmvalue" id="parmvalue1187716292558"><a name="parmvalue1187716292558"></a><a name="parmvalue1187716292558"></a>“///”</span>转为<span class="parmvalue" id="parmvalue387712298551"><a name="parmvalue387712298551"></a><a name="parmvalue387712298551"></a>“/”</span>。</p>
    <p id="p17877162935511"><a name="p17877162935511"></a><a name="p17877162935511"></a>例如：若用户不希望访问者从<span class="parmvalue" id="parmvalue8877129105512"><a name="parmvalue8877129105512"></a><a name="parmvalue8877129105512"></a>“www.test.com”</span>访问网站，则<span class="parmname" id="parmname13877122918551"><a name="parmname13877122918551"></a><a name="parmname13877122918551"></a>“Referer”</span>对应的<span class="parmvalue" id="parmvalue8877122965518"><a name="parmvalue8877122965518"></a><a name="parmvalue8877122965518"></a>“内容”</span>设置为<span class="parmvalue" id="parmvalue10878182916552"><a name="parmvalue10878182916552"></a><a name="parmvalue10878182916552"></a>“http://www.test.com”</span>。</p>
    </div></div>
    </li><li><span class="parmname" id="parmname1687116117378"><a name="parmname1687116117378"></a><a name="parmname1687116117378"></a>“目的限速”</span>：选择该参数时，可选择以下限速类型进行配置：<a name="ul4124201614447"></a><a name="ul4124201614447"></a><ul id="ul4124201614447"><li><span class="parmvalue" id="parmvalue24400461490"><a name="parmvalue24400461490"></a><a name="parmvalue24400461490"></a>“策略限速”</span> ：当多个域名共用一个策略时，该策略下对应的所有域名请求次数合并限速(不区分访问IP)；泛域名防护场景时，该泛域名对应的所有子域名的请求次数合并限速(不区分访问IP)。</li><li><span class="parmvalue" id="parmvalue1259613493492"><a name="parmvalue1259613493492"></a><a name="parmvalue1259613493492"></a>“域名限速”</span>：每个域名单独统计总请求次数，超过设定值则触发防护动作(不区分访问IP)。</li><li><span class="parmvalue" id="parmvalue1680885284916"><a name="parmvalue1680885284916"></a><a name="parmvalue1680885284916"></a>“URL限速”</span>：每个URL请求单独统计请求次数，超过设定值则触发防护动作(不区分访问IP)。</li></ul>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p1711495216348"><a name="p1711495216348"></a><a name="p1711495216348"></a>--</p>
    </td>
    </tr>
    <tr id="row9279193817572"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p09232049135711"><a name="p09232049135711"></a><a name="p09232049135711"></a>用户标识</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p1492374913577"><a name="p1492374913577"></a><a name="p1492374913577"></a><span class="parmname" id="parmname1392334911578"><a name="parmname1392334911578"></a><a name="parmname1392334911578"></a>“限速模式”</span>选择<span class="menucascade" id="menucascade142481518125813"><a name="menucascade142481518125813"></a><a name="menucascade142481518125813"></a>“<span class="uicontrol" id="uicontrol724810185585"><a name="uicontrol724810185585"></a><a name="uicontrol724810185585"></a>源限速</span> &gt; <span class="uicontrol" id="uicontrol74413025812"><a name="uicontrol74413025812"></a><a name="uicontrol74413025812"></a>用户限速</span>”</span>时，需要配置此参数：</p>
    <a name="ul17923124914573"></a><a name="ul17923124914573"></a><ul id="ul17923124914573"><li>选择Cookie时，设置Cookie字段名，即用户需要根据网站实际情况配置唯一可识别Web访问者的Cookie中的某属性变量名。用户标识的Cookie，不支持正则，必须完全匹配。<p id="p149231949175717"><a name="p149231949175717"></a><a name="p149231949175717"></a>例如：如果网站使用Cookie中的某个字段name唯一标识用户，那么可以选取name字段来区分Web访问者。</p>
    </li><li>选择Header时，设置需要防护的自定义HTTP首部，即用户需要根据网站实际情况配置可识别Web访问者的HTTP首部。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p15923164911577"><a name="p15923164911577"></a><a name="p15923164911577"></a>name</p>
    </td>
    </tr>
    <tr id="row0629171375917"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p362991345920"><a name="p362991345920"></a><a name="p362991345920"></a>域名聚合统计</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p141581068410"><a name="p141581068410"></a><a name="p141581068410"></a><span class="parmname" id="parmname125736193412"><a name="parmname125736193412"></a><a name="parmname125736193412"></a>“限速模式”</span>选择<span class="menucascade" id="menucascade10926171413417"><a name="menucascade10926171413417"></a><a name="menucascade10926171413417"></a>“<span class="uicontrol" id="uicontrol29267141045"><a name="uicontrol29267141045"></a><a name="uicontrol29267141045"></a>目的限速</span> &gt; <span class="uicontrol" id="uicontrol1792617144412"><a name="uicontrol1792617144412"></a><a name="uicontrol1792617144412"></a>策略限速</span>”</span>时，不需要配置此参数。</p>
    <p id="p15629121312599"><a name="p15629121312599"></a><a name="p15629121312599"></a>默认关闭，开启后，泛域名对应的所有子域名的请求次数合并限速(不区分访问IP)。例如，配置的泛域名为<span class="parmvalue" id="parmvalue1996511371264"><a name="parmvalue1996511371264"></a><a name="parmvalue1996511371264"></a>“*.a.com”</span>，会将所有子域名（b.a.com，c.a.com等）的请求一起聚合统计。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p96291613145910"><a name="p96291613145910"></a><a name="p96291613145910"></a>--</p>
    </td>
    </tr>
    <tr id="row88111966213"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p198111614213"><a name="p198111614213"></a><a name="p198111614213"></a>限速条件</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p148116617213"><a name="p148116617213"></a><a name="p148116617213"></a>单击<span class="uicontrol" id="uicontrol128121642118"><a name="uicontrol128121642118"></a><a name="uicontrol128121642118"></a>“添加”</span>增加新的条件，至少配置一项条件，最多可添加30项条件，多个条件同时满足时，本条规则才生效。</p>
    <a name="ul1381286182115"></a><a name="ul1381286182115"></a><ul id="ul1381286182115"><li>字段。</li><li>子字段：当<span class="parmname" id="parmname7812146122115"><a name="parmname7812146122115"></a><a name="parmname7812146122115"></a>“字段”</span>选择IPv4、IPv6、Cookie、Header、Params时，请根据实际需求配置子字段。<div class="notice" id="note981220611214"><a name="note981220611214"></a><a name="note981220611214"></a><span class="noticetitle"> 须知： </span><div class="noticebody"><p id="p381210682110"><a name="p381210682110"></a><a name="p381210682110"></a>子字段的长度不能超过2048字节，且只能由数字、字母、下划线和中划线组成。</p>
    </div></div>
    </li><li>逻辑：在<span class="parmname" id="parmname1381216619215"><a name="parmname1381216619215"></a><a name="parmname1381216619215"></a>“逻辑”</span>下拉列表中选择需要的逻辑关系。<div class="note" id="note138121767211"><a name="note138121767211"></a><a name="note138121767211"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1181217622118"><a name="p1181217622118"></a><a name="p1181217622118"></a>当<span class="parmname" id="parmname208127622111"><a name="parmname208127622111"></a><a name="parmname208127622111"></a>“逻辑”</span>关系选择<span class="parmvalue" id="parmvalue68139692117"><a name="parmvalue68139692117"></a><a name="parmvalue68139692117"></a>“包含任意一个”</span>、<span class="parmvalue" id="parmvalue781316152113"><a name="parmvalue781316152113"></a><a name="parmvalue781316152113"></a>“不包含所有”</span>、<span class="parmvalue" id="parmvalue1881319602117"><a name="parmvalue1881319602117"></a><a name="parmvalue1881319602117"></a>“等于任意一个”</span>、<span class="parmvalue" id="parmvalue4813126112118"><a name="parmvalue4813126112118"></a><a name="parmvalue4813126112118"></a>“不等于所有”</span>、<span class="parmvalue" id="parmvalue78130616219"><a name="parmvalue78130616219"></a><a name="parmvalue78130616219"></a>“前缀为任意一个”</span>、<span class="parmvalue" id="parmvalue148131469217"><a name="parmvalue148131469217"></a><a name="parmvalue148131469217"></a>“前缀不为所有”</span>、<span class="parmvalue" id="parmvalue9813562219"><a name="parmvalue9813562219"></a><a name="parmvalue9813562219"></a>“后缀为任意一个”</span>或者<span class="parmvalue" id="parmvalue58131766212"><a name="parmvalue58131766212"></a><a name="parmvalue58131766212"></a>“后缀不为所有”</span>时，需要选择引用表，创建引用表的详细操作请参见<a href="创建引用表对防护指标进行批量配置.md">创建引用表对防护指标进行批量配置</a>。</p>
    </div></div>
    </li><li>内容：输入或者选择条件匹配的内容。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p28131966218"><a name="p28131966218"></a><a name="p28131966218"></a><span class="parmvalue" id="parmvalue118130652119"><a name="parmvalue118130652119"></a><a name="parmvalue118130652119"></a>“路径”</span>包含<span class="parmvalue" id="parmvalue18814146192113"><a name="parmvalue18814146192113"></a><a name="parmvalue18814146192113"></a>“/admin/”</span></p>
    </td>
    </tr>
    <tr id="row781736152116"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p9817126112119"><a name="p9817126112119"></a><a name="p9817126112119"></a>限速频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p1281726152112"><a name="p1281726152112"></a><a name="p1281726152112"></a>单个Web访问者在限速周期内可以正常访问的次数，如果超过该访问次数，Web应用防火墙服务将根据配置的<span class="parmname" id="parmname14817164217"><a name="parmname14817164217"></a><a name="parmname14817164217"></a>“防护动作”</span>来处理。</p>
    <p id="p78171682111"><a name="p78171682111"></a><a name="p78171682111"></a><span class="parmname" id="parmname128172613216"><a name="parmname128172613216"></a><a name="parmname128172613216"></a>“全局计数”</span>：根据不同的限速模式，将已经标识的请求在一个或多个WAF节点上的计数聚合。默认为每WAF节点单独计数，开启后本区域所有节点合并计数。<span class="parmvalue" id="parmvalue1721911433176"><a name="parmvalue1721911433176"></a><a name="parmvalue1721911433176"></a>“IP限速”</span>不能满足针对某个用户进行限速，需要选择<span class="parmvalue" id="parmvalue1681720692112"><a name="parmvalue1681720692112"></a><a name="parmvalue1681720692112"></a>“用户限速”</span>或<span class="parmvalue" id="parmvalue168181672112"><a name="parmvalue168181672112"></a><a name="parmvalue168181672112"></a>“其他”</span>的Referer限速，此时标识的请求可能会访问到不同的WAF节点，开启全局计数后，将请求访问的一个或多个WAF节点访问量聚合，达到全局统计的目的。</p>
    <div class="note" id="note10429142661015"><a name="note10429142661015"></a><a name="note10429142661015"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="waf_01_0009_p2063088225"><a name="waf_01_0009_p2063088225"></a><a name="waf_01_0009_p2063088225"></a>如果网站在接入WAF前，已经使用了CDN、高防等其他代理服务，WAF收到的访问IP会被分散到各个WAF节点进行流量转发，WAF默认为WAF节点单独计数。因此，WAF针对单个Web访问者的访问次数的计数会分散，所以<span class="parmname" id="waf_01_0009_parmname191775052913"><a name="waf_01_0009_parmname191775052913"></a><a name="waf_01_0009_parmname191775052913"></a>“限速频率”</span>中访问次数的设置原则如下：</p>
    <a name="waf_01_0009_ul7545343123018"></a><a name="waf_01_0009_ul7545343123018"></a><ul id="waf_01_0009_ul7545343123018"><li>云模式：该模式支持<span class="parmname" id="waf_01_0009_parmname1662671553114"><a name="waf_01_0009_parmname1662671553114"></a><a name="waf_01_0009_parmname1662671553114"></a>“全局计数”</span>，即支持将已经标识的请求在一个或多个WAF节点上的计数聚合，因此，配置时勾选<span class="parmname" id="waf_01_0009_parmname95771641185410"><a name="waf_01_0009_parmname95771641185410"></a><a name="waf_01_0009_parmname95771641185410"></a>“全局计数”</span>即可。</li><li>独享模式：该模式暂不支持<span class="parmname" id="waf_01_0009_parmname112781914341"><a name="waf_01_0009_parmname112781914341"></a><a name="waf_01_0009_parmname112781914341"></a>“全局计数”</span>，因此配置<span class="parmname" id="waf_01_0009_parmname2093532803416"><a name="waf_01_0009_parmname2093532803416"></a><a name="waf_01_0009_parmname2093532803416"></a>“限速频率”</span>中访问次数应配置为：允许单个Web访问者在限速周期内访问网站的次数/MIN(WAF前使用的代理服务总数：WAF节点数)。<p id="waf_01_0009_p1118513516396"><a name="waf_01_0009_p1118513516396"></a><a name="waf_01_0009_p1118513516396"></a>例如，WAF前已使用3个代理服务，WAF节点数（防护该网站的独享引擎实例数）为2，则取其最小值为2，如果您想当单个Web访问者在限速周期内访问网站的次数不能超过1000次，则<span class="parmname" id="waf_01_0009_parmname669705174810"><a name="waf_01_0009_parmname669705174810"></a><a name="waf_01_0009_parmname669705174810"></a>“限速频率”</span>中访问次数应配置为1000除以2，500。</p>
    </li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p881896202110"><a name="p881896202110"></a><a name="p881896202110"></a>10次/60秒</p>
    </td>
    </tr>
    <tr id="row98183611216"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p2818363217"><a name="p2818363217"></a><a name="p2818363217"></a>防护动作</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p58189619213"><a name="p58189619213"></a><a name="p58189619213"></a>当访问的请求频率超过<span class="parmname" id="parmname881813611211"><a name="parmname881813611211"></a><a name="parmname881813611211"></a>“限速频率”</span>时，可设置以下防护动作：</p>
    <a name="ul581886182115"></a><a name="ul581886182115"></a><ul id="ul581886182115"><li class="MsoBodyText">人机验证：表示超过<span class="parmname" id="parmname581810642112"><a name="parmname581810642112"></a><a name="parmname581810642112"></a>“限速频率”</span>后弹出验证码，进行人机验证，完成验证后，请求将不受访问限制。人机验证目前支持英文。</li><li class="MsoBodyText">阻断：表示超过<span class="parmname" id="parmname18181164215"><a name="parmname18181164215"></a><a name="parmname18181164215"></a>“限速频率”</span>将直接阻断。</li><li>动态阻断：上一个限速周期内，请求频率超过<span class="parmname" id="parmname14819567218"><a name="parmname14819567218"></a><a name="parmname14819567218"></a>“限速频率”</span>将被阻断，那么在下一个限速周期内，请求频率超过<span class="parmname" id="parmname581926132116"><a name="parmname581926132116"></a><a name="parmname581926132116"></a>“放行频率”</span>将被阻断。</li><li class="MsoBodyText">仅记录：表示超过<span class="parmname" id="parmname128256618218"><a name="parmname128256618218"></a><a name="parmname128256618218"></a>“限速频率”</span>将只记录不阻断。可<a href="下载防护事件数据.md">下载防护事件数据</a>查看域名的防护日志。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p88251468213"><a name="p88251468213"></a><a name="p88251468213"></a>阻断</p>
    </td>
    </tr>
    <tr id="row1485755335715"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p10858105315716"><a name="p10858105315716"></a><a name="p10858105315716"></a>锁定验证</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p148581753195720"><a name="p148581753195720"></a><a name="p148581753195720"></a>当<span class="parmname" id="parmname15998316175816"><a name="parmname15998316175816"></a><a name="parmname15998316175816"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue11998216135810"><a name="parmvalue11998216135810"></a><a name="parmvalue11998216135810"></a>“人机验证”</span>时，需要配置该参数。</p>
    <p id="p135361416185911"><a name="p135361416185911"></a><a name="p135361416185911"></a>当人机验证未通过时，在设定时间内的访问都要进行验证。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p1785815325710"><a name="p1785815325710"></a><a name="p1785815325710"></a>300秒</p>
    </td>
    </tr>
    <tr id="row198251869211"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p108261366216"><a name="p108261366216"></a><a name="p108261366216"></a>放行频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p1882676162116"><a name="p1882676162116"></a><a name="p1882676162116"></a>当<span class="parmname" id="parmname28261268210"><a name="parmname28261268210"></a><a name="parmname28261268210"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue88266613212"><a name="parmvalue88266613212"></a><a name="parmvalue88266613212"></a>“动态阻断”</span>时，可配置放行频率。</p>
    <p id="p982636102115"><a name="p982636102115"></a><a name="p982636102115"></a>如果在一个限速周期内，访问超过<span class="parmname" id="parmname108261663215"><a name="parmname108261663215"></a><a name="parmname108261663215"></a>“限速频率”</span>触发了拦截，那么，在下一个限速周期内，拦截阈值动态调整为<span class="parmname" id="parmname482646152110"><a name="parmname482646152110"></a><a name="parmname482646152110"></a>“放行频率”</span>。</p>
    <p id="p198263613211"><a name="p198263613211"></a><a name="p198263613211"></a><span class="parmname" id="parmname18268617215"><a name="parmname18268617215"></a><a name="parmname18268617215"></a>“放行频率”</span>小于等于<span class="parmname" id="parmname198265612110"><a name="parmname198265612110"></a><a name="parmname198265612110"></a>“限速频率”</span>。</p>
    <div class="note" id="note19826206132117"><a name="note19826206132117"></a><a name="note19826206132117"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1582676142113"><a name="p1582676142113"></a><a name="p1582676142113"></a>当<span class="parmname" id="parmname1982610662119"><a name="parmname1982610662119"></a><a name="parmname1982610662119"></a>“放行频率”</span>设置为0时，表示如果上一个限速周期发生过拦截后，下一个限速周期所有的请求都不放行。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p6826462213"><a name="p6826462213"></a><a name="p6826462213"></a>8次/60秒</p>
    </td>
    </tr>
    <tr id="row48261163219"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p28260682113"><a name="p28260682113"></a><a name="p28260682113"></a>阻断时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p1882719615214"><a name="p1882719615214"></a><a name="p1882719615214"></a>当<span class="parmname" id="parmname0827261213"><a name="parmname0827261213"></a><a name="parmname0827261213"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue1382711615216"><a name="parmvalue1382711615216"></a><a name="parmvalue1382711615216"></a>“阻断”</span>时，可设置阻断后恢复正常访问页面的时间。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p7827661212"><a name="p7827661212"></a><a name="p7827661212"></a>600秒</p>
    </td>
    </tr>
    <tr id="row178278614219"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1482756182112"><a name="p1482756182112"></a><a name="p1482756182112"></a>阻断页面</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p13827126122120"><a name="p13827126122120"></a><a name="p13827126122120"></a>当<span class="parmname" id="parmname13827561211"><a name="parmname13827561211"></a><a name="parmname13827561211"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue382717692119"><a name="parmvalue382717692119"></a><a name="parmvalue382717692119"></a>“阻断”</span>时，需要设置该参数，即当访问超过限速频率时，返回的错误页面。</p>
    <a name="ul58276611212"></a><a name="ul58276611212"></a><ul id="ul58276611212"><li>当选择<span class="parmvalue" id="parmvalue11827061213"><a name="parmvalue11827061213"></a><a name="parmvalue11827061213"></a>“默认设置”</span>时，返回的错误页面为系统默认的阻断页面。</li><li>当选择<span class="parmvalue" id="parmvalue1282710662114"><a name="parmvalue1282710662114"></a><a name="parmvalue1282710662114"></a>“自定义”</span>，返回错误信息由用户自定义。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p148275632115"><a name="p148275632115"></a><a name="p148275632115"></a>自定义</p>
    </td>
    </tr>
    <tr id="row11828126112117"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1982896162114"><a name="p1982896162114"></a><a name="p1982896162114"></a>页面类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p17828196202114"><a name="p17828196202114"></a><a name="p17828196202114"></a>当<span class="parmname" id="parmname198285692115"><a name="parmname198285692115"></a><a name="parmname198285692115"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue12828156182110"><a name="parmvalue12828156182110"></a><a name="parmvalue12828156182110"></a>“自定义”</span>时，可选择阻断页面的类型<span class="parmvalue" id="parmvalue1182810616212"><a name="parmvalue1182810616212"></a><a name="parmvalue1182810616212"></a>“application/json”</span>、<span class="parmvalue" id="parmvalue10828368218"><a name="parmvalue10828368218"></a><a name="parmvalue10828368218"></a>“text/html”</span>或者<span class="parmvalue" id="parmvalue18828106142113"><a name="parmvalue18828106142113"></a><a name="parmvalue18828106142113"></a>“text/xml”</span>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p20828668216"><a name="p20828668216"></a><a name="p20828668216"></a>text/html</p>
    </td>
    </tr>
    <tr id="row118281863218"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p20828767216"><a name="p20828767216"></a><a name="p20828767216"></a>页面内容</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p5828066216"><a name="p5828066216"></a><a name="p5828066216"></a>当<span class="parmname" id="parmname882811632114"><a name="parmname882811632114"></a><a name="parmname882811632114"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue6828764211"><a name="parmvalue6828764211"></a><a name="parmvalue6828764211"></a>“自定义”</span>时，可设置自定义返回的内容。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p5828156162116"><a name="p5828156162116"></a><a name="p5828156162116"></a>不同页面类型对应的页面内容样式：</p>
    <a name="ul15828206152120"></a><a name="ul15828206152120"></a><ul id="ul15828206152120"><li>text/html：&lt;html&gt;&lt;body&gt;Forbidden&lt;/body&gt;&lt;/html&gt;</li><li>application/json：{"msg": "Forbidden"}</li><li>text/xml：&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;error&gt;	&lt;msg&gt;Forbidden&lt;/msg&gt;&lt;/error&gt;</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

9.  单击“确认“，添加的CC攻击防护规则展示在CC规则列表中。
    -   规则添加成功后，默认的“规则状态“为“已开启“，若您暂时不想使该规则生效，可在目标规则所在行的“操作“列，单击“关闭“。
    -   若需要修改添加的CC攻击防护规则时，可单击待修改的CC攻击防护规则所在行的“修改“，修改CC攻击防护规则。
    -   若需要删除用户自行添加的CC攻击防护规则时，可单击待删除的CC攻击防护规则所在行的“删除“，删除CC攻击防护规则。

## 防护效果<a name="section4176194446"></a>

假如已添加域名“www.example.com“，且配置了如[图2](#fig1083929152617)所示“阻断“防护动作的CC防护规则。可参照以下步骤验证防护效果：

1.  清理浏览器缓存，在浏览器中输入防护域名，测试网站域名是否能正常访问。
    -   不能正常访问，参照[网站设置](网站设置.md)章节重新完成域名接入。
    -   能正常访问，执行[2](#li88102353919)。

2.  <a name="li88102353919"></a>清理浏览器缓存，在浏览器中访问满足Cookie条件的“http://www.example.com/admin“页面，在60秒内刷新页面10次，正常情况下，在第11次访问该页面时，返回自定义的拦截页面；600秒后刷新目标页面，页面访问正常。

    如果您设置了“人机验证“防护动作，当用户访问超过限制后需要输入验证码才能继续访问。

    ![](figures/zh-cn_image_0000001695522016.jpg)

3.  返回Web应用防火墙控制界面，在左侧导航树中，单击“防护事件“，进入“防护事件“页面，查看防护域名拦截日志，您也可以[下载防护事件数据](下载防护事件数据.md)。

## 配置示例-人机验证<a name="section118149824913"></a>

假如防护域名“www.example.com“已接入WAF，您可以参照以下操作步骤验证人机验证防护效果。

1.  添加防护动作为“人机验证“CC防护规则。

    **图 3**  添加“人机验证“防护规则<a name="fig15654111421118"></a>  
    ![](figures/添加人机验证防护规则.png "添加人机验证防护规则")

2.  开启CC攻击防护。

    **图 4**  CC防护规则配置框<a name="fig1837813216579"></a>  
    ![](figures/CC防护规则配置框.png "CC防护规则配置框")

3.  清理浏览器缓存，在浏览器中访问“http://www.example.com/admin/“页面。

    当您在60秒内访问页面10次，在第11次访问该页面时，页面弹出验证码。此时，您需要输入验证码才能继续访问。

    ![](figures/zh-cn_image_0000001481923368.jpg)

4.  返回Web应用防火墙管理控制台，在左侧导航树中，单击“防护事件“，进入“防护事件“页面，您可以查看该防护事件。

    **图 5**  查看防护事件-人机验证<a name="waf_01_1209_fig41102863113"></a>  
    ![](figures/查看防护事件-人机验证.png "查看防护事件-人机验证")

