# 配置CC攻击防护规则<a name="waf_01_0009"></a>

该任务指导用户通过Web应用防火墙服务配置CC（Challenge Collapsar）攻击防护规则。

CC攻击防护规则根据IP、Cookie或者Referer字段设置灵活的限速策略，精准识别CC攻击以及有效缓解CC攻击。

## 前提条件<a name="section2256777914731"></a>

-   已获取管理控制台的帐号和密码。
-   已添加防护域名。

## 操作步骤<a name="section61533550183130"></a>

1.  登录管理控制台（https://console.huaweicloud.com/）。
2.  单击管理控制台左上角的![](figures/选择区域图标.jpg)，选择区域或项目。
3.  单击页面上方的“服务列表“，选择“安全  \>  Web应用防火墙“，在左侧导航树中选择“域名配置“，进入“域名配置“页面，如[图1](#waf_01_0008_fig164792010154510)所示。

    **图 1**  域名配置页面<a name="waf_01_0008_fig164792010154510"></a>  
    ![](figures/域名配置页面-10.png "域名配置页面-10")

4.  在目标域名所在行的“防护策略“栏中，单击“配置防护策略“，进入“防护配置“页面。
5.  在“CC攻击防护“配置框中，用户可根据自己的需要更改“状态“，单击“自定义CC攻击防护规则“，进入CC防护规则配置页面，如[图2](#fig102851827142620)所示。

    **图 2**  CC防护规则配置框<a name="fig102851827142620"></a>  
    ![](figures/CC防护规则配置框.png "CC防护规则配置框")

6.  在“CC防护“规则配置页面左上角，单击“添加规则“。
7.  在弹出的对话框中，添加CC防护规则，如[图3](#fig8736181862118)所示，请根据[表1](#table19744111819217)配置参数。

    **图 3**  添加CC防护规则<a name="fig8736181862118"></a>  
    ![](figures/添加CC防护规则.png "添加CC防护规则")

    **表 1**  CC防护规则参数说明

    <a name="table19744111819217"></a>
    <table><thead align="left"><tr id="row137372018152111"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.4.1.1"><p id="p1773791892116"><a name="p1773791892116"></a><a name="p1773791892116"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.88%" id="mcps1.2.4.1.2"><p id="p27379188215"><a name="p27379188215"></a><a name="p27379188215"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="30.12%" id="mcps1.2.4.1.3"><p id="p8737181818212"><a name="p8737181818212"></a><a name="p8737181818212"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1373871812117"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1373751862112"><a name="p1373751862112"></a><a name="p1373751862112"></a>路径</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p37371318202111"><a name="p37371318202111"></a><a name="p37371318202111"></a>CC防护的URL链接，不包含域名。</p>
    <a name="ul1515617591337"></a><a name="ul1515617591337"></a><ul id="ul1515617591337"><li>前缀匹配：以*结尾代表以该路径为前缀。例如，需要防护的路径为<span class="parmvalue" id="parmvalue1111962015414"><a name="parmvalue1111962015414"></a><a name="parmvalue1111962015414"></a>“/admin/test.php”</span>或 <span class="parmvalue" id="parmvalue5307927143"><a name="parmvalue5307927143"></a><a name="parmvalue5307927143"></a>“/adminabc”</span>，则路径可以填写为<span class="parmvalue" id="parmvalue12617113514412"><a name="parmvalue12617113514412"></a><a name="parmvalue12617113514412"></a>“/admin*”</span>。</li><li>精准匹配：需要防护的路径需要与此处填写的路径完全相等。例如，需要防护的路径为<span class="parmvalue" id="parmvalue1032614581447"><a name="parmvalue1032614581447"></a><a name="parmvalue1032614581447"></a>“/admin”</span>，该规则必须填写为<span class="parmvalue" id="parmvalue71301461752"><a name="parmvalue71301461752"></a><a name="parmvalue71301461752"></a>“/admin”</span>。</li></ul>
    <div class="note" id="note0434164315340"><a name="note0434164315340"></a><a name="note0434164315340"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul20707155819344"></a><a name="ul20707155819344"></a><ul id="ul20707155819344"><li>该路径不支持正则，仅支持前缀匹配和精准匹配的逻辑。</li><li>路径里不能含有连续的多条斜线的配置，如<span class="parmvalue" id="parmvalue15660135573716"><a name="parmvalue15660135573716"></a><a name="parmvalue15660135573716"></a>“///admin”</span>，WAF引擎会将<span class="parmvalue" id="parmvalue3913154823813"><a name="parmvalue3913154823813"></a><a name="parmvalue3913154823813"></a>“///”</span>转为<span class="parmvalue" id="parmvalue147935113816"><a name="parmvalue147935113816"></a><a name="parmvalue147935113816"></a>“/”</span>。</li></ul>
    </div></div>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p1173811852111"><a name="p1173811852111"></a><a name="p1173811852111"></a>/admin*</p>
    </td>
    </tr>
    <tr id="row1773971812119"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p773811822118"><a name="p773811822118"></a><a name="p773811822118"></a>防护模式</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><a name="ul77394180214"></a><a name="ul77394180214"></a><ul id="ul77394180214"><li>IP限速：根据IP区分单个Web访问者。</li><li>用户限速：根据Cookie键值区分单个Web访问者。</li><li>其他：根据Referer（自定义请求访问的来源）字段区分单个Web访问者。<div class="note" id="note8678492076"><a name="note8678492076"></a><a name="note8678492076"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p068134920713"><a name="p068134920713"></a><a name="p068134920713"></a>当<span class="parmname" id="parmname68812431599"><a name="parmname68812431599"></a><a name="parmname68812431599"></a>“防护模式”</span>选择<span class="parmvalue" id="parmvalue1988643591"><a name="parmvalue1988643591"></a><a name="parmvalue1988643591"></a>“其他”</span>时，<span class="parmvalue" id="parmvalue2549244121110"><a name="parmvalue2549244121110"></a><a name="parmvalue2549244121110"></a>“Referer”</span>对应的<span class="parmvalue" id="parmvalue10380628194010"><a name="parmvalue10380628194010"></a><a name="parmvalue10380628194010"></a>“内容”</span>填写为包含域名的完整URL链接，仅支持前缀匹配和精准匹配的逻辑，<span class="parmvalue" id="parmvalue134168569128"><a name="parmvalue134168569128"></a><a name="parmvalue134168569128"></a>“内容”</span>里不能含有连续的多条斜线的配置，如<span class="parmvalue" id="parmvalue1595175011228"><a name="parmvalue1595175011228"></a><a name="parmvalue1595175011228"></a>“///admin”</span>，WAF引擎会将<span class="parmvalue" id="parmvalue105951550182217"><a name="parmvalue105951550182217"></a><a name="parmvalue105951550182217"></a>“///”</span>转为<span class="parmvalue" id="parmvalue559645052219"><a name="parmvalue559645052219"></a><a name="parmvalue559645052219"></a>“/”</span>。</p>
    <p id="p12718311202113"><a name="p12718311202113"></a><a name="p12718311202113"></a>例如：防护路径设置为<span class="parmvalue" id="parmvalue13652152919480"><a name="parmvalue13652152919480"></a><a name="parmvalue13652152919480"></a>“/admin”</span>，若用户不希望访问者从<span class="parmvalue" id="parmvalue1655102904815"><a name="parmvalue1655102904815"></a><a name="parmvalue1655102904815"></a>“www.test.com”</span>访问该页面，则<span class="parmname" id="parmname765542984812"><a name="parmname765542984812"></a><a name="parmname765542984812"></a>“Referer”</span>对应的<span class="parmvalue" id="parmvalue455341372111"><a name="parmvalue455341372111"></a><a name="parmvalue455341372111"></a>“Content”</span>设置为<span class="parmvalue" id="parmvalue20657182964810"><a name="parmvalue20657182964810"></a><a name="parmvalue20657182964810"></a>“http://www.test.com”</span></p>
    </div></div>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p12641105306"><a name="p12641105306"></a><a name="p12641105306"></a>用户限速</p>
    </td>
    </tr>
    <tr id="row8739818162118"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1073931852111"><a name="p1073931852111"></a><a name="p1073931852111"></a>用户标识</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p87395187212"><a name="p87395187212"></a><a name="p87395187212"></a><span class="parmname" id="parmname17739171872111"><a name="parmname17739171872111"></a><a name="parmname17739171872111"></a>“防护模式”</span>选择<span class="parmvalue" id="parmvalue273920184217"><a name="parmvalue273920184217"></a><a name="parmvalue273920184217"></a>“用户限速”</span>时，需要设置Cookie字段名，即用户需要根据网站实际情况配置唯一可识别Web访问者的Cookie中的某属性变量名，用户标识的Cookie，不支持正则，必须完全匹配。如果用户没有设置Cookie键值，WAF会自动分配一个值。</p>
    <p id="p1573911812216"><a name="p1573911812216"></a><a name="p1573911812216"></a>例如：如果网站使用Cookie中的某个字段，name唯一标识用户，那么可以选取name字段来区分Web访问者。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p47391018152116"><a name="p47391018152116"></a><a name="p47391018152116"></a>name</p>
    </td>
    </tr>
    <tr id="row0741101862119"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p16739181862117"><a name="p16739181862117"></a><a name="p16739181862117"></a>限速频率</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p0741618112115"><a name="p0741618112115"></a><a name="p0741618112115"></a>单个Web访问者在限速周期内可以正常访问的次数，如果超过该访问次数，Web应用防火墙服务将暂停该Web访问者的访问。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p574111815216"><a name="p574111815216"></a><a name="p574111815216"></a>10次/60秒</p>
    </td>
    </tr>
    <tr id="row6741418122113"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p3741181822119"><a name="p3741181822119"></a><a name="p3741181822119"></a>防护动作</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p1474151814212"><a name="p1474151814212"></a><a name="p1474151814212"></a>当访问超过限制频率时，进行<span class="parmvalue" id="parmvalue107411218172119"><a name="parmvalue107411218172119"></a><a name="parmvalue107411218172119"></a>“人机验证”</span>或者<span class="parmvalue" id="parmvalue2741918142110"><a name="parmvalue2741918142110"></a><a name="parmvalue2741918142110"></a>“阻断”</span>。</p>
    <a name="ul374111183213"></a><a name="ul374111183213"></a><ul id="ul374111183213"><li class="MsoBodyText">人机验证：表示在指定时间内访问超过次数限制后弹出验证码，进行人机验证，完成验证后，请求将不受访问限制。</li><li class="MsoBodyText">阻断：表示在指定时间内访问超过次数限制将直接阻断。<div class="note" id="note151854308411"><a name="note151854308411"></a><a name="note151854308411"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1918615300417"><a name="p1918615300417"></a><a name="p1918615300417"></a>当<span class="parmname" id="parmname9951028104218"><a name="parmname9951028104218"></a><a name="parmname9951028104218"></a>“防护模式”</span>选择<span class="parmvalue" id="parmvalue189592816421"><a name="parmvalue189592816421"></a><a name="parmvalue189592816421"></a>“其他”</span>时，<span class="parmname" id="parmname1567554616436"><a name="parmname1567554616436"></a><a name="parmname1567554616436"></a>“防护动作”</span>只能选择<span class="parmvalue" id="parmvalue1534115919438"><a name="parmvalue1534115919438"></a><a name="parmvalue1534115919438"></a>“阻断”</span>。</p>
    </div></div>
    </li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p1774111819212"><a name="p1774111819212"></a><a name="p1774111819212"></a>阻断</p>
    </td>
    </tr>
    <tr id="row1274120181210"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p19741191892111"><a name="p19741191892111"></a><a name="p19741191892111"></a>阻断时长</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p1774110185217"><a name="p1774110185217"></a><a name="p1774110185217"></a>当<span class="parmname" id="parmname1174191813216"><a name="parmname1174191813216"></a><a name="parmname1174191813216"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue4741518152115"><a name="parmvalue4741518152115"></a><a name="parmvalue4741518152115"></a>“阻断”</span>时，可设置阻断后恢复正常访问页面的时间。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p20741121822113"><a name="p20741121822113"></a><a name="p20741121822113"></a>600秒</p>
    </td>
    </tr>
    <tr id="row8744101812218"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p1574181819218"><a name="p1574181819218"></a><a name="p1574181819218"></a>阻断页面</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p5743218112117"><a name="p5743218112117"></a><a name="p5743218112117"></a>当<span class="parmname" id="parmname56881346124512"><a name="parmname56881346124512"></a><a name="parmname56881346124512"></a>“防护动作”</span>选择<span class="parmvalue" id="parmvalue1268814694516"><a name="parmvalue1268814694516"></a><a name="parmvalue1268814694516"></a>“阻断”</span>时，需要设置，即当访问超过限速频率时，返回的错误页面。</p>
    <a name="ul15743111812116"></a><a name="ul15743111812116"></a><ul id="ul15743111812116"><li>当选择<span class="parmvalue" id="parmvalue1774321812112"><a name="parmvalue1774321812112"></a><a name="parmvalue1774321812112"></a>“默认设置”</span>时，返回的错误页面为系统默认的阻断页面。</li><li>当选择<span class="parmvalue" id="parmvalue7743141822119"><a name="parmvalue7743141822119"></a><a name="parmvalue7743141822119"></a>“自定义”</span>，返回错误信息由用户自定义。</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p374411811219"><a name="p374411811219"></a><a name="p374411811219"></a>自定义</p>
    </td>
    </tr>
    <tr id="row157442018202118"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p774418186216"><a name="p774418186216"></a><a name="p774418186216"></a>页面类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p1074481852115"><a name="p1074481852115"></a><a name="p1074481852115"></a>当<span class="parmname" id="parmname3744171872110"><a name="parmname3744171872110"></a><a name="parmname3744171872110"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue17744111812215"><a name="parmvalue17744111812215"></a><a name="parmvalue17744111812215"></a>“自定义”</span>时，可选择阻断页面的类型<span class="parmvalue" id="parmvalue1074415182213"><a name="parmvalue1074415182213"></a><a name="parmvalue1074415182213"></a>“application/json”</span>、<span class="parmvalue" id="parmvalue87444187217"><a name="parmvalue87444187217"></a><a name="parmvalue87444187217"></a>“text/html”</span>或者<span class="parmvalue" id="parmvalue1174481814213"><a name="parmvalue1174481814213"></a><a name="parmvalue1174481814213"></a>“text/xml”</span>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p117442018182120"><a name="p117442018182120"></a><a name="p117442018182120"></a>text/html</p>
    </td>
    </tr>
    <tr id="row1574471819217"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p207441181218"><a name="p207441181218"></a><a name="p207441181218"></a>页面内容</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.2 "><p id="p14744161812218"><a name="p14744161812218"></a><a name="p14744161812218"></a>当<span class="parmname" id="parmname5744151814212"><a name="parmname5744151814212"></a><a name="parmname5744151814212"></a>“阻断页面”</span>选择<span class="parmvalue" id="parmvalue17445187213"><a name="parmvalue17445187213"></a><a name="parmvalue17445187213"></a>“自定义”</span>时，可设置自定义返回的内容。</p>
    </td>
    <td class="cellrowborder" valign="top" width="30.12%" headers="mcps1.2.4.1.3 "><p id="p7744121802116"><a name="p7744121802116"></a><a name="p7744121802116"></a>&lt;html&gt;&lt;body&gt;Forbidden&lt;/body&gt;&lt;/html&gt;</p>
    </td>
    </tr>
    </tbody>
    </table>

8.  单击“确认添加“，在页面右上角弹出“添加成功“，添加的CC攻击防护规则展示在CC规则列表中。
    -   若需要修改添加的CC攻击防护规则时，可单击待修改的CC攻击防护规则所在行的“修改“，修改CC攻击防护规则。
    -   若需要删除用户自行添加的CC攻击防护规则时，可单击待删除的CC攻击防护规则所在行的“删除“，删除CC攻击防护规则。


