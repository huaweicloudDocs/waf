# 配置CC攻击防护规则<a name="waf_01_0009"></a>

该任务指导您通过Web应用防火墙服务配置CC（Challenge Collapsar）攻击防护规则。

您可以自定义CC防护规则，限制单个IP/Cookie/Referer访问者对您的网站上特定路径（URL）的访问频率，WAF会根据您配置的规则，精准识别CC攻击以及有效缓解CC攻击。例如，您可以配置该规则：当单个源IP在20秒内访问您域名下的“/login.html“页面超过20次时，封禁该IP一小时。

## 前提条件<a name="section2256777914731"></a>

-   已获取管理控制台的帐号和密码。
-   已添加防护域名。

## 操作步骤<a name="section61533550183130"></a>

1.  登录管理控制台（https://console.huaweicloud.com/）。
2.  单击管理控制台左上角的![](figures/选择区域图标.jpg)，选择区域或项目。
3.  单击页面上方的“服务列表“，选择“安全  \>  Web应用防火墙“，在左侧导航树中选择“域名配置“，进入“域名配置“页面，如[图1](#waf_01_0008_fig164792010154510)所示。

    **图 1**  域名配置页面<a name="waf_01_0008_fig164792010154510"></a>  
    ![](figures/域名配置页面-11.png "域名配置页面-11")

4.  在目标域名所在行的“防护策略“栏中，单击“配置防护策略“，进入“防护配置“页面。
5.  在“CC攻击防护“配置框中，用户可根据自己的需要更改“状态“，单击“自定义CC攻击防护规则“，进入CC防护规则配置页面，如[图2](#fig102851827142620)所示。

    **图 2**  CC防护规则配置框<a name="fig102851827142620"></a>  
    ![](figures/CC防护规则配置框.png "CC防护规则配置框")

6.  在“CC防护“规则配置页面左上角，单击“添加规则“。
7.  在弹出的对话框中，根据[表1](#table1173915209149)配置CC防护规则。

    以[图3](#fig172782071413)的配置为例，其含义为：Cookie标识为“name“的用户访问目标地址（前缀匹配）时，一旦在60秒内访问超过10次，就直接阻断该Cookie用户访问目标URL地址，阻断操作持续600秒，阻断页面返回自定义的页面内容。

    **图 3**  添加CC防护规则<a name="fig172782071413"></a>  
    ![](figures/添加CC防护规则.png "添加CC防护规则")

    **表 1**  CC防护规则参数说明

    <a name="table1173915209149"></a>
    <table><thead align="left"><tr id="row16728112012148"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.4.1.1"><p id="p177281920151410"><a name="p177281920151410"></a><a name="p177281920151410"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.88%" id="mcps1.2.4.1.2"><p id="p197281120161411"><a name="p197281120161411"></a><a name="p197281120161411"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="30.12%" id="mcps1.2.4.1.3"><p id="p1872872020147"><a name="p1872872020147"></a><a name="p1872872020147"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1073012091411"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p37282200144"><a name="p37282200144"></a><a name="p37282200144"></a>路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p2728220141413"><a name="p2728220141413"></a><a name="p2728220141413"></a>CC防护的URL链接，不包含域名。</p>
    <a name="ul1172942091416"></a><a name="ul1172942091416"></a><ul id="ul1172942091416"><li>前缀匹配：以*结尾代表以该路径为前缀。例如，需要防护的路径为<span class="parmvalue" id="parmvalue97281720131412"><a name="parmvalue97281720131412"></a><a name="parmvalue97281720131412"></a>“/admin/test.php”</span>或 <span class="parmvalue" id="parmvalue1872917207147"><a name="parmvalue1872917207147"></a><a name="parmvalue1872917207147"></a>“/adminabc”</span>，则路径可以填写为<span class="parmvalue" id="parmvalue20729720111415"><a name="parmvalue20729720111415"></a><a name="parmvalue20729720111415"></a>“/admin*”</span>。</li><li>精准匹配：需要防护的路径需要与此处填写的路径完全相等。例如，需要防护的路径为<span class="parmvalue" id="parmvalue672992019145"><a name="parmvalue672992019145"></a><a name="parmvalue672992019145"></a>“/admin”</span>，该规则必须填写为<span class="parmvalue" id="parmvalue1729182091416"><a name="parmvalue1729182091416"></a><a name="parmvalue1729182091416"></a>“/admin”</span>。</li></ul>
    <div class="note" id="note6730182015148"><a name="note6730182015148"></a><a name="note6730182015148"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul19730132018148"></a><a name="ul19730132018148"></a><ul id="ul19730132018148"><li>该路径不支持正则，仅支持前缀匹配和精准匹配的逻辑。</li><li>路径里不能含有连续的多条斜线的配置，如<span class="parmvalue" id="parmvalue473019200148"><a name="parmvalue473019200148"></a><a name="parmvalue473019200148"></a>“///admin”</span>，WAF引擎会将<span class="parmvalue" id="parmvalue177301020101413"><a name="parmvalue177301020101413"></a><a name="parmvalue177301020101413"></a>“///”</span>转为<span class="parmvalue" id="parmvalue1273010203145"><a name="parmvalue1273010203145"></a><a name="parmvalue1273010203145"></a>“/”</span>。</li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p1073022018145"><a name="p1073022018145"></a><a name="p1073022018145"></a>/admin*</p>
    </td>
    </tr>
    <tr id="row8733192051415"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p37301020121411"><a name="p37301020121411"></a><a name="p37301020121411"></a>防护模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><a name="ul167322202146"></a><a name="ul167322202146"></a><ul id="ul167322202146"><li>IP限速：根据IP区分单个Web访问者。</li><li>用户限速：根据Cookie键值区分单个Web访问者。</li><li>其他：根据Referer（自定义请求访问的来源）字段区分单个Web访问者。<div class="note" id="note17732132091410"><a name="note17732132091410"></a><a name="note17732132091410"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p147321020151413"><a name="p147321020151413"></a><a name="p147321020151413"></a>当<span class="parmname" id="parmname773122018141"><a name="parmname773122018141"></a><a name="parmname773122018141"></a>“防护模式”</span>选择<span class="parmvalue" id="parmvalue1273122019147"><a name="parmvalue1273122019147"></a><a name="parmvalue1273122019147"></a>“其他”</span>时，<span class="parmvalue" id="parmvalue16731320181412"><a name="parmvalue16731320181412"></a><a name="parmvalue16731320181412"></a>“Referer”</span>对应的<span class="parmvalue" id="parmvalue19731192013140"><a name="parmvalue19731192013140"></a><a name="parmvalue19731192013140"></a>“内容”</span>填写为包含域名的完整URL链接，仅支持前缀匹配和精准匹配的逻辑，<span class="parmvalue" id="parmvalue2073152021416"><a name="parmvalue2073152021416"></a><a name="parmvalue2073152021416"></a>“内容”</span>里不能含有连续的多条斜线的配置，如<span class="parmvalue" id="parmvalue18731220151412"><a name="parmvalue18731220151412"></a><a name="parmvalue18731220151412"></a>“///admin”</span>，WAF引擎会将<span class="parmvalue" id="parmvalue17732122014143"><a name="parmvalue17732122014143"></a><a name="parmvalue17732122014143"></a>“///”</span>转为<span class="parmvalue" id="parmvalue10732202081416"><a name="parmvalue10732202081416"></a><a name="parmvalue10732202081416"></a>“/”</span>。</p>
    <p id="p77329207149"><a name="p77329207149"></a><a name="p77329207149"></a>例如：防护路径设置为<span class="parmvalue" id="parmvalue1973213208144"><a name="parmvalue1973213208144"></a><a name="parmvalue1973213208144"></a>“/admin”</span>，若用户不希望访问者从<span class="parmvalue" id="parmvalue1073217209147"><a name="parmvalue1073217209147"></a><a name="parmvalue1073217209147"></a>“www.test.com”</span>访问该页面，则<span class="parmname" id="parmname1673202016142"><a name="parmname1673202016142"></a><a name="parmname1673202016142"></a>“Referer”</span>对应的<span class="parmvalue" id="parmvalue7732122012148"><a name="parmvalue7732122012148"></a><a name="parmvalue7732122012148"></a>“Content”</span>设置为<span class="parmvalue" id="parmvalue9732162091417"><a name="parmvalue9732162091417"></a><a name="parmvalue9732162091417"></a>“http://www.test.com”</span></p>
    </div></div>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p16733142061418"><a name="p16733142061418"></a><a name="p16733142061418"></a>用户限速</p>
    </td>
    </tr>
    <tr id="row1673319205141"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p573302001416"><a name="p573302001416"></a><a name="p573302001416"></a>用户标识</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p1573311208146"><a name="p1573311208146"></a><a name="p1573311208146"></a><span class="parmname" id="parmname1473322019148"><a name="parmname1473322019148"></a><a name="parmname1473322019148"></a>“防护模式”</span>选择<span class="parmvalue" id="parmvalue13733120161410"><a name="parmvalue13733120161410"></a><a name="parmvalue13733120161410"></a>“用户限速”</span>时，需要设置Cookie字段名，即用户需要根据网站实际情况配置唯一可识别Web访问者的Cookie中的某属性变量名，用户标识的Cookie，不支持正则，必须完全匹配。如果用户没有设置Cookie键值，WAF会自动分配一个值。</p>
    <p id="p127331420171418"><a name="p127331420171418"></a><a name="p127331420171418"></a>例如：如果网站使用Cookie中的某个字段，name唯一标识用户，那么可以选取name字段来区分Web访问者。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p47331420141414"><a name="p47331420141414"></a><a name="p47331420141414"></a>name</p>
    </td>
    </tr>
    <tr id="row13734220141419"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p13733120111420"><a name="p13733120111420"></a><a name="p13733120111420"></a>限速频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p17733102001415"><a name="p17733102001415"></a><a name="p17733102001415"></a>单个Web访问者在限速周期内可以正常访问的次数，如果超过该访问次数，Web应用防火墙服务将暂停该Web访问者的访问。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p1173417206149"><a name="p1173417206149"></a><a name="p1173417206149"></a>10次/60秒</p>
    </td>
    </tr>
    <tr id="row4735102013144"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1573462071420"><a name="p1573462071420"></a><a name="p1573462071420"></a>防护动作</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p177341320101410"><a name="p177341320101410"></a><a name="p177341320101410"></a>当访问超过限制频率时，进行<span class="parmvalue" id="parmvalue4734192014142"><a name="parmvalue4734192014142"></a><a name="parmvalue4734192014142"></a>“人机验证”</span>或者<span class="parmvalue" id="parmvalue373402091412"><a name="parmvalue373402091412"></a><a name="parmvalue373402091412"></a>“阻断”</span>。</p>
    <a name="ul1273582011416"></a><a name="ul1273582011416"></a><ul id="ul1273582011416"><li class="MsoBodyText">人机验证：表示在指定时间内访问超过次数限制后弹出验证码，进行人机验证，完成验证后，请求将不受访问限制。</li><li class="MsoBodyText">阻断：表示在指定时间内访问超过次数限制将直接阻断。<div class="note" id="note1273512081414"><a name="note1273512081414"></a><a name="note1273512081414"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p473522013144"><a name="p473522013144"></a><a name="p473522013144"></a>当<span class="parmname" id="parmname147345201143"><a name="parmname147345201143"></a><a name="parmname147345201143"></a>“防护模式”</span>选择<span class="parmvalue" id="parmvalue15735122061420"><a name="parmvalue15735122061420"></a><a name="parmvalue15735122061420"></a>“其他”</span>时，<span class="parmname" id="parmname8735142011418"><a name="parmname8735142011418"></a><a name="parmname8735142011418"></a>“防护动作”</span>只能选择<span class="parmvalue" id="parmvalue19735420171412"><a name="parmvalue19735420171412"></a><a name="parmvalue19735420171412"></a>“阻断”</span>。</p>
    </div></div>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p9735192091414"><a name="p9735192091414"></a><a name="p9735192091414"></a>阻断</p>
    </td>
    </tr>
    <tr id="row7736420181410"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p17735172015144"><a name="p17735172015144"></a><a name="p17735172015144"></a>阻断时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p117365207143"><a name="p117365207143"></a><a name="p117365207143"></a>当<span class="parmname" id="parmname157361420111414"><a name="parmname157361420111414"></a><a name="parmname157361420111414"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue67361920141412"><a name="parmvalue67361920141412"></a><a name="parmvalue67361920141412"></a>“阻断”</span>时，可设置阻断后恢复正常访问页面的时间。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p973610202149"><a name="p973610202149"></a><a name="p973610202149"></a>600秒</p>
    </td>
    </tr>
    <tr id="row157374203148"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1873610201146"><a name="p1873610201146"></a><a name="p1873610201146"></a>阻断页面</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p20736520101416"><a name="p20736520101416"></a><a name="p20736520101416"></a>当<span class="parmname" id="parmname6736192020149"><a name="parmname6736192020149"></a><a name="parmname6736192020149"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue15736102061411"><a name="parmvalue15736102061411"></a><a name="parmvalue15736102061411"></a>“阻断”</span>时，需要设置，即当访问超过限速频率时，返回的错误页面。</p>
    <a name="ul47377202143"></a><a name="ul47377202143"></a><ul id="ul47377202143"><li>当选择<span class="parmvalue" id="parmvalue5736172071412"><a name="parmvalue5736172071412"></a><a name="parmvalue5736172071412"></a>“默认设置”</span>时，返回的错误页面为系统默认的阻断页面。</li><li>当选择<span class="parmvalue" id="parmvalue0737172081419"><a name="parmvalue0737172081419"></a><a name="parmvalue0737172081419"></a>“自定义”</span>，返回错误信息由用户自定义。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p1173772014147"><a name="p1173772014147"></a><a name="p1173772014147"></a>自定义</p>
    </td>
    </tr>
    <tr id="row16738920121413"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1473752013147"><a name="p1473752013147"></a><a name="p1473752013147"></a>页面类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p273816207148"><a name="p273816207148"></a><a name="p273816207148"></a>当<span class="parmname" id="parmname57371420181412"><a name="parmname57371420181412"></a><a name="parmname57371420181412"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue9737172021410"><a name="parmvalue9737172021410"></a><a name="parmvalue9737172021410"></a>“自定义”</span>时，可选择阻断页面的类型<span class="parmvalue" id="parmvalue11737102018149"><a name="parmvalue11737102018149"></a><a name="parmvalue11737102018149"></a>“application/json”</span>、<span class="parmvalue" id="parmvalue1373892081418"><a name="parmvalue1373892081418"></a><a name="parmvalue1373892081418"></a>“text/html”</span>或者<span class="parmvalue" id="parmvalue173814202141"><a name="parmvalue173814202141"></a><a name="parmvalue173814202141"></a>“text/xml”</span>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p1273842014142"><a name="p1273842014142"></a><a name="p1273842014142"></a>text/html</p>
    </td>
    </tr>
    <tr id="row87384209145"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p187381320171411"><a name="p187381320171411"></a><a name="p187381320171411"></a>页面内容</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p073872018149"><a name="p073872018149"></a><a name="p073872018149"></a>当<span class="parmname" id="parmname77388207141"><a name="parmname77388207141"></a><a name="parmname77388207141"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue1273810205142"><a name="parmvalue1273810205142"></a><a name="parmvalue1273810205142"></a>“自定义”</span>时，可设置自定义返回的内容。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p19738202021418"><a name="p19738202021418"></a><a name="p19738202021418"></a>&lt;html&gt;&lt;body&gt;Forbidden&lt;/body&gt;&lt;/html&gt;</p>
    </td>
    </tr>
    </tbody>
    </table>

8.  单击“确认添加“，在页面右上角弹出“添加成功“，添加的CC攻击防护规则展示在CC规则列表中。
    -   若需要修改添加的CC攻击防护规则时，可单击待修改的CC攻击防护规则所在行的“修改“，修改CC攻击防护规则。
    -   若需要删除用户自行添加的CC攻击防护规则时，可单击待删除的CC攻击防护规则所在行的“删除“，删除CC攻击防护规则。


## 防护效果<a name="section2969132523417"></a>

假如已添加域名“www.example.com“，且配置了如[图3](#fig172782071413)所示的CC防护规则。可参照以下步骤验证防护效果：

1.  清理浏览器缓存，在浏览器中输入防护域名，测试网站域名是否能正常访问。
2.  清理浏览器缓存，在浏览器中访问满足Cookie条件的“http://www.example.com/admin\(包含admin的任意页面\)“页面，在60秒内刷新页面10次，正常情况下，在第11次访问该页面时，返回自定义的拦截页面；600秒后刷新目标页面，页面访问正常。
3.  返回Web应用防火墙控制界面，在左侧导航树中，单击“防护事件“，进入“防护事件“页面，查看防护域名拦截日志。

