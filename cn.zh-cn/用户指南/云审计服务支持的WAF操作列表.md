# 云审计服务支持的WAF操作列表<a name="waf_01_0059"></a>

云审计服务（Cloud Trace Service，CTS）记录了Web应用防火墙相关的操作事件，方便用户日后的查询、审计和回溯，具体请参见云审计服务用户指南。

云审计服务支持的WAF操作列表如[表1](#table5821116193525)所示。

>![](public_sys-resources/icon-notice.gif) **须知：** 
>目前以下区域支持云审计功能：
>-   华北-北京一
>-   华东-上海二
>-   华南-广州
>-   中国-香港
>-   亚太-曼谷
>-   亚太-新加坡
>-   非洲-约翰内斯堡
>-   拉美-圣地亚哥

**表 1**  云审计服务支持的WAF操作列表

<a name="table5821116193525"></a>
<table><thead align="left"><tr id="zh-cn_topic_0110861280_row117406265409"><th class="cellrowborder" valign="top" width="42.95429542954295%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0110861280_p187409267407"><a name="zh-cn_topic_0110861280_p187409267407"></a><a name="zh-cn_topic_0110861280_p187409267407"></a>操作名称</p>
</th>
<th class="cellrowborder" valign="top" width="27.062706270627064%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0110861280_p12740192644011"><a name="zh-cn_topic_0110861280_p12740192644011"></a><a name="zh-cn_topic_0110861280_p12740192644011"></a>资源类型</p>
</th>
<th class="cellrowborder" valign="top" width="29.982998299829983%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0110861280_p974092616405"><a name="zh-cn_topic_0110861280_p974092616405"></a><a name="zh-cn_topic_0110861280_p974092616405"></a>事件名称</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0110861280_row1874015262402"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p3740182617402"><a name="zh-cn_topic_0110861280_p3740182617402"></a><a name="zh-cn_topic_0110861280_p3740182617402"></a>创建Web应用防火墙防护实例</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1874062617408"><a name="zh-cn_topic_0110861280_p1874062617408"></a><a name="zh-cn_topic_0110861280_p1874062617408"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1374010260403"><a name="zh-cn_topic_0110861280_p1374010260403"></a><a name="zh-cn_topic_0110861280_p1374010260403"></a>createInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row37401269409"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p11741526164020"><a name="zh-cn_topic_0110861280_p11741526164020"></a><a name="zh-cn_topic_0110861280_p11741526164020"></a>删除Web应用防火墙防护实例</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p6741122654010"><a name="zh-cn_topic_0110861280_p6741122654010"></a><a name="zh-cn_topic_0110861280_p6741122654010"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p174142664010"><a name="zh-cn_topic_0110861280_p174142664010"></a><a name="zh-cn_topic_0110861280_p174142664010"></a>deleteInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row27417266401"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p13741112619409"><a name="zh-cn_topic_0110861280_p13741112619409"></a><a name="zh-cn_topic_0110861280_p13741112619409"></a>更新Web应用防火墙防护实例</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p2741102614011"><a name="zh-cn_topic_0110861280_p2741102614011"></a><a name="zh-cn_topic_0110861280_p2741102614011"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p0741726144019"><a name="zh-cn_topic_0110861280_p0741726144019"></a><a name="zh-cn_topic_0110861280_p0741726144019"></a>modifyInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row9741102613406"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p147410262409"><a name="zh-cn_topic_0110861280_p147410262409"></a><a name="zh-cn_topic_0110861280_p147410262409"></a>修改Web应用防火墙防护实例的防护状态</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p6741132694011"><a name="zh-cn_topic_0110861280_p6741132694011"></a><a name="zh-cn_topic_0110861280_p6741132694011"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p8741182617407"><a name="zh-cn_topic_0110861280_p8741182617407"></a><a name="zh-cn_topic_0110861280_p8741182617407"></a>modifyProtectStatus</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row10741526194013"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1574132694014"><a name="zh-cn_topic_0110861280_p1574132694014"></a><a name="zh-cn_topic_0110861280_p1574132694014"></a>修改Web应用防火墙防护实例的接入状态</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p5741122614409"><a name="zh-cn_topic_0110861280_p5741122614409"></a><a name="zh-cn_topic_0110861280_p5741122614409"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p12741132654010"><a name="zh-cn_topic_0110861280_p12741132654010"></a><a name="zh-cn_topic_0110861280_p12741132654010"></a>modifyAccessStatus</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row87411826184011"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1874122612404"><a name="zh-cn_topic_0110861280_p1874122612404"></a><a name="zh-cn_topic_0110861280_p1874122612404"></a>创建Web应用防火墙防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p127411326184014"><a name="zh-cn_topic_0110861280_p127411326184014"></a><a name="zh-cn_topic_0110861280_p127411326184014"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1474118265407"><a name="zh-cn_topic_0110861280_p1474118265407"></a><a name="zh-cn_topic_0110861280_p1474118265407"></a>createPolicy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1174119269405"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1674112617408"><a name="zh-cn_topic_0110861280_p1674112617408"></a><a name="zh-cn_topic_0110861280_p1674112617408"></a>应用Web应用防火墙防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p14741426154019"><a name="zh-cn_topic_0110861280_p14741426154019"></a><a name="zh-cn_topic_0110861280_p14741426154019"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p17741726194011"><a name="zh-cn_topic_0110861280_p17741726194011"></a><a name="zh-cn_topic_0110861280_p17741726194011"></a>applyToPolicy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row15741726184011"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p774152617405"><a name="zh-cn_topic_0110861280_p774152617405"></a><a name="zh-cn_topic_0110861280_p774152617405"></a>更新Web应用防火墙防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1274114266408"><a name="zh-cn_topic_0110861280_p1274114266408"></a><a name="zh-cn_topic_0110861280_p1274114266408"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p17741132674015"><a name="zh-cn_topic_0110861280_p17741132674015"></a><a name="zh-cn_topic_0110861280_p17741132674015"></a>modifyPolicy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row12741122616405"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p137421126174018"><a name="zh-cn_topic_0110861280_p137421126174018"></a><a name="zh-cn_topic_0110861280_p137421126174018"></a>删除Web应用防火墙防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p10742926154012"><a name="zh-cn_topic_0110861280_p10742926154012"></a><a name="zh-cn_topic_0110861280_p10742926154012"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p12742526194015"><a name="zh-cn_topic_0110861280_p12742526194015"></a><a name="zh-cn_topic_0110861280_p12742526194015"></a>deletePolicy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1974210266402"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p117421626184019"><a name="zh-cn_topic_0110861280_p117421626184019"></a><a name="zh-cn_topic_0110861280_p117421626184019"></a>修改告警通知设置</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p2742202604020"><a name="zh-cn_topic_0110861280_p2742202604020"></a><a name="zh-cn_topic_0110861280_p2742202604020"></a>alertNoticeConfig</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p874222664018"><a name="zh-cn_topic_0110861280_p874222664018"></a><a name="zh-cn_topic_0110861280_p874222664018"></a>modifyAlertNoticeConfig</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row474212269407"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p16742152614012"><a name="zh-cn_topic_0110861280_p16742152614012"></a><a name="zh-cn_topic_0110861280_p16742152614012"></a>添加证书</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1874242612400"><a name="zh-cn_topic_0110861280_p1874242612400"></a><a name="zh-cn_topic_0110861280_p1874242612400"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p97421826144016"><a name="zh-cn_topic_0110861280_p97421826144016"></a><a name="zh-cn_topic_0110861280_p97421826144016"></a>createCertificate</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row185431219164114"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p12543141954110"><a name="zh-cn_topic_0110861280_p12543141954110"></a><a name="zh-cn_topic_0110861280_p12543141954110"></a>修改证书名称</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p105431519134114"><a name="zh-cn_topic_0110861280_p105431519134114"></a><a name="zh-cn_topic_0110861280_p105431519134114"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1054381984111"><a name="zh-cn_topic_0110861280_p1054381984111"></a><a name="zh-cn_topic_0110861280_p1054381984111"></a>modifyCertificate</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row0742172610408"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p11742132615403"><a name="zh-cn_topic_0110861280_p11742132615403"></a><a name="zh-cn_topic_0110861280_p11742132615403"></a>删除证书</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1574232694011"><a name="zh-cn_topic_0110861280_p1574232694011"></a><a name="zh-cn_topic_0110861280_p1574232694011"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1174212613408"><a name="zh-cn_topic_0110861280_p1174212613408"></a><a name="zh-cn_topic_0110861280_p1174212613408"></a>deleteCertificate</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1874292613408"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p157421826104012"><a name="zh-cn_topic_0110861280_p157421826104012"></a><a name="zh-cn_topic_0110861280_p157421826104012"></a>创建CC规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p07423264407"><a name="zh-cn_topic_0110861280_p07423264407"></a><a name="zh-cn_topic_0110861280_p07423264407"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p4742926174013"><a name="zh-cn_topic_0110861280_p4742926174013"></a><a name="zh-cn_topic_0110861280_p4742926174013"></a>createCc</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row974272617409"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1674212610407"><a name="zh-cn_topic_0110861280_p1674212610407"></a><a name="zh-cn_topic_0110861280_p1674212610407"></a>修改CC规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p3742026204014"><a name="zh-cn_topic_0110861280_p3742026204014"></a><a name="zh-cn_topic_0110861280_p3742026204014"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1674272613405"><a name="zh-cn_topic_0110861280_p1674272613405"></a><a name="zh-cn_topic_0110861280_p1674272613405"></a>modifyCc</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row17742132615403"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p207421826194020"><a name="zh-cn_topic_0110861280_p207421826194020"></a><a name="zh-cn_topic_0110861280_p207421826194020"></a>删除CC规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1374222674016"><a name="zh-cn_topic_0110861280_p1374222674016"></a><a name="zh-cn_topic_0110861280_p1374222674016"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p074362611401"><a name="zh-cn_topic_0110861280_p074362611401"></a><a name="zh-cn_topic_0110861280_p074362611401"></a>deleteCc</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row4743162610403"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p874312614406"><a name="zh-cn_topic_0110861280_p874312614406"></a><a name="zh-cn_topic_0110861280_p874312614406"></a>创建精准防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p15743726184013"><a name="zh-cn_topic_0110861280_p15743726184013"></a><a name="zh-cn_topic_0110861280_p15743726184013"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p107431262407"><a name="zh-cn_topic_0110861280_p107431262407"></a><a name="zh-cn_topic_0110861280_p107431262407"></a>createCustom</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row20743726124019"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p11743102674013"><a name="zh-cn_topic_0110861280_p11743102674013"></a><a name="zh-cn_topic_0110861280_p11743102674013"></a>修改精准防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p4743182654010"><a name="zh-cn_topic_0110861280_p4743182654010"></a><a name="zh-cn_topic_0110861280_p4743182654010"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p57433267403"><a name="zh-cn_topic_0110861280_p57433267403"></a><a name="zh-cn_topic_0110861280_p57433267403"></a>modifyCustom</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1274352611403"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p474342616406"><a name="zh-cn_topic_0110861280_p474342616406"></a><a name="zh-cn_topic_0110861280_p474342616406"></a>删除精准防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p174372664013"><a name="zh-cn_topic_0110861280_p174372664013"></a><a name="zh-cn_topic_0110861280_p174372664013"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p5743102618404"><a name="zh-cn_topic_0110861280_p5743102618404"></a><a name="zh-cn_topic_0110861280_p5743102618404"></a>deleteCustom</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row19743926114013"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p16743192604017"><a name="zh-cn_topic_0110861280_p16743192604017"></a><a name="zh-cn_topic_0110861280_p16743192604017"></a>创建IP黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p17743126194013"><a name="zh-cn_topic_0110861280_p17743126194013"></a><a name="zh-cn_topic_0110861280_p17743126194013"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p117431226134018"><a name="zh-cn_topic_0110861280_p117431226134018"></a><a name="zh-cn_topic_0110861280_p117431226134018"></a>createWhiteblackip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row11743326104017"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p19743172618407"><a name="zh-cn_topic_0110861280_p19743172618407"></a><a name="zh-cn_topic_0110861280_p19743172618407"></a>修改IP黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1574382674019"><a name="zh-cn_topic_0110861280_p1574382674019"></a><a name="zh-cn_topic_0110861280_p1574382674019"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p874392694020"><a name="zh-cn_topic_0110861280_p874392694020"></a><a name="zh-cn_topic_0110861280_p874392694020"></a>modifyWhiteblackip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1774318262403"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1674372664017"><a name="zh-cn_topic_0110861280_p1674372664017"></a><a name="zh-cn_topic_0110861280_p1674372664017"></a>删除IP黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p15743202664017"><a name="zh-cn_topic_0110861280_p15743202664017"></a><a name="zh-cn_topic_0110861280_p15743202664017"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p10743426114010"><a name="zh-cn_topic_0110861280_p10743426114010"></a><a name="zh-cn_topic_0110861280_p10743426114010"></a>deleteWhiteblackip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1774332617403"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1874392684019"><a name="zh-cn_topic_0110861280_p1874392684019"></a><a name="zh-cn_topic_0110861280_p1874392684019"></a>创建网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p87437261407"><a name="zh-cn_topic_0110861280_p87437261407"></a><a name="zh-cn_topic_0110861280_p87437261407"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p474414267402"><a name="zh-cn_topic_0110861280_p474414267402"></a><a name="zh-cn_topic_0110861280_p474414267402"></a>createAntitamper</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row187446269406"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p157441326124012"><a name="zh-cn_topic_0110861280_p157441326124012"></a><a name="zh-cn_topic_0110861280_p157441326124012"></a>刷新网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p7744102664013"><a name="zh-cn_topic_0110861280_p7744102664013"></a><a name="zh-cn_topic_0110861280_p7744102664013"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p15744142664011"><a name="zh-cn_topic_0110861280_p15744142664011"></a><a name="zh-cn_topic_0110861280_p15744142664011"></a>refreshAntitamper</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1774402684016"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1974472674011"><a name="zh-cn_topic_0110861280_p1974472674011"></a><a name="zh-cn_topic_0110861280_p1974472674011"></a>删除网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1474422619404"><a name="zh-cn_topic_0110861280_p1474422619404"></a><a name="zh-cn_topic_0110861280_p1474422619404"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p474410263403"><a name="zh-cn_topic_0110861280_p474410263403"></a><a name="zh-cn_topic_0110861280_p474410263403"></a>deleteAntitamper</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row2744152612404"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p574442604010"><a name="zh-cn_topic_0110861280_p574442604010"></a><a name="zh-cn_topic_0110861280_p574442604010"></a>创建误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p47443260406"><a name="zh-cn_topic_0110861280_p47443260406"></a><a name="zh-cn_topic_0110861280_p47443260406"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p157440261404"><a name="zh-cn_topic_0110861280_p157440261404"></a><a name="zh-cn_topic_0110861280_p157440261404"></a>createIgnore</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1874412684012"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1374417267408"><a name="zh-cn_topic_0110861280_p1374417267408"></a><a name="zh-cn_topic_0110861280_p1374417267408"></a>删除误报屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p174472614405"><a name="zh-cn_topic_0110861280_p174472614405"></a><a name="zh-cn_topic_0110861280_p174472614405"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p18744726124019"><a name="zh-cn_topic_0110861280_p18744726124019"></a><a name="zh-cn_topic_0110861280_p18744726124019"></a>deleteIgnore</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row167441926194018"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p67442026174017"><a name="zh-cn_topic_0110861280_p67442026174017"></a><a name="zh-cn_topic_0110861280_p67442026174017"></a>创建隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p2074462616407"><a name="zh-cn_topic_0110861280_p2074462616407"></a><a name="zh-cn_topic_0110861280_p2074462616407"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p5744826124014"><a name="zh-cn_topic_0110861280_p5744826124014"></a><a name="zh-cn_topic_0110861280_p5744826124014"></a>createPrivacy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row074492617404"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p207441426164019"><a name="zh-cn_topic_0110861280_p207441426164019"></a><a name="zh-cn_topic_0110861280_p207441426164019"></a>修改隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p117441126104010"><a name="zh-cn_topic_0110861280_p117441126104010"></a><a name="zh-cn_topic_0110861280_p117441126104010"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p15744142634015"><a name="zh-cn_topic_0110861280_p15744142634015"></a><a name="zh-cn_topic_0110861280_p15744142634015"></a>modifyPrivacy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1974413267409"><td class="cellrowborder" valign="top" width="42.95429542954295%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1074452654011"><a name="zh-cn_topic_0110861280_p1074452654011"></a><a name="zh-cn_topic_0110861280_p1074452654011"></a>删除隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="27.062706270627064%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p3744726104010"><a name="zh-cn_topic_0110861280_p3744726104010"></a><a name="zh-cn_topic_0110861280_p3744726104010"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="29.982998299829983%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p16744122614010"><a name="zh-cn_topic_0110861280_p16744122614010"></a><a name="zh-cn_topic_0110861280_p16744122614010"></a>deletePrivacy</p>
</td>
</tr>
</tbody>
</table>

