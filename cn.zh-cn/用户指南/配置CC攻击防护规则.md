# 配置CC攻击防护规则<a name="waf_01_0009"></a>

该任务指导用户通过Web应用防火墙服务配置CC（Challenge Collapsar，以下简称CC）攻击防护规则。

CC攻击防护规则根据IP或Cookie字段名设置灵活的限速策略，精准识别CC攻击以及有效缓解CC攻击。

## 前提条件<a name="section2256777914731"></a>

-   已获取管理控制台的帐号和密码。
-   已添加防护域名。

## 操作步骤<a name="section61533550183130"></a>

1.  登录管理控制台（https://console.huaweicloud.com/）。
2.  单击页面上方的“服务列表“，选择“安全  \>  Web应用防火墙“，在左侧导航树中选择“域名配置“，进入“域名配置“页面。
3.  在目标域名所在行的“防护策略“栏中，单击策略名称，进入防护配置页面，如[图1](#waf_01_0008_fig164792010154510)所示。

    **图 1**  防护策略<a name="waf_01_0008_fig164792010154510"></a>  
    ![](figures/防护策略.jpg "防护策略")

4.  在“CC攻击防护“配置框中，单击“自定义CC攻击防护规则“，进入CC防护规则配置页面，如[图2](#fig102851827142620)所示。

    单击![](figures/关闭图标.jpg)，开启防护检测。

    **图 2**  CC防护规则配置框<a name="fig102851827142620"></a>  
    ![](figures/CC防护规则配置框.png "CC防护规则配置框")

5.  在页面左上角，单击“添加规则“，添加CC防护规则，如[图3](#fig2221052162213)所示，请根据[表1](#table99941318113516)配置参数。

    **图 3**  添加CC防护规则<a name="fig2221052162213"></a>  
    ![](figures/添加CC防护规则.jpg "添加CC防护规则")

    **表 1**  CC防护规则参数说明

    <a name="table99941318113516"></a>
    <table><thead align="left"><tr id="row19995918153510"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.4.1.1"><p id="p11170204863513"><a name="p11170204863513"></a><a name="p11170204863513"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="51%" id="mcps1.2.4.1.2"><p id="p99961118193514"><a name="p99961118193514"></a><a name="p99961118193514"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.3"><p id="p699601814351"><a name="p699601814351"></a><a name="p699601814351"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row159963188358"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p5894162393615"><a name="p5894162393615"></a><a name="p5894162393615"></a>路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.2 "><p id="p1080314361368"><a name="p1080314361368"></a><a name="p1080314361368"></a>CC防护的URL链接，不包含域名。</p>
    <a name="ul20810143683616"></a><a name="ul20810143683616"></a><ul id="ul20810143683616"><li>前缀匹配：填写的路径前缀与需要防护的路径相同即可。<p id="p1682623653615"><a name="p1682623653615"></a><a name="p1682623653615"></a>如果防护路径为<span class="parmvalue" id="parmvalue178335366361"><a name="parmvalue178335366361"></a><a name="parmvalue178335366361"></a>“/admin”</span>，该规则填写为<span class="parmvalue" id="parmvalue1283710367365"><a name="parmvalue1283710367365"></a><a name="parmvalue1283710367365"></a>“/admin*”</span>，该规则生效。</p>
    </li><li>完全匹配：需要防护的路径需要与此处填写的路径完全相等。<p id="p1285333620361"><a name="p1285333620361"></a><a name="p1285333620361"></a>如果防护路径为<span class="parmvalue" id="parmvalue88609362364"><a name="parmvalue88609362364"></a><a name="parmvalue88609362364"></a>“/admin”</span>，该规则必须填写为<span class="parmvalue" id="parmvalue1586415365362"><a name="parmvalue1586415365362"></a><a name="parmvalue1586415365362"></a>“/admin”</span>。</p>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.3 "><p id="p2944115243613"><a name="p2944115243613"></a><a name="p2944115243613"></a>/admin</p>
    </td>
    </tr>
    <tr id="row1499713189352"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1499711184353"><a name="p1499711184353"></a><a name="p1499711184353"></a>防护模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.2 "><a name="ul555831610497"></a><a name="ul555831610497"></a><ul id="ul555831610497"><li>IP限速：根据IP区分单个Web访问者。</li><li>用户限速：根据Cookie键值区分单个Web访问者。</li><li>其他：根据Referer（自定义请求访问的来源）字段区分单个Web访问者。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.3 "><p id="p13492614205019"><a name="p13492614205019"></a><a name="p13492614205019"></a>IP限速</p>
    </td>
    </tr>
    <tr id="row12136181112194"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p213641118192"><a name="p213641118192"></a><a name="p213641118192"></a>用户标识</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.2 "><p id="p10587161611499"><a name="p10587161611499"></a><a name="p10587161611499"></a>Cookie字段名，用户需要根据网站实际情况配置唯一可识别Web访问者的Cookie中的某属性变量名。如果用户没有设置Cookie键值，WAF会自动分配一个值。</p>
    <p id="p1359220166499"><a name="p1359220166499"></a><a name="p1359220166499"></a>例如：如果网站使用Cookie中的某个字段，name唯一标识用户，那么可以选取name字段来区分Web访问者。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.3 "><p id="p613741111915"><a name="p613741111915"></a><a name="p613741111915"></a>name</p>
    </td>
    </tr>
    <tr id="row1999918185358"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p15705184715378"><a name="p15705184715378"></a><a name="p15705184715378"></a>限速频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.2 "><p id="p876010445310"><a name="p876010445310"></a><a name="p876010445310"></a>单个Web访问者在限速周期内可以正常访问的次数，如果超过该访问次数，Web应用防火墙服务将暂停该Web访问者的访问。单位为<span class="parmname" id="parmname1052994325017"><a name="parmname1052994325017"></a><a name="parmname1052994325017"></a>“次/秒”</span>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.3 "><p id="p145702040319"><a name="p145702040319"></a><a name="p145702040319"></a>60次/10秒</p>
    </td>
    </tr>
    <tr id="row3394344114115"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p18395104484117"><a name="p18395104484117"></a><a name="p18395104484117"></a>防护动作</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.2 "><p id="p1337642115414"><a name="p1337642115414"></a><a name="p1337642115414"></a>当访问超过限制频率时，进行<span class="parmvalue" id="parmvalue1234494215412"><a name="parmvalue1234494215412"></a><a name="parmvalue1234494215412"></a>“人机验证”</span>或者<span class="parmvalue" id="parmvalue19350104217543"><a name="parmvalue19350104217543"></a><a name="parmvalue19350104217543"></a>“阻断”</span>。</p>
    <a name="ul1756281910212"></a><a name="ul1756281910212"></a><ul id="ul1756281910212"><li class="MsoBodyText">人机验证：表示在指定时间内访问超过次数限制后弹出验证码，进行人机验证，完成验证后，请求将不受访问限制。</li><li class="MsoBodyText">阻断：表示在指定时间内访问超过次数限制将直接阻断。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.3 "><p id="p52472231722"><a name="p52472231722"></a><a name="p52472231722"></a>阻断</p>
    </td>
    </tr>
    <tr id="row720934564212"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p15209104514210"><a name="p15209104514210"></a><a name="p15209104514210"></a>阻断时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.2 "><p id="p42102459424"><a name="p42102459424"></a><a name="p42102459424"></a>阻断后恢复正常访问页面的时间。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.3 "><p id="p72104455420"><a name="p72104455420"></a><a name="p72104455420"></a>600秒</p>
    </td>
    </tr>
    <tr id="row144310116562"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1085534975615"><a name="p1085534975615"></a><a name="p1085534975615"></a>阻断页面</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.2 "><p id="p95507237585"><a name="p95507237585"></a><a name="p95507237585"></a>当访问超过限速频率时，返回的错误页面。可以采用<span class="parmname" id="parmname205562023195817"><a name="parmname205562023195817"></a><a name="parmname205562023195817"></a>“默认设置”</span>或者<span class="parmname" id="parmname12562122375816"><a name="parmname12562122375816"></a><a name="parmname12562122375816"></a>“自定义”</span>。</p>
    <a name="ul145621723165816"></a><a name="ul145621723165816"></a><ul id="ul145621723165816"><li>当选择<span class="parmvalue" id="parmvalue1156542345816"><a name="parmvalue1156542345816"></a><a name="parmvalue1156542345816"></a>“默认设置”</span>时，返回错误为<span class="parmvalue" id="parmvalue8573142312587"><a name="parmvalue8573142312587"></a><a name="parmvalue8573142312587"></a>“Reuqest Blocked  Your request seems like a malicious access!  Alternatively, if you are administrator, you can access the WAF Console for handling false positives.”</span></li><li>当选择<span class="parmvalue" id="parmvalue1959122315817"><a name="parmvalue1959122315817"></a><a name="parmvalue1959122315817"></a>“自定义”</span>，返回错误信息由用户自定义。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.3 "><p id="p7445119569"><a name="p7445119569"></a><a name="p7445119569"></a>自定义</p>
    </td>
    </tr>
    <tr id="row95216110578"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1353021185711"><a name="p1353021185711"></a><a name="p1353021185711"></a>页面类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.2 "><p id="p35303117572"><a name="p35303117572"></a><a name="p35303117572"></a>当<span class="parmname" id="parmname564219901"><a name="parmname564219901"></a><a name="parmname564219901"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue156490919020"><a name="parmvalue156490919020"></a><a name="parmvalue156490919020"></a>“自定义”</span>时，可选择阻断页面的类型<span class="parmvalue" id="parmvalue66541591905"><a name="parmvalue66541591905"></a><a name="parmvalue66541591905"></a>“application/json”</span>、<span class="parmvalue" id="parmvalue566189804"><a name="parmvalue566189804"></a><a name="parmvalue566189804"></a>“text/html”</span>或者<span class="parmvalue" id="parmvalue126671291001"><a name="parmvalue126671291001"></a><a name="parmvalue126671291001"></a>“text/xml”</span>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.3 "><p id="p7531316573"><a name="p7531316573"></a><a name="p7531316573"></a>text/html</p>
    </td>
    </tr>
    <tr id="row119741813105719"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p159741713105710"><a name="p159741713105710"></a><a name="p159741713105710"></a>页面内容</p>
    </td>
    <td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.2 "><p id="p151425358014"><a name="p151425358014"></a><a name="p151425358014"></a>当<span class="parmname" id="parmname514713351307"><a name="parmname514713351307"></a><a name="parmname514713351307"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue51541535707"><a name="parmvalue51541535707"></a><a name="parmvalue51541535707"></a>“自定义”</span>时，可设置自定义返回的内容。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.3 "><p id="p2049013408416"><a name="p2049013408416"></a><a name="p2049013408416"></a>&lt;html&gt;&lt;body&gt;Forbidden&lt;/body&gt;&lt;/html&gt;</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“确认添加“，在页面右上角弹出“添加成功“，添加的CC攻击防护规则展示在CC规则列表中。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   若需要修改添加的CC攻击防护规则时，可单击待修改的CC攻击防护规则所在行的“修改“，修改CC攻击防护规则。  
    >-   若需要删除添加的CC攻击防护规则时，可单击待删除的CC攻击防护规则所在行的“删除“，删除CC攻击防护规则。  


