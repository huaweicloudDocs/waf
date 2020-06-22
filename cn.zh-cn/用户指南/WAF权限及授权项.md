# WAF权限及授权项<a name="waf_01_0244"></a>

如果您需要对您所拥有的WAF进行精细的权限管理，您可以使用统一身份认证服务（Identity and Access Management，IAM），如果华为云账号已经能满足您的要求，不需要创建独立的IAM用户，您可以跳过本章节，不影响您使用WAF服务的其它功能。

默认情况下，新建的IAM用户没有任何权限，您需要将其加入用户组，并给用户组授予策略或角色，才能使用户组中的用户获得相应的权限，这一过程称为授权。授权后，用户就可以基于已有权限对云服务进行操作。

权限根据授权的精细程度，分为[角色](https://support.huaweicloud.com/usermanual-iam/iam_01_0601.html)和[策略](https://support.huaweicloud.com/usermanual-iam/iam_01_0017.html)。角色以服务为粒度，是IAM最初提供的一种根据用户的工作职能定义权限的粗粒度授权机制。策略授权更加精细，可以精确到某个操作、资源和条件，能够满足企业对权限最小化的安全管控要求。

## 支持的授权项<a name="section1132991515465"></a>

策略包含系统策略和自定义策略，如果系统策略不满足授权要求，管理员可以创建自定义策略，并通过给用户组授予自定义策略来进行精细的访问控制。

-   权限：允许或拒绝某项操作。
-   授权项：自定义策略中支持的Action，在自定义策略中的Action中写入授权项，可以实现授权项对应的权限功能。

<a name="table8211143315354"></a>
<table><thead align="left"><tr id="row144381133183517"><th class="cellrowborder" valign="top" width="30.509999999999998%" id="mcps1.1.3.1.1"><p id="p1443820332357"><a name="p1443820332357"></a><a name="p1443820332357"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="69.49%" id="mcps1.1.3.1.2"><p id="p19438733133512"><a name="p19438733133512"></a><a name="p19438733133512"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row84382333355"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p78607282509"><a name="p78607282509"></a><a name="p78607282509"></a>查询防敏感信息泄漏规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1067841345112"><a name="p1067841345112"></a><a name="p1067841345112"></a>waf:antiLeakageRule:get</p>
</td>
</tr>
<tr id="row8646114211514"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p1864724225117"><a name="p1864724225117"></a><a name="p1864724225117"></a>查询网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p16647104265111"><a name="p16647104265111"></a><a name="p16647104265111"></a>waf:antiTamperRule:get</p>
</td>
</tr>
<tr id="row45747397522"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p857412391527"><a name="p857412391527"></a><a name="p857412391527"></a>查询CC攻击防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1574173945213"><a name="p1574173945213"></a><a name="p1574173945213"></a>waf:ccRule:get</p>
</td>
</tr>
<tr id="row679124410528"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p1979174414528"><a name="p1979174414528"></a><a name="p1979174414528"></a>查询精准访问防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p147984414529"><a name="p147984414529"></a><a name="p147984414529"></a>waf:preciseProtectionRule:get</p>
</td>
</tr>
<tr id="row19711248105216"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p17971164815219"><a name="p17971164815219"></a><a name="p17971164815219"></a>查询误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p4971194825214"><a name="p4971194825214"></a><a name="p4971194825214"></a>waf:falseAlarmMaskRule:get</p>
</td>
</tr>
<tr id="row722205515315"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p322255595312"><a name="p322255595312"></a><a name="p322255595312"></a>查询隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p722275520537"><a name="p722275520537"></a><a name="p722275520537"></a>waf:privacyRule:get</p>
</td>
</tr>
<tr id="row1726610596534"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p122671159125317"><a name="p122671159125317"></a><a name="p122671159125317"></a>查询黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p14267359155317"><a name="p14267359155317"></a><a name="p14267359155317"></a>waf:whiteBlackIpRule:get</p>
</td>
</tr>
<tr id="row11219105917521"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p2220159185213"><a name="p2220159185213"></a><a name="p2220159185213"></a>查询地址位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p32201159195220"><a name="p32201159195220"></a><a name="p32201159195220"></a>waf:geoIpRule:get</p>
</td>
</tr>
<tr id="row68157487554"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p781554810557"><a name="p781554810557"></a><a name="p781554810557"></a>查询证书</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p138155481553"><a name="p138155481553"></a><a name="p138155481553"></a>waf:certificate:get</p>
</td>
</tr>
<tr id="row1364305219557"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p7643195225515"><a name="p7643195225515"></a><a name="p7643195225515"></a>查询防护事件</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p464315215555"><a name="p464315215555"></a><a name="p464315215555"></a>waf:event:get</p>
</td>
</tr>
<tr id="row16142933185612"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p714343325617"><a name="p714343325617"></a><a name="p714343325617"></a>查询防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p91431334567"><a name="p91431334567"></a><a name="p91431334567"></a>waf:instance:get</p>
</td>
</tr>
<tr id="row10786736145616"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p57861236165618"><a name="p57861236165618"></a><a name="p57861236165618"></a>查询防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p187861536135611"><a name="p187861536135611"></a><a name="p187861536135611"></a>waf:policy:get</p>
</td>
</tr>
<tr id="row149704310579"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p169704395713"><a name="p169704395713"></a><a name="p169704395713"></a>查询用户套餐信息</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p497033105710"><a name="p497033105710"></a><a name="p497033105710"></a>waf:bundle:get</p>
</td>
</tr>
<tr id="row1535317145716"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p203531272574"><a name="p203531272574"></a><a name="p203531272574"></a>查询防护事件下载链接</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p19353107115712"><a name="p19353107115712"></a><a name="p19353107115712"></a>waf:dumpEventLink:get</p>
</td>
</tr>
<tr id="row1178853911582"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p1778843916581"><a name="p1778843916581"></a><a name="p1778843916581"></a>查询页面配置信息</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p20788173916589"><a name="p20788173916589"></a><a name="p20788173916589"></a>waf:consoleConfig:get</p>
</td>
</tr>
<tr id="row16348194325817"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p834818432587"><a name="p834818432587"></a><a name="p834818432587"></a>查询回源IP段</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p17348134315813"><a name="p17348134315813"></a><a name="p17348134315813"></a>waf:sourceIp:get</p>
</td>
</tr>
<tr id="row19555154613587"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p18555104610583"><a name="p18555104610583"></a><a name="p18555104610583"></a>更新防敏感信息泄漏规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p7555146115817"><a name="p7555146115817"></a><a name="p7555146115817"></a>waf:antiLeakageRule:put</p>
</td>
</tr>
<tr id="row164931625015"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p84937210012"><a name="p84937210012"></a><a name="p84937210012"></a>更新网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p14493621202"><a name="p14493621202"></a><a name="p14493621202"></a>waf:antiTamperRule:put</p>
</td>
</tr>
<tr id="row1362954919585"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p262924919582"><a name="p262924919582"></a><a name="p262924919582"></a>更新CC攻击防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1262924945817"><a name="p1262924945817"></a><a name="p1262924945817"></a>waf:ccRuleRule:put</p>
</td>
</tr>
<tr id="row6271410901"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p1928161019016"><a name="p1928161019016"></a><a name="p1928161019016"></a>更新精准访问防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p12841016017"><a name="p12841016017"></a><a name="p12841016017"></a>waf:preciseProtectionRule:put</p>
</td>
</tr>
<tr id="row1328210708"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p182821018020"><a name="p182821018020"></a><a name="p182821018020"></a>更新误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p172817101019"><a name="p172817101019"></a><a name="p172817101019"></a>waf:falseAlarmMaskRule:put</p>
</td>
</tr>
<tr id="row17877720912"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p5877220518"><a name="p5877220518"></a><a name="p5877220518"></a>更新隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p13877320214"><a name="p13877320214"></a><a name="p13877320214"></a>waf:privacyRule:put</p>
</td>
</tr>
<tr id="row2932827319"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p12932627116"><a name="p12932627116"></a><a name="p12932627116"></a>更新黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p169323271511"><a name="p169323271511"></a><a name="p169323271511"></a>waf:whiteBlackIpRule:put</p>
</td>
</tr>
<tr id="row1193214271411"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p126032450319"><a name="p126032450319"></a><a name="p126032450319"></a>更新地址位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1293272715118"><a name="p1293272715118"></a><a name="p1293272715118"></a>waf:geoIpRule:put</p>
</td>
</tr>
<tr id="row202358378119"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p32361337910"><a name="p32361337910"></a><a name="p32361337910"></a>更新防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p12236203717120"><a name="p12236203717120"></a><a name="p12236203717120"></a>waf:instance:put</p>
</td>
</tr>
<tr id="row20236183719114"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p42361337416"><a name="p42361337416"></a><a name="p42361337416"></a>更新防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1923612371512"><a name="p1923612371512"></a><a name="p1923612371512"></a>waf:policy:put</p>
</td>
</tr>
<tr id="row20236103717120"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p1323683711114"><a name="p1323683711114"></a><a name="p1323683711114"></a>删除防敏感信息泄漏规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p102362037312"><a name="p102362037312"></a><a name="p102362037312"></a>waf:antiLeakageRule:delete</p>
</td>
</tr>
<tr id="row2236203717113"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p22362371112"><a name="p22362371112"></a><a name="p22362371112"></a>删除网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p323620373114"><a name="p323620373114"></a><a name="p323620373114"></a>waf:antiTamperRule:delete</p>
</td>
</tr>
<tr id="row382616301348"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p12016331957"><a name="p12016331957"></a><a name="p12016331957"></a>删除CC攻击防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p48271130344"><a name="p48271130344"></a><a name="p48271130344"></a>waf:ccRule:delete</p>
</td>
</tr>
<tr id="row382719303411"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p682793018412"><a name="p682793018412"></a><a name="p682793018412"></a>删除精准访问防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p7827630148"><a name="p7827630148"></a><a name="p7827630148"></a>waf:preciseProtectionRule:delete</p>
</td>
</tr>
<tr id="row166863547510"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p156861854558"><a name="p156861854558"></a><a name="p156861854558"></a>删除误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p196861754357"><a name="p196861754357"></a><a name="p196861754357"></a>waf:falseAlarmMaskRule:delete</p>
</td>
</tr>
<tr id="row14354558753"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p6354155814517"><a name="p6354155814517"></a><a name="p6354155814517"></a>删除隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1935411583510"><a name="p1935411583510"></a><a name="p1935411583510"></a>waf:privacyRule:delete</p>
</td>
</tr>
<tr id="row185045541865"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p1250420541163"><a name="p1250420541163"></a><a name="p1250420541163"></a>删除黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1350419543613"><a name="p1350419543613"></a><a name="p1350419543613"></a>waf:whiteBlackIpRule:delete</p>
</td>
</tr>
<tr id="row8986208711"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p10987110573"><a name="p10987110573"></a><a name="p10987110573"></a>删除地址位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p8987001979"><a name="p8987001979"></a><a name="p8987001979"></a>waf:geoIpRule:delete</p>
</td>
</tr>
<tr id="row79871101376"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p5987202715"><a name="p5987202715"></a><a name="p5987202715"></a>删除防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p17987102714"><a name="p17987102714"></a><a name="p17987102714"></a>waf:instance:delete</p>
</td>
</tr>
<tr id="row1384372215819"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p178431422389"><a name="p178431422389"></a><a name="p178431422389"></a>删除防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p68431122888"><a name="p68431122888"></a><a name="p68431122888"></a>waf:policy:delete</p>
</td>
</tr>
<tr id="row79302720819"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p493327386"><a name="p493327386"></a><a name="p493327386"></a>创建防敏感信息泄漏规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1931527280"><a name="p1931527280"></a><a name="p1931527280"></a>waf:antiLeakageRule:create</p>
</td>
</tr>
<tr id="row189342719817"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p1894182718811"><a name="p1894182718811"></a><a name="p1894182718811"></a>创建网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p12944272817"><a name="p12944272817"></a><a name="p12944272817"></a>waf:antiTamperRule:create</p>
</td>
</tr>
<tr id="row88249285913"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p482542812919"><a name="p482542812919"></a><a name="p482542812919"></a>创建CC攻击防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1182552816914"><a name="p1182552816914"></a><a name="p1182552816914"></a>waf:ccRule:create</p>
</td>
</tr>
<tr id="row11802833095"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p188031733793"><a name="p188031733793"></a><a name="p188031733793"></a>创建精准访问防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p188031933099"><a name="p188031933099"></a><a name="p188031933099"></a>waf:preciseProtectionRule:create</p>
</td>
</tr>
<tr id="row148030337916"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p108032336915"><a name="p108032336915"></a><a name="p108032336915"></a>创建误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p88036331598"><a name="p88036331598"></a><a name="p88036331598"></a>waf:falseAlarmMaskRule:create</p>
</td>
</tr>
<tr id="row6537738792"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p353719381691"><a name="p353719381691"></a><a name="p353719381691"></a>创建隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1553716381910"><a name="p1553716381910"></a><a name="p1553716381910"></a>waf:privacyRule:create</p>
</td>
</tr>
<tr id="row1353793816916"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p19537338199"><a name="p19537338199"></a><a name="p19537338199"></a>创建黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p145379381911"><a name="p145379381911"></a><a name="p145379381911"></a>waf:whiteBlackIpRule:create</p>
</td>
</tr>
<tr id="row1537538898"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p95371738599"><a name="p95371738599"></a><a name="p95371738599"></a>创建地址位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p153815381396"><a name="p153815381396"></a><a name="p153815381396"></a>waf:geoIpRule:create</p>
</td>
</tr>
<tr id="row1253823811916"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p14538153818911"><a name="p14538153818911"></a><a name="p14538153818911"></a>创建证书</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p353814387919"><a name="p353814387919"></a><a name="p353814387919"></a>waf:certificate:create</p>
</td>
</tr>
<tr id="row3549165651116"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p85502056131113"><a name="p85502056131113"></a><a name="p85502056131113"></a>创建防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p95501956151116"><a name="p95501956151116"></a><a name="p95501956151116"></a>waf:instance:create</p>
</td>
</tr>
<tr id="row198494614126"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p48494610122"><a name="p48494610122"></a><a name="p48494610122"></a>创建防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p08491062129"><a name="p08491062129"></a><a name="p08491062129"></a>waf:policy:create</p>
</td>
</tr>
<tr id="row178494621216"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p484918691216"><a name="p484918691216"></a><a name="p484918691216"></a>查询防敏感信息泄漏规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p084966131219"><a name="p084966131219"></a><a name="p084966131219"></a>waf:antiLeakageRule:list</p>
</td>
</tr>
<tr id="row4444174310126"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p13445124351212"><a name="p13445124351212"></a><a name="p13445124351212"></a>查询网页防篡改规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p3445543151211"><a name="p3445543151211"></a><a name="p3445543151211"></a>waf:antiTamperRule:list</p>
</td>
</tr>
<tr id="row1844513437120"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p1244514391210"><a name="p1244514391210"></a><a name="p1244514391210"></a>查询CC攻击防护规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p9445174341213"><a name="p9445174341213"></a><a name="p9445174341213"></a>waf:ccRuleRule:list</p>
</td>
</tr>
<tr id="row10662104715128"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p4662847161210"><a name="p4662847161210"></a><a name="p4662847161210"></a>查询精准访问防护规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p166254712122"><a name="p166254712122"></a><a name="p166254712122"></a>waf:preciseProtectionRule:list</p>
</td>
</tr>
<tr id="row1666244716124"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p76623476125"><a name="p76623476125"></a><a name="p76623476125"></a>查询误报屏蔽规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1666211474129"><a name="p1666211474129"></a><a name="p1666211474129"></a>waf:falseAlarmMaskRule:list</p>
</td>
</tr>
<tr id="row8662124781215"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p18662114714123"><a name="p18662114714123"></a><a name="p18662114714123"></a>查询隐私屏蔽规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p12662124701216"><a name="p12662124701216"></a><a name="p12662124701216"></a>waf:privacyRule:list</p>
</td>
</tr>
<tr id="row1566816931613"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p16668998163"><a name="p16668998163"></a><a name="p16668998163"></a>查询黑白名单规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p1166913921614"><a name="p1166913921614"></a><a name="p1166913921614"></a>waf:whiteBlackIpRule:list</p>
</td>
</tr>
<tr id="row16356111621610"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p7365131616161"><a name="p7365131616161"></a><a name="p7365131616161"></a>查询地址位置访问控制规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p6382111641613"><a name="p6382111641613"></a><a name="p6382111641613"></a>waf:geoIpRule:list</p>
</td>
</tr>
<tr id="row738214162166"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p173821164162"><a name="p173821164162"></a><a name="p173821164162"></a>查询防护域名列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p938241651619"><a name="p938241651619"></a><a name="p938241651619"></a>waf:instance:list</p>
</td>
</tr>
<tr id="row8288112781813"><td class="cellrowborder" valign="top" width="30.509999999999998%" headers="mcps1.1.3.1.1 "><p id="p2289527101811"><a name="p2289527101811"></a><a name="p2289527101811"></a>查询防护策略列表</p>
</td>
<td class="cellrowborder" valign="top" width="69.49%" headers="mcps1.1.3.1.2 "><p id="p228962741810"><a name="p228962741810"></a><a name="p228962741810"></a>waf:policy:list</p>
</td>
</tr>
</tbody>
</table>

