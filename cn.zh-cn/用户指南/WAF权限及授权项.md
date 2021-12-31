# WAF权限及授权项<a name="waf_01_0244"></a>

如果您需要对您所拥有的WAF进行精细的权限管理，您可以使用统一身份认证服务（Identity and Access Management，IAM），如果华为云帐号已经能满足您的要求，不需要创建独立的IAM用户，您可以跳过本章节，不影响您使用WAF服务的其它功能。

默认情况下，新建的IAM用户没有任何权限，您需要将其加入用户组，并给用户组授予策略或角色，才能使用户组中的用户获得相应的权限，这一过程称为授权。授权后，用户就可以基于已有权限对云服务进行操作。

权限根据授权的精细程度，分为[角色](https://support.huaweicloud.com/usermanual-iam/iam_01_0601.html)和[策略](https://support.huaweicloud.com/usermanual-iam/iam_01_0017.html)。角色以服务为粒度，是IAM最初提供的一种根据用户的工作职能定义权限的粗粒度授权机制。策略授权更加精细，可以精确到某个操作、资源和条件，能够满足企业对权限最小化的安全管控要求。

## 支持的授权项<a name="section1132991515465"></a>

策略包含系统策略和自定义策略，如果系统策略不满足授权要求，管理员可以创建自定义策略，并通过给用户组授予自定义策略来进行精细的访问控制。

-   权限：允许或拒绝某项操作。
-   授权项：自定义策略中支持的Action，在自定义策略中的Action中写入授权项，可以实现授权项对应的权限功能。

<a name="table8211143315354"></a>
<table><thead align="left"><tr id="row144381133183517"><th class="cellrowborder" valign="top" width="24.76247624762476%" id="mcps1.1.5.1.1"><p id="p1443820332357"><a name="p1443820332357"></a><a name="p1443820332357"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="33.803380338033804%" id="mcps1.1.5.1.2"><p id="p19438733133512"><a name="p19438733133512"></a><a name="p19438733133512"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="24.18241824182418%" id="mcps1.1.5.1.3"><p id="p5609151914280"><a name="p5609151914280"></a><a name="p5609151914280"></a>IAM项目(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="17.25172517251725%" id="mcps1.1.5.1.4"><p id="p95277361933"><a name="p95277361933"></a><a name="p95277361933"></a>企业项目(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row84382333355"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p78607282509"><a name="p78607282509"></a><a name="p78607282509"></a>查询防敏感信息泄漏规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1067841345112"><a name="p1067841345112"></a><a name="p1067841345112"></a>waf:antiLeakageRule:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p136094191287"><a name="p136094191287"></a><a name="p136094191287"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1971852813010"><a name="p1971852813010"></a><a name="p1971852813010"></a>√</p>
</td>
</tr>
<tr id="row8646114211514"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1864724225117"><a name="p1864724225117"></a><a name="p1864724225117"></a>查询网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p16647104265111"><a name="p16647104265111"></a><a name="p16647104265111"></a>waf:antiTamperRule:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p5609171922817"><a name="p5609171922817"></a><a name="p5609171922817"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p17727828143012"><a name="p17727828143012"></a><a name="p17727828143012"></a>√</p>
</td>
</tr>
<tr id="row45747397522"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p857412391527"><a name="p857412391527"></a><a name="p857412391527"></a>查询CC攻击防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1574173945213"><a name="p1574173945213"></a><a name="p1574173945213"></a>waf:ccRule:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p136093194281"><a name="p136093194281"></a><a name="p136093194281"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1873882810306"><a name="p1873882810306"></a><a name="p1873882810306"></a>√</p>
</td>
</tr>
<tr id="row679124410528"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1979174414528"><a name="p1979174414528"></a><a name="p1979174414528"></a>查询精准访问防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p147984414529"><a name="p147984414529"></a><a name="p147984414529"></a>waf:preciseProtectionRule:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p4108125412918"><a name="p4108125412918"></a><a name="p4108125412918"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p474762812309"><a name="p474762812309"></a><a name="p474762812309"></a>√</p>
</td>
</tr>
<tr id="row19711248105216"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p17971164815219"><a name="p17971164815219"></a><a name="p17971164815219"></a>查询误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p4971194825214"><a name="p4971194825214"></a><a name="p4971194825214"></a>waf:falseAlarmMaskRule:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p213315442916"><a name="p213315442916"></a><a name="p213315442916"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p7756528143011"><a name="p7756528143011"></a><a name="p7756528143011"></a>√</p>
</td>
</tr>
<tr id="row722205515315"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p322255595312"><a name="p322255595312"></a><a name="p322255595312"></a>查询隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p722275520537"><a name="p722275520537"></a><a name="p722275520537"></a>waf:privacyRule:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p616415422910"><a name="p616415422910"></a><a name="p616415422910"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p15766192820302"><a name="p15766192820302"></a><a name="p15766192820302"></a>√</p>
</td>
</tr>
<tr id="row1726610596534"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p122671159125317"><a name="p122671159125317"></a><a name="p122671159125317"></a>查询黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p14267359155317"><a name="p14267359155317"></a><a name="p14267359155317"></a>waf:whiteBlackIpRule:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p11741954122913"><a name="p11741954122913"></a><a name="p11741954122913"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p197740288306"><a name="p197740288306"></a><a name="p197740288306"></a>√</p>
</td>
</tr>
<tr id="row11219105917521"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p2220159185213"><a name="p2220159185213"></a><a name="p2220159185213"></a>查询地址位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p32201159195220"><a name="p32201159195220"></a><a name="p32201159195220"></a>waf:geoIpRule:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p7184205414290"><a name="p7184205414290"></a><a name="p7184205414290"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1678432812304"><a name="p1678432812304"></a><a name="p1678432812304"></a>√</p>
</td>
</tr>
<tr id="row68157487554"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p781554810557"><a name="p781554810557"></a><a name="p781554810557"></a>查询证书</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p138155481553"><a name="p138155481553"></a><a name="p138155481553"></a>waf:certificate:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p181931254152911"><a name="p181931254152911"></a><a name="p181931254152911"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p117941728133015"><a name="p117941728133015"></a><a name="p117941728133015"></a>√</p>
</td>
</tr>
<tr id="row1374983065816"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p8947549185811"><a name="p8947549185811"></a><a name="p8947549185811"></a>修改WAF证书</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p394734995816"><a name="p394734995816"></a><a name="p394734995816"></a>waf:certificate:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p364115512587"><a name="p364115512587"></a><a name="p364115512587"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p564185511586"><a name="p564185511586"></a><a name="p564185511586"></a>√</p>
</td>
</tr>
<tr id="row118655279596"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p157039547597"><a name="p157039547597"></a><a name="p157039547597"></a>应用证书到域名</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p12703145405918"><a name="p12703145405918"></a><a name="p12703145405918"></a>waf:certificate:apply</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p105214591594"><a name="p105214591594"></a><a name="p105214591594"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p2521185910596"><a name="p2521185910596"></a><a name="p2521185910596"></a>√</p>
</td>
</tr>
<tr id="row1364305219557"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p7643195225515"><a name="p7643195225515"></a><a name="p7643195225515"></a>查询防护事件</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p464315215555"><a name="p464315215555"></a><a name="p464315215555"></a>waf:event:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p020565492912"><a name="p020565492912"></a><a name="p020565492912"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p48044283304"><a name="p48044283304"></a><a name="p48044283304"></a>√</p>
</td>
</tr>
<tr id="row16142933185612"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p714343325617"><a name="p714343325617"></a><a name="p714343325617"></a>查询防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p91431334567"><a name="p91431334567"></a><a name="p91431334567"></a>waf:instance:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p521419543295"><a name="p521419543295"></a><a name="p521419543295"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p48131928153017"><a name="p48131928153017"></a><a name="p48131928153017"></a>√</p>
</td>
</tr>
<tr id="row10786736145616"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p57861236165618"><a name="p57861236165618"></a><a name="p57861236165618"></a>查询防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p187861536135611"><a name="p187861536135611"></a><a name="p187861536135611"></a>waf:policy:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p522715416299"><a name="p522715416299"></a><a name="p522715416299"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p8821122813306"><a name="p8821122813306"></a><a name="p8821122813306"></a>√</p>
</td>
</tr>
<tr id="row149704310579"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p169704395713"><a name="p169704395713"></a><a name="p169704395713"></a>查询用户套餐信息</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p497033105710"><a name="p497033105710"></a><a name="p497033105710"></a>waf:bundle:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p123765413295"><a name="p123765413295"></a><a name="p123765413295"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p168321528123012"><a name="p168321528123012"></a><a name="p168321528123012"></a>√</p>
</td>
</tr>
<tr id="row1535317145716"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p203531272574"><a name="p203531272574"></a><a name="p203531272574"></a>查询防护事件下载链接</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p19353107115712"><a name="p19353107115712"></a><a name="p19353107115712"></a>waf:dumpEventLink:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p724511545296"><a name="p724511545296"></a><a name="p724511545296"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p15843428123019"><a name="p15843428123019"></a><a name="p15843428123019"></a>√</p>
</td>
</tr>
<tr id="row1178853911582"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1778843916581"><a name="p1778843916581"></a><a name="p1778843916581"></a>查询页面配置信息</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p20788173916589"><a name="p20788173916589"></a><a name="p20788173916589"></a>waf:consoleConfig:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p2255954162911"><a name="p2255954162911"></a><a name="p2255954162911"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p385272813306"><a name="p385272813306"></a><a name="p385272813306"></a>√</p>
</td>
</tr>
<tr id="row16348194325817"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p834818432587"><a name="p834818432587"></a><a name="p834818432587"></a>查询回源IP段</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p17348134315813"><a name="p17348134315813"></a><a name="p17348134315813"></a>waf:sourceIp:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p202669542290"><a name="p202669542290"></a><a name="p202669542290"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p12524131914307"><a name="p12524131914307"></a><a name="p12524131914307"></a>√</p>
</td>
</tr>
<tr id="row19555154613587"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p18555104610583"><a name="p18555104610583"></a><a name="p18555104610583"></a>更新防敏感信息泄漏规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p7555146115817"><a name="p7555146115817"></a><a name="p7555146115817"></a>waf:antiLeakageRule:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p172769549293"><a name="p172769549293"></a><a name="p172769549293"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p0536319193018"><a name="p0536319193018"></a><a name="p0536319193018"></a>√</p>
</td>
</tr>
<tr id="row164931625015"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p84937210012"><a name="p84937210012"></a><a name="p84937210012"></a>更新网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p14493621202"><a name="p14493621202"></a><a name="p14493621202"></a>waf:antiTamperRule:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p328635411292"><a name="p328635411292"></a><a name="p328635411292"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p11546141983012"><a name="p11546141983012"></a><a name="p11546141983012"></a>√</p>
</td>
</tr>
<tr id="row1362954919585"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p262924919582"><a name="p262924919582"></a><a name="p262924919582"></a>更新CC攻击防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1262924945817"><a name="p1262924945817"></a><a name="p1262924945817"></a>waf:ccRuleRule:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1296155492916"><a name="p1296155492916"></a><a name="p1296155492916"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p755691963011"><a name="p755691963011"></a><a name="p755691963011"></a>√</p>
</td>
</tr>
<tr id="row6271410901"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1928161019016"><a name="p1928161019016"></a><a name="p1928161019016"></a>更新精准访问防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p12841016017"><a name="p12841016017"></a><a name="p12841016017"></a>waf:preciseProtectionRule:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p133051054192918"><a name="p133051054192918"></a><a name="p133051054192918"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p6567111963018"><a name="p6567111963018"></a><a name="p6567111963018"></a>√</p>
</td>
</tr>
<tr id="row1328210708"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p182821018020"><a name="p182821018020"></a><a name="p182821018020"></a>更新误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p172817101019"><a name="p172817101019"></a><a name="p172817101019"></a>waf:falseAlarmMaskRule:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p9315155415297"><a name="p9315155415297"></a><a name="p9315155415297"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1257821917309"><a name="p1257821917309"></a><a name="p1257821917309"></a>√</p>
</td>
</tr>
<tr id="row17877720912"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p5877220518"><a name="p5877220518"></a><a name="p5877220518"></a>更新隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p13877320214"><a name="p13877320214"></a><a name="p13877320214"></a>waf:privacyRule:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1232610540297"><a name="p1232610540297"></a><a name="p1232610540297"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p13588101917304"><a name="p13588101917304"></a><a name="p13588101917304"></a>√</p>
</td>
</tr>
<tr id="row2932827319"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p12932627116"><a name="p12932627116"></a><a name="p12932627116"></a>更新黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p169323271511"><a name="p169323271511"></a><a name="p169323271511"></a>waf:whiteBlackIpRule:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1733525411299"><a name="p1733525411299"></a><a name="p1733525411299"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p959811993010"><a name="p959811993010"></a><a name="p959811993010"></a>√</p>
</td>
</tr>
<tr id="row1193214271411"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p126032450319"><a name="p126032450319"></a><a name="p126032450319"></a>更新地址位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1293272715118"><a name="p1293272715118"></a><a name="p1293272715118"></a>waf:geoIpRule:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p4343754122914"><a name="p4343754122914"></a><a name="p4343754122914"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p66101019133013"><a name="p66101019133013"></a><a name="p66101019133013"></a>√</p>
</td>
</tr>
<tr id="row202358378119"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p32361337910"><a name="p32361337910"></a><a name="p32361337910"></a>更新防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p12236203717120"><a name="p12236203717120"></a><a name="p12236203717120"></a>waf:instance:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p133521354122915"><a name="p133521354122915"></a><a name="p133521354122915"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p7619181923016"><a name="p7619181923016"></a><a name="p7619181923016"></a>√</p>
</td>
</tr>
<tr id="row20236183719114"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p42361337416"><a name="p42361337416"></a><a name="p42361337416"></a>更新防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1923612371512"><a name="p1923612371512"></a><a name="p1923612371512"></a>waf:policy:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p536315415295"><a name="p536315415295"></a><a name="p536315415295"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1162821910301"><a name="p1162821910301"></a><a name="p1162821910301"></a>√</p>
</td>
</tr>
<tr id="row20236103717120"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1323683711114"><a name="p1323683711114"></a><a name="p1323683711114"></a>删除防敏感信息泄漏规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p102362037312"><a name="p102362037312"></a><a name="p102362037312"></a>waf:antiLeakageRule:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p6373185482915"><a name="p6373185482915"></a><a name="p6373185482915"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p11637419103011"><a name="p11637419103011"></a><a name="p11637419103011"></a>√</p>
</td>
</tr>
<tr id="row2236203717113"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p22362371112"><a name="p22362371112"></a><a name="p22362371112"></a>删除网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p323620373114"><a name="p323620373114"></a><a name="p323620373114"></a>waf:antiTamperRule:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p13381145462915"><a name="p13381145462915"></a><a name="p13381145462915"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p464816198302"><a name="p464816198302"></a><a name="p464816198302"></a>√</p>
</td>
</tr>
<tr id="row382616301348"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p12016331957"><a name="p12016331957"></a><a name="p12016331957"></a>删除CC攻击防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p48271130344"><a name="p48271130344"></a><a name="p48271130344"></a>waf:ccRule:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p839125412298"><a name="p839125412298"></a><a name="p839125412298"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p136601619193015"><a name="p136601619193015"></a><a name="p136601619193015"></a>√</p>
</td>
</tr>
<tr id="row382719303411"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p682793018412"><a name="p682793018412"></a><a name="p682793018412"></a>删除精准访问防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p7827630148"><a name="p7827630148"></a><a name="p7827630148"></a>waf:preciseProtectionRule:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p134020543294"><a name="p134020543294"></a><a name="p134020543294"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1567051923012"><a name="p1567051923012"></a><a name="p1567051923012"></a>√</p>
</td>
</tr>
<tr id="row166863547510"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p156861854558"><a name="p156861854558"></a><a name="p156861854558"></a>删除误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p196861754357"><a name="p196861754357"></a><a name="p196861754357"></a>waf:falseAlarmMaskRule:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p164112054152918"><a name="p164112054152918"></a><a name="p164112054152918"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p166835196302"><a name="p166835196302"></a><a name="p166835196302"></a>√</p>
</td>
</tr>
<tr id="row14354558753"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p6354155814517"><a name="p6354155814517"></a><a name="p6354155814517"></a>删除隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1935411583510"><a name="p1935411583510"></a><a name="p1935411583510"></a>waf:privacyRule:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p2420135412294"><a name="p2420135412294"></a><a name="p2420135412294"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1169391913016"><a name="p1169391913016"></a><a name="p1169391913016"></a>√</p>
</td>
</tr>
<tr id="row185045541865"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1250420541163"><a name="p1250420541163"></a><a name="p1250420541163"></a>删除黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1350419543613"><a name="p1350419543613"></a><a name="p1350419543613"></a>waf:whiteBlackIpRule:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p14429115422917"><a name="p14429115422917"></a><a name="p14429115422917"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p070331916305"><a name="p070331916305"></a><a name="p070331916305"></a>√</p>
</td>
</tr>
<tr id="row8986208711"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p10987110573"><a name="p10987110573"></a><a name="p10987110573"></a>删除地址位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p8987001979"><a name="p8987001979"></a><a name="p8987001979"></a>waf:geoIpRule:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1443913540291"><a name="p1443913540291"></a><a name="p1443913540291"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1371311983011"><a name="p1371311983011"></a><a name="p1371311983011"></a>√</p>
</td>
</tr>
<tr id="row79871101376"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p5987202715"><a name="p5987202715"></a><a name="p5987202715"></a>删除防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p17987102714"><a name="p17987102714"></a><a name="p17987102714"></a>waf:instance:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1844819545297"><a name="p1844819545297"></a><a name="p1844819545297"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p2072371910302"><a name="p2072371910302"></a><a name="p2072371910302"></a>√</p>
</td>
</tr>
<tr id="row1384372215819"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p178431422389"><a name="p178431422389"></a><a name="p178431422389"></a>删除防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p68431122888"><a name="p68431122888"></a><a name="p68431122888"></a>waf:policy:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p94591054112918"><a name="p94591054112918"></a><a name="p94591054112918"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p16734121919303"><a name="p16734121919303"></a><a name="p16734121919303"></a>√</p>
</td>
</tr>
<tr id="row79302720819"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p493327386"><a name="p493327386"></a><a name="p493327386"></a>创建防敏感信息泄漏规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1931527280"><a name="p1931527280"></a><a name="p1931527280"></a>waf:antiLeakageRule:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p104661654102919"><a name="p104661654102919"></a><a name="p104661654102919"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p37445197304"><a name="p37445197304"></a><a name="p37445197304"></a>√</p>
</td>
</tr>
<tr id="row189342719817"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1894182718811"><a name="p1894182718811"></a><a name="p1894182718811"></a>创建网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p12944272817"><a name="p12944272817"></a><a name="p12944272817"></a>waf:antiTamperRule:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1647455413291"><a name="p1647455413291"></a><a name="p1647455413291"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p17753619103018"><a name="p17753619103018"></a><a name="p17753619103018"></a>√</p>
</td>
</tr>
<tr id="row88249285913"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p482542812919"><a name="p482542812919"></a><a name="p482542812919"></a>创建CC攻击防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1182552816914"><a name="p1182552816914"></a><a name="p1182552816914"></a>waf:ccRule:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1048412549299"><a name="p1048412549299"></a><a name="p1048412549299"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p19762101918306"><a name="p19762101918306"></a><a name="p19762101918306"></a>√</p>
</td>
</tr>
<tr id="row11802833095"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p188031733793"><a name="p188031733793"></a><a name="p188031733793"></a>创建精准访问防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p188031933099"><a name="p188031933099"></a><a name="p188031933099"></a>waf:preciseProtectionRule:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p7493185412910"><a name="p7493185412910"></a><a name="p7493185412910"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p2077241918301"><a name="p2077241918301"></a><a name="p2077241918301"></a>√</p>
</td>
</tr>
<tr id="row148030337916"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p108032336915"><a name="p108032336915"></a><a name="p108032336915"></a>创建误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p88036331598"><a name="p88036331598"></a><a name="p88036331598"></a>waf:falseAlarmMaskRule:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p15501105452912"><a name="p15501105452912"></a><a name="p15501105452912"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p878012198309"><a name="p878012198309"></a><a name="p878012198309"></a>√</p>
</td>
</tr>
<tr id="row6537738792"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p353719381691"><a name="p353719381691"></a><a name="p353719381691"></a>创建隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1553716381910"><a name="p1553716381910"></a><a name="p1553716381910"></a>waf:privacyRule:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p13511165442918"><a name="p13511165442918"></a><a name="p13511165442918"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p279071993012"><a name="p279071993012"></a><a name="p279071993012"></a>√</p>
</td>
</tr>
<tr id="row1353793816916"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p19537338199"><a name="p19537338199"></a><a name="p19537338199"></a>创建黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p145379381911"><a name="p145379381911"></a><a name="p145379381911"></a>waf:whiteBlackIpRule:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p9519105416293"><a name="p9519105416293"></a><a name="p9519105416293"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p20799161910308"><a name="p20799161910308"></a><a name="p20799161910308"></a>√</p>
</td>
</tr>
<tr id="row1537538898"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p95371738599"><a name="p95371738599"></a><a name="p95371738599"></a>创建地址位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p153815381396"><a name="p153815381396"></a><a name="p153815381396"></a>waf:geoIpRule:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p7530954132918"><a name="p7530954132918"></a><a name="p7530954132918"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p7809619183011"><a name="p7809619183011"></a><a name="p7809619183011"></a>√</p>
</td>
</tr>
<tr id="row1253823811916"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p14538153818911"><a name="p14538153818911"></a><a name="p14538153818911"></a>创建证书</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p353814387919"><a name="p353814387919"></a><a name="p353814387919"></a>waf:certificate:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p7539154182912"><a name="p7539154182912"></a><a name="p7539154182912"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p98201192309"><a name="p98201192309"></a><a name="p98201192309"></a>√</p>
</td>
</tr>
<tr id="row3549165651116"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p85502056131113"><a name="p85502056131113"></a><a name="p85502056131113"></a>创建防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p95501956151116"><a name="p95501956151116"></a><a name="p95501956151116"></a>waf:instance:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p15551175492912"><a name="p15551175492912"></a><a name="p15551175492912"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p28291219153015"><a name="p28291219153015"></a><a name="p28291219153015"></a>√</p>
</td>
</tr>
<tr id="row198494614126"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p48494610122"><a name="p48494610122"></a><a name="p48494610122"></a>创建防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p08491062129"><a name="p08491062129"></a><a name="p08491062129"></a>waf:policy:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p165601854202916"><a name="p165601854202916"></a><a name="p165601854202916"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p583881917306"><a name="p583881917306"></a><a name="p583881917306"></a>√</p>
</td>
</tr>
<tr id="row178494621216"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p484918691216"><a name="p484918691216"></a><a name="p484918691216"></a>查询防敏感信息泄漏规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p084966131219"><a name="p084966131219"></a><a name="p084966131219"></a>waf:antiLeakageRule:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p55681254182911"><a name="p55681254182911"></a><a name="p55681254182911"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1084801943020"><a name="p1084801943020"></a><a name="p1084801943020"></a>√</p>
</td>
</tr>
<tr id="row4444174310126"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p13445124351212"><a name="p13445124351212"></a><a name="p13445124351212"></a>查询网页防篡改规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p3445543151211"><a name="p3445543151211"></a><a name="p3445543151211"></a>waf:antiTamperRule:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1576155422912"><a name="p1576155422912"></a><a name="p1576155422912"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p17859111910307"><a name="p17859111910307"></a><a name="p17859111910307"></a>√</p>
</td>
</tr>
<tr id="row1844513437120"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1244514391210"><a name="p1244514391210"></a><a name="p1244514391210"></a>查询CC攻击防护规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p9445174341213"><a name="p9445174341213"></a><a name="p9445174341213"></a>waf:ccRuleRule:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p458415492911"><a name="p458415492911"></a><a name="p458415492911"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p6870319113011"><a name="p6870319113011"></a><a name="p6870319113011"></a>√</p>
</td>
</tr>
<tr id="row10662104715128"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p4662847161210"><a name="p4662847161210"></a><a name="p4662847161210"></a>查询精准访问防护规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p166254712122"><a name="p166254712122"></a><a name="p166254712122"></a>waf:preciseProtectionRule:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p5593125415299"><a name="p5593125415299"></a><a name="p5593125415299"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p487981913307"><a name="p487981913307"></a><a name="p487981913307"></a>√</p>
</td>
</tr>
<tr id="row1666244716124"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p76623476125"><a name="p76623476125"></a><a name="p76623476125"></a>查询误报屏蔽规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1666211474129"><a name="p1666211474129"></a><a name="p1666211474129"></a>waf:falseAlarmMaskRule:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1460195422918"><a name="p1460195422918"></a><a name="p1460195422918"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p98901719183012"><a name="p98901719183012"></a><a name="p98901719183012"></a>√</p>
</td>
</tr>
<tr id="row8662124781215"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p18662114714123"><a name="p18662114714123"></a><a name="p18662114714123"></a>查询隐私屏蔽规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p12662124701216"><a name="p12662124701216"></a><a name="p12662124701216"></a>waf:privacyRule:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p761095452918"><a name="p761095452918"></a><a name="p761095452918"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p16900519143012"><a name="p16900519143012"></a><a name="p16900519143012"></a>√</p>
</td>
</tr>
<tr id="row1566816931613"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p16668998163"><a name="p16668998163"></a><a name="p16668998163"></a>查询黑白名单规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1166913921614"><a name="p1166913921614"></a><a name="p1166913921614"></a>waf:whiteBlackIpRule:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p15620205442910"><a name="p15620205442910"></a><a name="p15620205442910"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p12909319143018"><a name="p12909319143018"></a><a name="p12909319143018"></a>√</p>
</td>
</tr>
<tr id="row16356111621610"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p7365131616161"><a name="p7365131616161"></a><a name="p7365131616161"></a>查询地址位置访问控制规则列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p6382111641613"><a name="p6382111641613"></a><a name="p6382111641613"></a>waf:geoIpRule:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p18629105416294"><a name="p18629105416294"></a><a name="p18629105416294"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1892311913305"><a name="p1892311913305"></a><a name="p1892311913305"></a>√</p>
</td>
</tr>
<tr id="row738214162166"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p173821164162"><a name="p173821164162"></a><a name="p173821164162"></a>查询防护域名列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p938241651619"><a name="p938241651619"></a><a name="p938241651619"></a>waf:instance:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p463705482910"><a name="p463705482910"></a><a name="p463705482910"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p9936101917303"><a name="p9936101917303"></a><a name="p9936101917303"></a>√</p>
</td>
</tr>
<tr id="row8288112781813"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p2289527101811"><a name="p2289527101811"></a><a name="p2289527101811"></a>查询防护策略列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p228962741810"><a name="p228962741810"></a><a name="p228962741810"></a>waf:policy:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p0612161913282"><a name="p0612161913282"></a><a name="p0612161913282"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p3947121916302"><a name="p3947121916302"></a><a name="p3947121916302"></a>√</p>
</td>
</tr>
<tr id="row16456715192719"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1645712157271"><a name="p1645712157271"></a><a name="p1645712157271"></a>查询云模式计费资源</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p12457141516275"><a name="p12457141516275"></a><a name="p12457141516275"></a>waf:subscription:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p54571315102714"><a name="p54571315102714"></a><a name="p54571315102714"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p19457171522711"><a name="p19457171522711"></a><a name="p19457171522711"></a>√</p>
</td>
</tr>
<tr id="row1534541916274"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1434671952710"><a name="p1434671952710"></a><a name="p1434671952710"></a>查询告警通知配置</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1346519192712"><a name="p1346519192712"></a><a name="p1346519192712"></a>waf:alert:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p43461919112715"><a name="p43461919112715"></a><a name="p43461919112715"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1346161912714"><a name="p1346161912714"></a><a name="p1346161912714"></a>√</p>
</td>
</tr>
<tr id="row14497192414279"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p134979240275"><a name="p134979240275"></a><a name="p134979240275"></a>更新告警通知配置</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1949742472717"><a name="p1949742472717"></a><a name="p1949742472717"></a>waf:alert:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p7497102418272"><a name="p7497102418272"></a><a name="p7497102418272"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1049712420272"><a name="p1049712420272"></a><a name="p1049712420272"></a>√</p>
</td>
</tr>
<tr id="row1725625132913"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p10256175117291"><a name="p10256175117291"></a><a name="p10256175117291"></a>查询云日志配额</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p14256155114292"><a name="p14256155114292"></a><a name="p14256155114292"></a>waf:ltsConfig:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1925613516295"><a name="p1925613516295"></a><a name="p1925613516295"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p22562516297"><a name="p22562516297"></a><a name="p22562516297"></a>√</p>
</td>
</tr>
<tr id="row9191111412303"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1019181453017"><a name="p1019181453017"></a><a name="p1019181453017"></a>更新云日志配额</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p16191111473012"><a name="p16191111473012"></a><a name="p16191111473012"></a>waf:ltsConfig:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p101922143309"><a name="p101922143309"></a><a name="p101922143309"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1319219143306"><a name="p1319219143306"></a><a name="p1319219143306"></a>√</p>
</td>
</tr>
<tr id="row1735535616305"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p435516561304"><a name="p435516561304"></a><a name="p435516561304"></a>创建云模式包周期订单</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p193561567301"><a name="p193561567301"></a><a name="p193561567301"></a>waf:prepaid:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p13356105620306"><a name="p13356105620306"></a><a name="p13356105620306"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p73568568306"><a name="p73568568306"></a><a name="p73568568306"></a>√</p>
</td>
</tr>
<tr id="row114336376341"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p17434123753420"><a name="p17434123753420"></a><a name="p17434123753420"></a>查询独享引擎实例列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p174341237173412"><a name="p174341237173412"></a><a name="p174341237173412"></a>waf:premiumInstance:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p17434113753419"><a name="p17434113753419"></a><a name="p17434113753419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p54341737183410"><a name="p54341737183410"></a><a name="p54341737183410"></a>√</p>
</td>
</tr>
<tr id="row25574526358"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p655875219357"><a name="p655875219357"></a><a name="p655875219357"></a>查询独享引擎</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1155845211358"><a name="p1155845211358"></a><a name="p1155845211358"></a>waf:premiumInstance:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p7558125219355"><a name="p7558125219355"></a><a name="p7558125219355"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p6558175218352"><a name="p6558175218352"></a><a name="p6558175218352"></a>√</p>
</td>
</tr>
<tr id="row17886191873612"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p9886141817369"><a name="p9886141817369"></a><a name="p9886141817369"></a>创建独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1288641810369"><a name="p1288641810369"></a><a name="p1288641810369"></a>waf:premiumInstance:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p888614188368"><a name="p888614188368"></a><a name="p888614188368"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p98862018163614"><a name="p98862018163614"></a><a name="p98862018163614"></a>√</p>
</td>
</tr>
<tr id="row18911154163716"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p6891135413719"><a name="p6891135413719"></a><a name="p6891135413719"></a>删除独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p19891165416379"><a name="p19891165416379"></a><a name="p19891165416379"></a>waf:premiumInstance:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p38914544376"><a name="p38914544376"></a><a name="p38914544376"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p189185443713"><a name="p189185443713"></a><a name="p189185443713"></a>√</p>
</td>
</tr>
<tr id="row9315225382"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p131202293815"><a name="p131202293815"></a><a name="p131202293815"></a>更新独享引擎</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p7311722123816"><a name="p7311722123816"></a><a name="p7311722123816"></a>waf:premiumInstance:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p173117229382"><a name="p173117229382"></a><a name="p173117229382"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p83162233816"><a name="p83162233816"></a><a name="p83162233816"></a>√</p>
</td>
</tr>
<tr id="row7180503813"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p8678172031016"><a name="p8678172031016"></a><a name="p8678172031016"></a>查看WAF实例组详情</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1867812016104"><a name="p1867812016104"></a><a name="p1867812016104"></a>waf:pool:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p126801658201012"><a name="p126801658201012"></a><a name="p126801658201012"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p126806580100"><a name="p126806580100"></a><a name="p126806580100"></a>√</p>
</td>
</tr>
<tr id="row15685197193"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1467815201104"><a name="p1467815201104"></a><a name="p1467815201104"></a>修改WAF实例组配置</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p76782209104"><a name="p76782209104"></a><a name="p76782209104"></a>waf:pool:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p125989215114"><a name="p125989215114"></a><a name="p125989215114"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p14598621141118"><a name="p14598621141118"></a><a name="p14598621141118"></a>√</p>
</td>
</tr>
<tr id="row0741631498"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p26781120121018"><a name="p26781120121018"></a><a name="p26781120121018"></a>创建WAF实例组</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p17678112011101"><a name="p17678112011101"></a><a name="p17678112011101"></a>waf:pool:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p461313181118"><a name="p461313181118"></a><a name="p461313181118"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1561314311113"><a name="p1561314311113"></a><a name="p1561314311113"></a>√</p>
</td>
</tr>
<tr id="row06716013911"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p136799204109"><a name="p136799204109"></a><a name="p136799204109"></a>删除WAF实例组</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1567902013104"><a name="p1567902013104"></a><a name="p1567902013104"></a>waf:pool:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p36132313117"><a name="p36132313117"></a><a name="p36132313117"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p5613123113114"><a name="p5613123113114"></a><a name="p5613123113114"></a>√</p>
</td>
</tr>
<tr id="row0884205614819"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p5679152001014"><a name="p5679152001014"></a><a name="p5679152001014"></a>查看WAF实例组列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p967922014106"><a name="p967922014106"></a><a name="p967922014106"></a>waf:pool:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1461353181111"><a name="p1461353181111"></a><a name="p1461353181111"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p18614133110113"><a name="p18614133110113"></a><a name="p18614133110113"></a>√</p>
</td>
</tr>
<tr id="row148039538817"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p0679172014105"><a name="p0679172014105"></a><a name="p0679172014105"></a>查询WAF实例组绑定详情</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p1867918200108"><a name="p1867918200108"></a><a name="p1867918200108"></a>waf:poolBinding:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1614163112115"><a name="p1614163112115"></a><a name="p1614163112115"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1161413316118"><a name="p1161413316118"></a><a name="p1161413316118"></a>√</p>
</td>
</tr>
<tr id="row557716291193"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p156791920121013"><a name="p156791920121013"></a><a name="p156791920121013"></a>绑定WAF实例组</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p4679820161013"><a name="p4679820161013"></a><a name="p4679820161013"></a>waf:poolBinding:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p156141314118"><a name="p156141314118"></a><a name="p156141314118"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p146148316117"><a name="p146148316117"></a><a name="p146148316117"></a>√</p>
</td>
</tr>
<tr id="row25213319917"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p567912014107"><a name="p567912014107"></a><a name="p567912014107"></a>取消绑定WAF实例组</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p186796201108"><a name="p186796201108"></a><a name="p186796201108"></a>waf:poolBinding:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p8614113120119"><a name="p8614113120119"></a><a name="p8614113120119"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p20614531101119"><a name="p20614531101119"></a><a name="p20614531101119"></a>√</p>
</td>
</tr>
<tr id="row1110817375910"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p8680162061010"><a name="p8680162061010"></a><a name="p8680162061010"></a>查询WAF实例组绑定详情</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p17680020171013"><a name="p17680020171013"></a><a name="p17680020171013"></a>waf:poolBinding:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p16614531151114"><a name="p16614531151114"></a><a name="p16614531151114"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p206145317111"><a name="p206145317111"></a><a name="p206145317111"></a>√</p>
</td>
</tr>
<tr id="row489016391392"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p86801820161013"><a name="p86801820161013"></a><a name="p86801820161013"></a>查询WAF实例组健康检查配置</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p106801320141020"><a name="p106801320141020"></a><a name="p106801320141020"></a>waf:poolHealthMonitor:get</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p1761463181115"><a name="p1761463181115"></a><a name="p1761463181115"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p1861493111111"><a name="p1861493111111"></a><a name="p1861493111111"></a>√</p>
</td>
</tr>
<tr id="row12890204217912"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p168072071014"><a name="p168072071014"></a><a name="p168072071014"></a>修改WAF实例组健康检查配置</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p106800208106"><a name="p106800208106"></a><a name="p106800208106"></a>waf:poolHealthMonitor:put</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p6614231151120"><a name="p6614231151120"></a><a name="p6614231151120"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p9614103118118"><a name="p9614103118118"></a><a name="p9614103118118"></a>√</p>
</td>
</tr>
<tr id="row15809345893"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p106801120101019"><a name="p106801120101019"></a><a name="p106801120101019"></a>创建WAF实例组健康检查配置</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p19680122015106"><a name="p19680122015106"></a><a name="p19680122015106"></a>waf:poolHealthMonitor:create</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p79401443117"><a name="p79401443117"></a><a name="p79401443117"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p694017445118"><a name="p694017445118"></a><a name="p694017445118"></a>√</p>
</td>
</tr>
<tr id="row1260710481492"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p1668192016108"><a name="p1668192016108"></a><a name="p1668192016108"></a>删除WAF实例组健康检查配置</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p16681122011020"><a name="p16681122011020"></a><a name="p16681122011020"></a>waf:poolHealthMonitor:delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p053316466116"><a name="p053316466116"></a><a name="p053316466116"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p653318464116"><a name="p653318464116"></a><a name="p653318464116"></a>√</p>
</td>
</tr>
<tr id="row321316513914"><td class="cellrowborder" valign="top" width="24.76247624762476%" headers="mcps1.1.5.1.1 "><p id="p3681172015100"><a name="p3681172015100"></a><a name="p3681172015100"></a>查询WAF实例组健康检查配置列表</p>
</td>
<td class="cellrowborder" valign="top" width="33.803380338033804%" headers="mcps1.1.5.1.2 "><p id="p7681132081015"><a name="p7681132081015"></a><a name="p7681132081015"></a>waf:poolHealthMonitor:list</p>
</td>
<td class="cellrowborder" valign="top" width="24.18241824182418%" headers="mcps1.1.5.1.3 "><p id="p44394816112"><a name="p44394816112"></a><a name="p44394816112"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="17.25172517251725%" headers="mcps1.1.5.1.4 "><p id="p543548191120"><a name="p543548191120"></a><a name="p543548191120"></a>√</p>
</td>
</tr>
</tbody>
</table>

