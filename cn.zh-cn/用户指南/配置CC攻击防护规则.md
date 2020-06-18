# 配置CC攻击防护规则<a name="waf_01_0009"></a>

您可以自定义CC（Challenge Collapsar）防护规则，限制单个IP/Cookie/Referer访问者对您的网站上特定路径（URL）的访问频率，WAF会根据您配置的规则，精准识别CC攻击以及有效缓解CC攻击。例如，您可以配置该规则：当Cookie标识为name的用户在60秒内访问您域名下的“/admin\*“页面超过10次时，封禁该用户访问目标网址600秒。

>![](public_sys-resources/icon-note.gif) **说明：**   
>WAF会在客户请求Cookie中插入HWWAFSESID，HWWAFSESTIME等字段，这些字段服务于WAF统计和安全特性。  

## 前提条件<a name="section2256777914731"></a>

-   已获取管理控制台的账号和密码。
-   已添加防护域名。

## 操作步骤<a name="section61533550183130"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入防护配置入口，如[图1](#waf_01_0008_fig089771664710)所示。

    **图 1**  防护配置入口<a name="waf_01_0008_fig089771664710"></a>  
    ![](figures/防护配置入口.png "防护配置入口")


1.  在“CC攻击防护“配置框中，用户可根据自己的需要更改“状态“，单击“自定义CC攻击防护规则“，进入CC防护规则配置页面，如[图2](#fig102851827142620)所示。

    **图 2**  CC防护规则配置框<a name="fig102851827142620"></a>  
    ![](figures/CC防护规则配置框.png "CC防护规则配置框")

2.  在“CC防护“规则配置页面左上角，单击“添加规则“。
3.  在弹出的对话框中，根据[表1](#table1173915209149)配置CC防护规则。

    以[图3](#fig172782071413)的配置为例，其含义为：Cookie标识为“name“的用户访问目标地址（以/admin为前缀的地址，例如，Https://www.example.com/adminlogic）时，一旦在60秒内访问超过10次，就直接阻断该Cookie用户访问目标URL地址，阻断操作持续600秒，阻断页面返回自定义的页面内容。

    **图 3**  添加CC防护规则<a name="fig172782071413"></a>  
    ![](figures/添加CC防护规则.png "添加CC防护规则")

    **表 1**  CC防护规则参数说明

    <a name="table1173915209149"></a>
    <table><thead align="left"><tr id="row16728112012148"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.4.1.1"><p id="p177281920151410"><a name="p177281920151410"></a><a name="p177281920151410"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="54.26%" id="mcps1.2.4.1.2"><p id="p197281120161411"><a name="p197281120161411"></a><a name="p197281120161411"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="26.740000000000002%" id="mcps1.2.4.1.3"><p id="p1872872020147"><a name="p1872872020147"></a><a name="p1872872020147"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row948393052717"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p12483330162719"><a name="p12483330162719"></a><a name="p12483330162719"></a>工作模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><a name="ul426016212810"></a><a name="ul426016212810"></a><ul id="ul426016212810"><li>标准：只支持对域名的防护路径做限制。</li><li>高级：支持对路径、IP、Cookie字段做限制。仅企业版和旗舰版支持高级模式。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p17483193017279"><a name="p17483193017279"></a><a name="p17483193017279"></a>标准</p>
    </td>
    </tr>
    <tr id="row1073012091411"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p37282200144"><a name="p37282200144"></a><a name="p37282200144"></a>路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p472717511324"><a name="p472717511324"></a><a name="p472717511324"></a>当<span class="parmname" id="parmname131724123216"><a name="parmname131724123216"></a><a name="parmname131724123216"></a>“工作模式”</span>选择<span class="parmvalue" id="parmvalue660963320326"><a name="parmvalue660963320326"></a><a name="parmvalue660963320326"></a>“标准”</span>时，才配置此参数。</p>
    <p id="p2728220141413"><a name="p2728220141413"></a><a name="p2728220141413"></a>CC防护的URL链接，不包含域名。</p>
    <a name="ul1172942091416"></a><a name="ul1172942091416"></a><ul id="ul1172942091416"><li>前缀匹配：以*结尾代表以该路径为前缀。例如，需要防护的路径为<span class="parmvalue" id="parmvalue97281720131412"><a name="parmvalue97281720131412"></a><a name="parmvalue97281720131412"></a>“/admin/test.php”</span>或 <span class="parmvalue" id="parmvalue1872917207147"><a name="parmvalue1872917207147"></a><a name="parmvalue1872917207147"></a>“/adminabc”</span>，则路径可以填写为<span class="parmvalue" id="parmvalue20729720111415"><a name="parmvalue20729720111415"></a><a name="parmvalue20729720111415"></a>“/admin*”</span>。</li><li>精准匹配：需要防护的路径需要与此处填写的路径完全一致。例如，需要防护的路径为<span class="parmvalue" id="parmvalue672992019145"><a name="parmvalue672992019145"></a><a name="parmvalue672992019145"></a>“/admin”</span>，该规则必须填写为<span class="parmvalue" id="parmvalue1729182091416"><a name="parmvalue1729182091416"></a><a name="parmvalue1729182091416"></a>“/admin”</span>。</li></ul>
    <div class="note" id="note6730182015148"><a name="note6730182015148"></a><a name="note6730182015148"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul19730132018148"></a><a name="ul19730132018148"></a><ul id="ul19730132018148"><li>该路径不支持正则，仅支持前缀匹配和精准匹配的逻辑。</li><li>路径里不能含有连续多条斜线的配置，如<span class="parmvalue" id="parmvalue473019200148"><a name="parmvalue473019200148"></a><a name="parmvalue473019200148"></a>“///admin”</span>，WAF引擎会将<span class="parmvalue" id="parmvalue177301020101413"><a name="parmvalue177301020101413"></a><a name="parmvalue177301020101413"></a>“///”</span>转为<span class="parmvalue" id="parmvalue1273010203145"><a name="parmvalue1273010203145"></a><a name="parmvalue1273010203145"></a>“/”</span>。</li><li>该路径区分大小写。</li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p1073022018145"><a name="p1073022018145"></a><a name="p1073022018145"></a>/admin*</p>
    </td>
    </tr>
    <tr id="row3847404486"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p8848170124810"><a name="p8848170124810"></a><a name="p8848170124810"></a>条件列表</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p4848107487"><a name="p4848107487"></a><a name="p4848107487"></a>当<span class="parmname" id="parmname112092964820"><a name="parmname112092964820"></a><a name="parmname112092964820"></a>“工作模式”</span>选择<span class="parmvalue" id="parmvalue1212012913482"><a name="parmvalue1212012913482"></a><a name="parmvalue1212012913482"></a>“高级”</span>时，才配置此参数。</p>
    <p id="p7182153715485"><a name="p7182153715485"></a><a name="p7182153715485"></a><span>单击</span><span class="uicontrol" id="uicontrol1121619347492"><a name="uicontrol1121619347492"></a><a name="uicontrol1121619347492"></a>“添加”</span><span>增加新的条件，至少配置一项条件，最多可添加30项条件，多个条件同时满足时，本条规则才生效。</span></p>
    <a name="ul61829843104748"></a><a name="ul61829843104748"></a><ul id="ul61829843104748"><li>字段：路径、IP、Cookie。</li><li>子字段：当<span class="parmname" id="parmname16697185810527"><a name="parmname16697185810527"></a><a name="parmname16697185810527"></a>“字段”</span>选择<span class="parmvalue" id="parmvalue7793131533815"><a name="parmvalue7793131533815"></a><a name="parmvalue7793131533815"></a>“Cookie”</span>时，请根据实际需求配置子字段。<div class="notice" id="note85400119109"><a name="note85400119109"></a><a name="note85400119109"></a><span class="noticetitle"> 须知： </span><div class="noticebody"><p id="p954031113102"><a name="p954031113102"></a><a name="p954031113102"></a>子字段的长度不能超过2048字节，且只能由数字、字母、下划线和中划线组成。</p>
    </div></div>
    </li><li>逻辑：在<span class="parmname" id="parmname43845565104748"><a name="parmname43845565104748"></a><a name="parmname43845565104748"></a>“逻辑”</span>下拉列表中选择需要的逻辑关系。<div class="note" id="note168625321513"><a name="note168625321513"></a><a name="note168625321513"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p19863173225111"><a name="p19863173225111"></a><a name="p19863173225111"></a>当<span class="parmname" id="parmname9158165611519"><a name="parmname9158165611519"></a><a name="parmname9158165611519"></a>“逻辑”</span>关系选择<span class="parmvalue" id="parmvalue316420107"><a name="parmvalue316420107"></a><a name="parmvalue316420107"></a>“包含任意一个”</span>、<span class="parmvalue" id="parmvalue12165801907"><a name="parmvalue12165801907"></a><a name="parmvalue12165801907"></a>“不包含所有”</span>、<span class="parmvalue" id="parmvalue1816610017019"><a name="parmvalue1816610017019"></a><a name="parmvalue1816610017019"></a>“等于任意一个”</span>、<span class="parmvalue" id="parmvalue1616710407"><a name="parmvalue1616710407"></a><a name="parmvalue1616710407"></a>“不等于所有”</span>、<span class="parmvalue" id="parmvalue1616911010016"><a name="parmvalue1616911010016"></a><a name="parmvalue1616911010016"></a>“前缀为任意一个”</span>、<span class="parmvalue" id="parmvalue61702001013"><a name="parmvalue61702001013"></a><a name="parmvalue61702001013"></a>“前缀不为所有”</span>、<span class="parmvalue" id="parmvalue5170308017"><a name="parmvalue5170308017"></a><a name="parmvalue5170308017"></a>“后缀为任意一个”</span>或者<span class="parmvalue" id="parmvalue1717050303"><a name="parmvalue1717050303"></a><a name="parmvalue1717050303"></a>“后缀不为所有”</span>时，需要选择引用表，创建引用表的详细操作请参见<a href="创建引用表.md">创建引用表</a>。</p>
    </div></div>
    </li><li>内容：输入或者选择条件匹配的内容。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p961644792"><a name="p961644792"></a><a name="p961644792"></a><span class="parmvalue" id="parmvalue16126131216576"><a name="parmvalue16126131216576"></a><a name="parmvalue16126131216576"></a>“路径”</span>包含<span class="parmvalue" id="parmvalue1914790105042"><a name="parmvalue1914790105042"></a><a name="parmvalue1914790105042"></a>“/admin/”</span></p>
    </td>
    </tr>
    <tr id="row8733192051415"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p37301020121411"><a name="p37301020121411"></a><a name="p37301020121411"></a>限速模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><a name="ul167322202146"></a><a name="ul167322202146"></a><ul id="ul167322202146"><li>IP限速：根据IP区分单个Web访问者。</li><li>用户限速：根据Cookie键值区分单个Web访问者。</li><li>其他：根据Referer（自定义请求访问的来源）字段区分单个Web访问者。<div class="note" id="note17732132091410"><a name="note17732132091410"></a><a name="note17732132091410"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p147321020151413"><a name="p147321020151413"></a><a name="p147321020151413"></a>当<span class="parmname" id="parmname773122018141"><a name="parmname773122018141"></a><a name="parmname773122018141"></a>“防护模式”</span>选择<span class="parmvalue" id="parmvalue1273122019147"><a name="parmvalue1273122019147"></a><a name="parmvalue1273122019147"></a>“其他”</span>时，<span class="parmvalue" id="parmvalue16731320181412"><a name="parmvalue16731320181412"></a><a name="parmvalue16731320181412"></a>“Referer”</span>对应的<span class="parmvalue" id="parmvalue19731192013140"><a name="parmvalue19731192013140"></a><a name="parmvalue19731192013140"></a>“内容”</span>填写为包含域名的完整URL链接，仅支持前缀匹配和精准匹配的逻辑，<span class="parmvalue" id="parmvalue2073152021416"><a name="parmvalue2073152021416"></a><a name="parmvalue2073152021416"></a>“内容”</span>里不能含有连续的多条斜线的配置，如<span class="parmvalue" id="parmvalue18731220151412"><a name="parmvalue18731220151412"></a><a name="parmvalue18731220151412"></a>“///admin”</span>，WAF引擎会将<span class="parmvalue" id="parmvalue17732122014143"><a name="parmvalue17732122014143"></a><a name="parmvalue17732122014143"></a>“///”</span>转为<span class="parmvalue" id="parmvalue10732202081416"><a name="parmvalue10732202081416"></a><a name="parmvalue10732202081416"></a>“/”</span>。</p>
    <p id="p77329207149"><a name="p77329207149"></a><a name="p77329207149"></a>例如：防护路径设置为<span class="parmvalue" id="parmvalue1973213208144"><a name="parmvalue1973213208144"></a><a name="parmvalue1973213208144"></a>“/admin”</span>，若用户不希望访问者从<span class="parmvalue" id="parmvalue1073217209147"><a name="parmvalue1073217209147"></a><a name="parmvalue1073217209147"></a>“www.test.com”</span>访问该页面，则<span class="parmname" id="parmname1673202016142"><a name="parmname1673202016142"></a><a name="parmname1673202016142"></a>“Referer”</span>对应的<span class="parmvalue" id="parmvalue7732122012148"><a name="parmvalue7732122012148"></a><a name="parmvalue7732122012148"></a>“内容”</span>设置为<span class="parmvalue" id="parmvalue9732162091417"><a name="parmvalue9732162091417"></a><a name="parmvalue9732162091417"></a>“http://www.test.com”</span>。</p>
    </div></div>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p16733142061418"><a name="p16733142061418"></a><a name="p16733142061418"></a>用户限速</p>
    </td>
    </tr>
    <tr id="row1673319205141"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p573302001416"><a name="p573302001416"></a><a name="p573302001416"></a>用户标识</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p1573311208146"><a name="p1573311208146"></a><a name="p1573311208146"></a><span class="parmname" id="parmname1473322019148"><a name="parmname1473322019148"></a><a name="parmname1473322019148"></a>“防护模式”</span>选择<span class="parmvalue" id="parmvalue13733120161410"><a name="parmvalue13733120161410"></a><a name="parmvalue13733120161410"></a>“用户限速”</span>时，需要设置Cookie字段名，即用户需要根据网站实际情况配置唯一可识别Web访问者的Cookie中的某属性变量名。用户标识的Cookie，不支持正则，必须完全匹配。如果用户没有设置Cookie键值，WAF会自动分配一个值。</p>
    <p id="p127331420171418"><a name="p127331420171418"></a><a name="p127331420171418"></a>例如：如果网站使用Cookie中的某个字段name唯一标识用户，那么可以选取name字段来区分Web访问者。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p47331420141414"><a name="p47331420141414"></a><a name="p47331420141414"></a>name</p>
    </td>
    </tr>
    <tr id="row13734220141419"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p13733120111420"><a name="p13733120111420"></a><a name="p13733120111420"></a>限速频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p17733102001415"><a name="p17733102001415"></a><a name="p17733102001415"></a>单个Web访问者在限速周期内可以正常访问的次数，如果超过该访问次数，Web应用防火墙服务将根据配置的<span class="parmname" id="parmname14347201916"><a name="parmname14347201916"></a><a name="parmname14347201916"></a>“防护动作”</span>来处理。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p1173417206149"><a name="p1173417206149"></a><a name="p1173417206149"></a>10次/60秒</p>
    </td>
    </tr>
    <tr id="row4735102013144"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1573462071420"><a name="p1573462071420"></a><a name="p1573462071420"></a>防护动作</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p177341320101410"><a name="p177341320101410"></a><a name="p177341320101410"></a>当访问的请求频率超过<span class="parmname" id="parmname12866152313105"><a name="parmname12866152313105"></a><a name="parmname12866152313105"></a>“限速频率”</span>时，可设置以下防护动作：</p>
    <a name="ul1273582011416"></a><a name="ul1273582011416"></a><ul id="ul1273582011416"><li class="MsoBodyText">人机验证：表示超过<span class="parmname" id="parmname135017162317"><a name="parmname135017162317"></a><a name="parmname135017162317"></a>“限速频率”</span>后弹出验证码，进行人机验证，完成验证后，请求将不受访问限制。</li><li class="MsoBodyText">阻断：表示超过<span class="parmname" id="parmname2027844183115"><a name="parmname2027844183115"></a><a name="parmname2027844183115"></a>“限速频率”</span>将直接阻断。</li><li>动态阻断：上一个限速周期内，请求频率超过<span class="parmname" id="parmname7247154133211"><a name="parmname7247154133211"></a><a name="parmname7247154133211"></a>“限速频率”</span>将被阻断，那么在下一个限速周期内，请求频率超过<span class="parmname" id="parmname2024714143216"><a name="parmname2024714143216"></a><a name="parmname2024714143216"></a>“放行频率”</span>将被阻断。<p id="p1413384683216"><a name="p1413384683216"></a><a name="p1413384683216"></a>仅<span class="parmname" id="parmname544935418133"><a name="parmname544935418133"></a><a name="parmname544935418133"></a>“工作模式”</span>选择<span class="parmvalue" id="parmvalue184491354171317"><a name="parmvalue184491354171317"></a><a name="parmvalue184491354171317"></a>“高级”</span>时，才支持此防护动作。</p>
    </li><li class="MsoBodyText">仅记录：表示超过<span class="parmname" id="parmname5477145263110"><a name="parmname5477145263110"></a><a name="parmname5477145263110"></a>“限速频率”</span>将只记录不阻断。可<a href="下载防护事件数据.md">下载防护事件数据</a>查看域名的防护日志。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p9735192091414"><a name="p9735192091414"></a><a name="p9735192091414"></a>阻断</p>
    </td>
    </tr>
    <tr id="row230819642110"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p130817602111"><a name="p130817602111"></a><a name="p130817602111"></a>放行频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p2308156192118"><a name="p2308156192118"></a><a name="p2308156192118"></a>当<span class="parmname" id="parmname12401133122110"><a name="parmname12401133122110"></a><a name="parmname12401133122110"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue2040113112215"><a name="parmvalue2040113112215"></a><a name="parmvalue2040113112215"></a>“动态阻断”</span>时，可配置放行频率。</p>
    <p id="p8353134410399"><a name="p8353134410399"></a><a name="p8353134410399"></a>如果在一个限速周期内，访问超过<span class="parmname" id="parmname11555134563911"><a name="parmname11555134563911"></a><a name="parmname11555134563911"></a>“限速频率”</span>触发了拦截，那么，在下一个限速周期内，拦截阈值动态调整为<span class="parmname" id="parmname125553459392"><a name="parmname125553459392"></a><a name="parmname125553459392"></a>“放行频率”</span>。</p>
    <p id="p139821814410"><a name="p139821814410"></a><a name="p139821814410"></a><span class="parmname" id="parmname0921142210459"><a name="parmname0921142210459"></a><a name="parmname0921142210459"></a>“放行频率”</span>小于等于<span class="parmname" id="parmname2025711289450"><a name="parmname2025711289450"></a><a name="parmname2025711289450"></a>“限速频率”</span>。</p>
    <div class="note" id="note1273813381478"><a name="note1273813381478"></a><a name="note1273813381478"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1673811389719"><a name="p1673811389719"></a><a name="p1673811389719"></a>当<span class="parmname" id="parmname966384711714"><a name="parmname966384711714"></a><a name="parmname966384711714"></a>“放行频率”</span>设置为0时，表示如果上一个限速周期发生过拦截后，下一个限速周期所有的请求都不放行。</p>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p12308126182112"><a name="p12308126182112"></a><a name="p12308126182112"></a>8次/60秒</p>
    </td>
    </tr>
    <tr id="row7736420181410"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p17735172015144"><a name="p17735172015144"></a><a name="p17735172015144"></a>阻断时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p117365207143"><a name="p117365207143"></a><a name="p117365207143"></a>当<span class="parmname" id="parmname157361420111414"><a name="parmname157361420111414"></a><a name="parmname157361420111414"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue67361920141412"><a name="parmvalue67361920141412"></a><a name="parmvalue67361920141412"></a>“阻断”</span>时，可设置阻断后恢复正常访问页面的时间。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p973610202149"><a name="p973610202149"></a><a name="p973610202149"></a>600秒</p>
    </td>
    </tr>
    <tr id="row157374203148"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1873610201146"><a name="p1873610201146"></a><a name="p1873610201146"></a>阻断页面</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p20736520101416"><a name="p20736520101416"></a><a name="p20736520101416"></a>当<span class="parmname" id="parmname6736192020149"><a name="parmname6736192020149"></a><a name="parmname6736192020149"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue15736102061411"><a name="parmvalue15736102061411"></a><a name="parmvalue15736102061411"></a>“阻断”</span>时，需要设置，即当访问超过限速频率时，返回的错误页面。</p>
    <a name="ul47377202143"></a><a name="ul47377202143"></a><ul id="ul47377202143"><li>当选择<span class="parmvalue" id="parmvalue5736172071412"><a name="parmvalue5736172071412"></a><a name="parmvalue5736172071412"></a>“默认设置”</span>时，返回的错误页面为系统默认的阻断页面。</li><li>当选择<span class="parmvalue" id="parmvalue0737172081419"><a name="parmvalue0737172081419"></a><a name="parmvalue0737172081419"></a>“自定义”</span>，返回错误信息由用户自定义。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p1173772014147"><a name="p1173772014147"></a><a name="p1173772014147"></a>自定义</p>
    </td>
    </tr>
    <tr id="row16738920121413"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1473752013147"><a name="p1473752013147"></a><a name="p1473752013147"></a>页面类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p273816207148"><a name="p273816207148"></a><a name="p273816207148"></a>当<span class="parmname" id="parmname57371420181412"><a name="parmname57371420181412"></a><a name="parmname57371420181412"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue9737172021410"><a name="parmvalue9737172021410"></a><a name="parmvalue9737172021410"></a>“自定义”</span>时，可选择阻断页面的类型<span class="parmvalue" id="parmvalue11737102018149"><a name="parmvalue11737102018149"></a><a name="parmvalue11737102018149"></a>“application/json”</span>、<span class="parmvalue" id="parmvalue1373892081418"><a name="parmvalue1373892081418"></a><a name="parmvalue1373892081418"></a>“text/html”</span>或者<span class="parmvalue" id="parmvalue173814202141"><a name="parmvalue173814202141"></a><a name="parmvalue173814202141"></a>“text/xml”</span>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p1273842014142"><a name="p1273842014142"></a><a name="p1273842014142"></a>text/html</p>
    </td>
    </tr>
    <tr id="row87384209145"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p187381320171411"><a name="p187381320171411"></a><a name="p187381320171411"></a>页面内容</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p073872018149"><a name="p073872018149"></a><a name="p073872018149"></a>当<span class="parmname" id="parmname77388207141"><a name="parmname77388207141"></a><a name="parmname77388207141"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue1273810205142"><a name="parmvalue1273810205142"></a><a name="parmvalue1273810205142"></a>“自定义”</span>时，可设置自定义返回的内容。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p6118151728"><a name="p6118151728"></a><a name="p6118151728"></a>不同页面类型对应的页面内容样式：</p>
    <a name="ul046819338313"></a><a name="ul046819338313"></a><ul id="ul046819338313"><li>text/html：&lt;html&gt;&lt;body&gt;Forbidden&lt;/body&gt;&lt;/html&gt;</li><li>application/json：{"msg": "Forbidden"}</li><li>text/xml：&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;error&gt;	&lt;msg&gt;Forbidden&lt;/msg&gt;&lt;/error&gt;</li></ul>
    </td>
    </tr>
    <tr id="row77392201145"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p5738122020143"><a name="p5738122020143"></a><a name="p5738122020143"></a>规则描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="54.26%" headers="mcps1.2.4.1.2 "><p id="p1473832031411"><a name="p1473832031411"></a><a name="p1473832031411"></a>可选参数，设置该规则的备注信息。</p>
    </td>
    <td class="cellrowborder" valign="top" width="26.740000000000002%" headers="mcps1.2.4.1.3 "><p id="p15739202018147"><a name="p15739202018147"></a><a name="p15739202018147"></a>--</p>
    </td>
    </tr>
    </tbody>
    </table>

4.  单击“确认添加“，添加的CC攻击防护规则展示在CC规则列表中。

    **图 4**  CC规则列表<a name="fig1944015498156"></a>  
    ![](figures/CC规则列表.png "CC规则列表")

    -   规则添加成功后，默认的“规则状态“为“已开启“，若您暂时不想使该规则生效，可在目标规则所在行的“操作“列，单击“关闭“。
    -   若需要修改添加的CC攻击防护规则时，可单击待修改的CC攻击防护规则所在行的“修改“，修改CC攻击防护规则。
    -   若需要删除用户自行添加的CC攻击防护规则时，可单击待删除的CC攻击防护规则所在行的“删除“，删除CC攻击防护规则。


## 防护效果<a name="section2969132523417"></a>

假如已添加域名“www.example.com“，且配置了如[图3](#fig172782071413)所示的CC防护规则。可参照以下步骤验证防护效果：

1.  清理浏览器缓存，在浏览器中输入防护域名，测试网站域名是否能正常访问。
    -   不能正常访问，参照[域名接入WAF](zh-cn_topic_0125242653.md)章节重新完成域名接入。
    -   能正常访问，执行[2](#li88102353919)。

2.  <a name="li88102353919"></a>清理浏览器缓存，在浏览器中访问满足Cookie条件的“http://www.example.com/admin“页面，在60秒内刷新页面10次，正常情况下，在第11次访问该页面时，返回自定义的拦截页面；600秒后刷新目标页面，页面访问正常。
3.  返回Web应用防火墙控制界面，在左侧导航树中，单击“防护事件“，进入“防护事件“页面，查看防护域名拦截日志，您也可以[下载防护事件数据](下载防护事件数据.md)。

