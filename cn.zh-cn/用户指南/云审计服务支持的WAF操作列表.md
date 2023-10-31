# 云审计服务支持的WAF操作列表<a name="waf_01_0059"></a>

云审计服务（Cloud Trace Service，CTS）记录了Web应用防火墙相关的操作事件，方便用户日后的查询、审计和回溯，具体请参见云审计服务用户指南。

**表 1**  云审计服务支持的WAF操作列表

<a name="table16112422163510"></a>
<table><thead align="left"><tr id="zh-cn_topic_0110861280_row181831055132217"><th class="cellrowborder" valign="top" width="27.48274827482748%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0110861280_p157897716259"><a name="zh-cn_topic_0110861280_p157897716259"></a><a name="zh-cn_topic_0110861280_p157897716259"></a>操作名称</p>
</th>
<th class="cellrowborder" valign="top" width="32.97329732973297%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0110861280_p1418418555226"><a name="zh-cn_topic_0110861280_p1418418555226"></a><a name="zh-cn_topic_0110861280_p1418418555226"></a>资源类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.54395439543954%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0110861280_p11184195512227"><a name="zh-cn_topic_0110861280_p11184195512227"></a><a name="zh-cn_topic_0110861280_p11184195512227"></a>事件名称</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0110861280_row918414557224"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p13226830202719"><a name="zh-cn_topic_0110861280_p13226830202719"></a><a name="zh-cn_topic_0110861280_p13226830202719"></a>创建云模式域名</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p10226130152711"><a name="zh-cn_topic_0110861280_p10226130152711"></a><a name="zh-cn_topic_0110861280_p10226130152711"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p16226183002716"><a name="zh-cn_topic_0110861280_p16226183002716"></a><a name="zh-cn_topic_0110861280_p16226183002716"></a>createInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row818412559224"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1522653052716"><a name="zh-cn_topic_0110861280_p1522653052716"></a><a name="zh-cn_topic_0110861280_p1522653052716"></a>删除云模式域名</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p16226830112715"><a name="zh-cn_topic_0110861280_p16226830112715"></a><a name="zh-cn_topic_0110861280_p16226830112715"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1722619306276"><a name="zh-cn_topic_0110861280_p1722619306276"></a><a name="zh-cn_topic_0110861280_p1722619306276"></a>deleteInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row14184105592218"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p922615302274"><a name="zh-cn_topic_0110861280_p922615302274"></a><a name="zh-cn_topic_0110861280_p922615302274"></a>修改云模式域名的防护状态</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p13226203014275"><a name="zh-cn_topic_0110861280_p13226203014275"></a><a name="zh-cn_topic_0110861280_p13226203014275"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p20226203032710"><a name="zh-cn_topic_0110861280_p20226203032710"></a><a name="zh-cn_topic_0110861280_p20226203032710"></a>modifyProtectStatus</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row15184195515221"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p42261230142715"><a name="zh-cn_topic_0110861280_p42261230142715"></a><a name="zh-cn_topic_0110861280_p42261230142715"></a>修改云模式域名的接入状态</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p2226153012271"><a name="zh-cn_topic_0110861280_p2226153012271"></a><a name="zh-cn_topic_0110861280_p2226153012271"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p202261930172719"><a name="zh-cn_topic_0110861280_p202261930172719"></a><a name="zh-cn_topic_0110861280_p202261930172719"></a>modifyAccessStatus</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row218419555227"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p152261430202718"><a name="zh-cn_topic_0110861280_p152261430202718"></a><a name="zh-cn_topic_0110861280_p152261430202718"></a>修改云模式域名</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p123703062710"><a name="zh-cn_topic_0110861280_p123703062710"></a><a name="zh-cn_topic_0110861280_p123703062710"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p4237173011277"><a name="zh-cn_topic_0110861280_p4237173011277"></a><a name="zh-cn_topic_0110861280_p4237173011277"></a>modifyInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row191851655172216"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p162371230172710"><a name="zh-cn_topic_0110861280_p162371230172710"></a><a name="zh-cn_topic_0110861280_p162371230172710"></a>修改DNS解析，快速接入WAF</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p13237123042717"><a name="zh-cn_topic_0110861280_p13237123042717"></a><a name="zh-cn_topic_0110861280_p13237123042717"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1623716300271"><a name="zh-cn_topic_0110861280_p1623716300271"></a><a name="zh-cn_topic_0110861280_p1623716300271"></a>quickAccessInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row11185115542217"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p112371030152713"><a name="zh-cn_topic_0110861280_p112371030152713"></a><a name="zh-cn_topic_0110861280_p112371030152713"></a>服务器线路设置</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p723723014273"><a name="zh-cn_topic_0110861280_p723723014273"></a><a name="zh-cn_topic_0110861280_p723723014273"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p62371530122711"><a name="zh-cn_topic_0110861280_p62371530122711"></a><a name="zh-cn_topic_0110861280_p62371530122711"></a>modifyInstanceRoute</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1118595513220"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p723711306279"><a name="zh-cn_topic_0110861280_p723711306279"></a><a name="zh-cn_topic_0110861280_p723711306279"></a>创建域名（独享）</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p62371530102715"><a name="zh-cn_topic_0110861280_p62371530102715"></a><a name="zh-cn_topic_0110861280_p62371530102715"></a>host</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1237163072715"><a name="zh-cn_topic_0110861280_p1237163072715"></a><a name="zh-cn_topic_0110861280_p1237163072715"></a>createHost</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row4185555122217"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p19237163042712"><a name="zh-cn_topic_0110861280_p19237163042712"></a><a name="zh-cn_topic_0110861280_p19237163042712"></a>修改域名（独享）</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p5238193013272"><a name="zh-cn_topic_0110861280_p5238193013272"></a><a name="zh-cn_topic_0110861280_p5238193013272"></a>host</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p192388306276"><a name="zh-cn_topic_0110861280_p192388306276"></a><a name="zh-cn_topic_0110861280_p192388306276"></a>modifyHost</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row218535532210"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p19238123012711"><a name="zh-cn_topic_0110861280_p19238123012711"></a><a name="zh-cn_topic_0110861280_p19238123012711"></a>删除域名（独享）</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1323815306271"><a name="zh-cn_topic_0110861280_p1323815306271"></a><a name="zh-cn_topic_0110861280_p1323815306271"></a>host</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p123833016273"><a name="zh-cn_topic_0110861280_p123833016273"></a><a name="zh-cn_topic_0110861280_p123833016273"></a>deleteHost</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row6185135512221"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p123853013276"><a name="zh-cn_topic_0110861280_p123853013276"></a><a name="zh-cn_topic_0110861280_p123853013276"></a>修改防护状态（独享）</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p142381130102719"><a name="zh-cn_topic_0110861280_p142381130102719"></a><a name="zh-cn_topic_0110861280_p142381130102719"></a>host</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1823820300273"><a name="zh-cn_topic_0110861280_p1823820300273"></a><a name="zh-cn_topic_0110861280_p1823820300273"></a>modifyProtectStatus</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row191852554224"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p823823092711"><a name="zh-cn_topic_0110861280_p823823092711"></a><a name="zh-cn_topic_0110861280_p823823092711"></a>修改接入状态（独享）</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p18238143062718"><a name="zh-cn_topic_0110861280_p18238143062718"></a><a name="zh-cn_topic_0110861280_p18238143062718"></a>host</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1323823016271"><a name="zh-cn_topic_0110861280_p1323823016271"></a><a name="zh-cn_topic_0110861280_p1323823016271"></a>modifyAccessStatus</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1186105532213"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1523823012272"><a name="zh-cn_topic_0110861280_p1523823012272"></a><a name="zh-cn_topic_0110861280_p1523823012272"></a>修改接入配置（独享）</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p123843013274"><a name="zh-cn_topic_0110861280_p123843013274"></a><a name="zh-cn_topic_0110861280_p123843013274"></a>host</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1323810304277"><a name="zh-cn_topic_0110861280_p1323810304277"></a><a name="zh-cn_topic_0110861280_p1323810304277"></a>modifyAccessProgress</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row0579165442317"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p22391330182718"><a name="zh-cn_topic_0110861280_p22391330182718"></a><a name="zh-cn_topic_0110861280_p22391330182718"></a>域名迁移</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p023910305275"><a name="zh-cn_topic_0110861280_p023910305275"></a><a name="zh-cn_topic_0110861280_p023910305275"></a>migrate-host</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1823993014276"><a name="zh-cn_topic_0110861280_p1823993014276"></a><a name="zh-cn_topic_0110861280_p1823993014276"></a>migrateHosts</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row2579125413233"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p82396305272"><a name="zh-cn_topic_0110861280_p82396305272"></a><a name="zh-cn_topic_0110861280_p82396305272"></a>添加证书</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p924073014278"><a name="zh-cn_topic_0110861280_p924073014278"></a><a name="zh-cn_topic_0110861280_p924073014278"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p122401302274"><a name="zh-cn_topic_0110861280_p122401302274"></a><a name="zh-cn_topic_0110861280_p122401302274"></a>createCertificate</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row857911542232"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p424020301279"><a name="zh-cn_topic_0110861280_p424020301279"></a><a name="zh-cn_topic_0110861280_p424020301279"></a>修改证书</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p10240153012274"><a name="zh-cn_topic_0110861280_p10240153012274"></a><a name="zh-cn_topic_0110861280_p10240153012274"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p32404303275"><a name="zh-cn_topic_0110861280_p32404303275"></a><a name="zh-cn_topic_0110861280_p32404303275"></a>updateCertificate</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row4995155916237"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p024012303273"><a name="zh-cn_topic_0110861280_p024012303273"></a><a name="zh-cn_topic_0110861280_p024012303273"></a>删除证书</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p5240930182717"><a name="zh-cn_topic_0110861280_p5240930182717"></a><a name="zh-cn_topic_0110861280_p5240930182717"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p624013306275"><a name="zh-cn_topic_0110861280_p624013306275"></a><a name="zh-cn_topic_0110861280_p624013306275"></a>deleteCertificate</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1995259112312"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p17240830172716"><a name="zh-cn_topic_0110861280_p17240830172716"></a><a name="zh-cn_topic_0110861280_p17240830172716"></a>应用证书（将证书添加到域名）</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p32401830182717"><a name="zh-cn_topic_0110861280_p32401830182717"></a><a name="zh-cn_topic_0110861280_p32401830182717"></a>certificate</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p14240163010276"><a name="zh-cn_topic_0110861280_p14240163010276"></a><a name="zh-cn_topic_0110861280_p14240163010276"></a>applyCertificate</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row2099516590233"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p5241133016271"><a name="zh-cn_topic_0110861280_p5241133016271"></a><a name="zh-cn_topic_0110861280_p5241133016271"></a>共享证书</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1224163072719"><a name="zh-cn_topic_0110861280_p1224163072719"></a><a name="zh-cn_topic_0110861280_p1224163072719"></a>certificate-sharing</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p18241173002718"><a name="zh-cn_topic_0110861280_p18241173002718"></a><a name="zh-cn_topic_0110861280_p18241173002718"></a>createCertificateSharing</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row8995195915236"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p124163032713"><a name="zh-cn_topic_0110861280_p124163032713"></a><a name="zh-cn_topic_0110861280_p124163032713"></a>关闭证书共享</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p3241183052720"><a name="zh-cn_topic_0110861280_p3241183052720"></a><a name="zh-cn_topic_0110861280_p3241183052720"></a>certificate-sharing</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p8241183017271"><a name="zh-cn_topic_0110861280_p8241183017271"></a><a name="zh-cn_topic_0110861280_p8241183017271"></a>deleteCertificateSharing</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row79954592237"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p2241193022711"><a name="zh-cn_topic_0110861280_p2241193022711"></a><a name="zh-cn_topic_0110861280_p2241193022711"></a>创建Web应用防火墙防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p524113018271"><a name="zh-cn_topic_0110861280_p524113018271"></a><a name="zh-cn_topic_0110861280_p524113018271"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p72419307279"><a name="zh-cn_topic_0110861280_p72419307279"></a><a name="zh-cn_topic_0110861280_p72419307279"></a>createPolicy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1699514596230"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p3241193012715"><a name="zh-cn_topic_0110861280_p3241193012715"></a><a name="zh-cn_topic_0110861280_p3241193012715"></a>应用Web应用防火墙防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p182421430152714"><a name="zh-cn_topic_0110861280_p182421430152714"></a><a name="zh-cn_topic_0110861280_p182421430152714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p182422030112713"><a name="zh-cn_topic_0110861280_p182422030112713"></a><a name="zh-cn_topic_0110861280_p182422030112713"></a>applyToHost</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row20996359122316"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1324217305279"><a name="zh-cn_topic_0110861280_p1324217305279"></a><a name="zh-cn_topic_0110861280_p1324217305279"></a>更新Web应用防火墙防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p4242143011279"><a name="zh-cn_topic_0110861280_p4242143011279"></a><a name="zh-cn_topic_0110861280_p4242143011279"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p11242193015274"><a name="zh-cn_topic_0110861280_p11242193015274"></a><a name="zh-cn_topic_0110861280_p11242193015274"></a>modifyPolicy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row39961659192318"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p10242143016278"><a name="zh-cn_topic_0110861280_p10242143016278"></a><a name="zh-cn_topic_0110861280_p10242143016278"></a>删除Web应用防火墙防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p18242130152720"><a name="zh-cn_topic_0110861280_p18242130152720"></a><a name="zh-cn_topic_0110861280_p18242130152720"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1624215306274"><a name="zh-cn_topic_0110861280_p1624215306274"></a><a name="zh-cn_topic_0110861280_p1624215306274"></a>deletePolicy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row14996559162318"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p524233012270"><a name="zh-cn_topic_0110861280_p524233012270"></a><a name="zh-cn_topic_0110861280_p524233012270"></a>创建CC规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p13242730152713"><a name="zh-cn_topic_0110861280_p13242730152713"></a><a name="zh-cn_topic_0110861280_p13242730152713"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p15243183062714"><a name="zh-cn_topic_0110861280_p15243183062714"></a><a name="zh-cn_topic_0110861280_p15243183062714"></a>createCc</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row499615911235"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p182435301274"><a name="zh-cn_topic_0110861280_p182435301274"></a><a name="zh-cn_topic_0110861280_p182435301274"></a>修改CC规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1824383014279"><a name="zh-cn_topic_0110861280_p1824383014279"></a><a name="zh-cn_topic_0110861280_p1824383014279"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1224313015273"><a name="zh-cn_topic_0110861280_p1224313015273"></a><a name="zh-cn_topic_0110861280_p1224313015273"></a>modifyCc</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1699665952317"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p12431630172715"><a name="zh-cn_topic_0110861280_p12431630172715"></a><a name="zh-cn_topic_0110861280_p12431630172715"></a>删除CC规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p12431530192717"><a name="zh-cn_topic_0110861280_p12431530192717"></a><a name="zh-cn_topic_0110861280_p12431530192717"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p824363013277"><a name="zh-cn_topic_0110861280_p824363013277"></a><a name="zh-cn_topic_0110861280_p824363013277"></a>deleteCc</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row69969593237"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p2243103014278"><a name="zh-cn_topic_0110861280_p2243103014278"></a><a name="zh-cn_topic_0110861280_p2243103014278"></a>创建精准防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p0243430152717"><a name="zh-cn_topic_0110861280_p0243430152717"></a><a name="zh-cn_topic_0110861280_p0243430152717"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p62431630162710"><a name="zh-cn_topic_0110861280_p62431630162710"></a><a name="zh-cn_topic_0110861280_p62431630162710"></a>createCustom</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row89961859122317"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p624317308272"><a name="zh-cn_topic_0110861280_p624317308272"></a><a name="zh-cn_topic_0110861280_p624317308272"></a>修改精准防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p112431030132712"><a name="zh-cn_topic_0110861280_p112431030132712"></a><a name="zh-cn_topic_0110861280_p112431030132712"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p12243173052719"><a name="zh-cn_topic_0110861280_p12243173052719"></a><a name="zh-cn_topic_0110861280_p12243173052719"></a>modifyCustom</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1399635962312"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p19243173017277"><a name="zh-cn_topic_0110861280_p19243173017277"></a><a name="zh-cn_topic_0110861280_p19243173017277"></a>删除精准防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p424393042710"><a name="zh-cn_topic_0110861280_p424393042710"></a><a name="zh-cn_topic_0110861280_p424393042710"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p42436309277"><a name="zh-cn_topic_0110861280_p42436309277"></a><a name="zh-cn_topic_0110861280_p42436309277"></a>deleteCustom</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1799605916236"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p132441330152718"><a name="zh-cn_topic_0110861280_p132441330152718"></a><a name="zh-cn_topic_0110861280_p132441330152718"></a>创建IP黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p624418304274"><a name="zh-cn_topic_0110861280_p624418304274"></a><a name="zh-cn_topic_0110861280_p624418304274"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p182441530102710"><a name="zh-cn_topic_0110861280_p182441530102710"></a><a name="zh-cn_topic_0110861280_p182441530102710"></a>createWhiteblackip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1157915418236"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1224473032720"><a name="zh-cn_topic_0110861280_p1224473032720"></a><a name="zh-cn_topic_0110861280_p1224473032720"></a>修改IP黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p7244230172719"><a name="zh-cn_topic_0110861280_p7244230172719"></a><a name="zh-cn_topic_0110861280_p7244230172719"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p9244103082713"><a name="zh-cn_topic_0110861280_p9244103082713"></a><a name="zh-cn_topic_0110861280_p9244103082713"></a>modifyWhiteblackip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row205941810246"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p13244130102714"><a name="zh-cn_topic_0110861280_p13244130102714"></a><a name="zh-cn_topic_0110861280_p13244130102714"></a>删除IP黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p4244103092714"><a name="zh-cn_topic_0110861280_p4244103092714"></a><a name="zh-cn_topic_0110861280_p4244103092714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p172446300271"><a name="zh-cn_topic_0110861280_p172446300271"></a><a name="zh-cn_topic_0110861280_p172446300271"></a>deleteWhiteblackip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row55944812240"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p16245230142710"><a name="zh-cn_topic_0110861280_p16245230142710"></a><a name="zh-cn_topic_0110861280_p16245230142710"></a>创建/刷新网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1524573052713"><a name="zh-cn_topic_0110861280_p1524573052713"></a><a name="zh-cn_topic_0110861280_p1524573052713"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p324533032711"><a name="zh-cn_topic_0110861280_p324533032711"></a><a name="zh-cn_topic_0110861280_p324533032711"></a>createAntitamper</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1059498192417"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p324563022720"><a name="zh-cn_topic_0110861280_p324563022720"></a><a name="zh-cn_topic_0110861280_p324563022720"></a>开启/关闭网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p024523022716"><a name="zh-cn_topic_0110861280_p024523022716"></a><a name="zh-cn_topic_0110861280_p024523022716"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p4245193015272"><a name="zh-cn_topic_0110861280_p4245193015272"></a><a name="zh-cn_topic_0110861280_p4245193015272"></a>modifyAntitamper</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row659419842411"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p424573082714"><a name="zh-cn_topic_0110861280_p424573082714"></a><a name="zh-cn_topic_0110861280_p424573082714"></a>删除网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p324543072720"><a name="zh-cn_topic_0110861280_p324543072720"></a><a name="zh-cn_topic_0110861280_p324543072720"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p124516308276"><a name="zh-cn_topic_0110861280_p124516308276"></a><a name="zh-cn_topic_0110861280_p124516308276"></a>deleteAntitamper</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row12595181248"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p524573014270"><a name="zh-cn_topic_0110861280_p524573014270"></a><a name="zh-cn_topic_0110861280_p524573014270"></a>创建全局白名单（原误报屏蔽）规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1224512302274"><a name="zh-cn_topic_0110861280_p1224512302274"></a><a name="zh-cn_topic_0110861280_p1224512302274"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1124510304272"><a name="zh-cn_topic_0110861280_p1124510304272"></a><a name="zh-cn_topic_0110861280_p1124510304272"></a>createIgnore</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row859538142416"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p2024543082716"><a name="zh-cn_topic_0110861280_p2024543082716"></a><a name="zh-cn_topic_0110861280_p2024543082716"></a>修改全局白名单（原误报屏蔽）规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p192469302271"><a name="zh-cn_topic_0110861280_p192469302271"></a><a name="zh-cn_topic_0110861280_p192469302271"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p9246730102718"><a name="zh-cn_topic_0110861280_p9246730102718"></a><a name="zh-cn_topic_0110861280_p9246730102718"></a>modifyIgnore</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1959510812244"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p14246103042713"><a name="zh-cn_topic_0110861280_p14246103042713"></a><a name="zh-cn_topic_0110861280_p14246103042713"></a>删除全局白名单（原误报屏蔽）规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p12460301277"><a name="zh-cn_topic_0110861280_p12460301277"></a><a name="zh-cn_topic_0110861280_p12460301277"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p12474305277"><a name="zh-cn_topic_0110861280_p12474305277"></a><a name="zh-cn_topic_0110861280_p12474305277"></a>deleteIgnore</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row959578132417"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p124719305272"><a name="zh-cn_topic_0110861280_p124719305272"></a><a name="zh-cn_topic_0110861280_p124719305272"></a>创建隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p12247030202712"><a name="zh-cn_topic_0110861280_p12247030202712"></a><a name="zh-cn_topic_0110861280_p12247030202712"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p5247530102718"><a name="zh-cn_topic_0110861280_p5247530102718"></a><a name="zh-cn_topic_0110861280_p5247530102718"></a>createPrivacy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row105952087246"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1724753018278"><a name="zh-cn_topic_0110861280_p1724753018278"></a><a name="zh-cn_topic_0110861280_p1724753018278"></a>修改隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p72479309274"><a name="zh-cn_topic_0110861280_p72479309274"></a><a name="zh-cn_topic_0110861280_p72479309274"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p7247193002715"><a name="zh-cn_topic_0110861280_p7247193002715"></a><a name="zh-cn_topic_0110861280_p7247193002715"></a>modifyPrivacy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row14595178172410"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p102479306278"><a name="zh-cn_topic_0110861280_p102479306278"></a><a name="zh-cn_topic_0110861280_p102479306278"></a>删除隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p122473305275"><a name="zh-cn_topic_0110861280_p122473305275"></a><a name="zh-cn_topic_0110861280_p122473305275"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p10247183002714"><a name="zh-cn_topic_0110861280_p10247183002714"></a><a name="zh-cn_topic_0110861280_p10247183002714"></a>deletePrivacy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1159519872419"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p82481130172715"><a name="zh-cn_topic_0110861280_p82481130172715"></a><a name="zh-cn_topic_0110861280_p82481130172715"></a>创建攻击惩罚规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p14248230182716"><a name="zh-cn_topic_0110861280_p14248230182716"></a><a name="zh-cn_topic_0110861280_p14248230182716"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1024883016273"><a name="zh-cn_topic_0110861280_p1024883016273"></a><a name="zh-cn_topic_0110861280_p1024883016273"></a>createPunishment</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1959618132415"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p22484306272"><a name="zh-cn_topic_0110861280_p22484306272"></a><a name="zh-cn_topic_0110861280_p22484306272"></a>修改攻击惩罚规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p17248103092716"><a name="zh-cn_topic_0110861280_p17248103092716"></a><a name="zh-cn_topic_0110861280_p17248103092716"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p19248123010273"><a name="zh-cn_topic_0110861280_p19248123010273"></a><a name="zh-cn_topic_0110861280_p19248123010273"></a>modifyPunishment</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row12596285241"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1624833018274"><a name="zh-cn_topic_0110861280_p1624833018274"></a><a name="zh-cn_topic_0110861280_p1624833018274"></a>删除攻击惩罚规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p5248730102714"><a name="zh-cn_topic_0110861280_p5248730102714"></a><a name="zh-cn_topic_0110861280_p5248730102714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p5248153012271"><a name="zh-cn_topic_0110861280_p5248153012271"></a><a name="zh-cn_topic_0110861280_p5248153012271"></a>deletePunishment</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1259612892410"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p12248830122716"><a name="zh-cn_topic_0110861280_p12248830122716"></a><a name="zh-cn_topic_0110861280_p12248830122716"></a>创建地理位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p15248103013275"><a name="zh-cn_topic_0110861280_p15248103013275"></a><a name="zh-cn_topic_0110861280_p15248103013275"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1124803012710"><a name="zh-cn_topic_0110861280_p1124803012710"></a><a name="zh-cn_topic_0110861280_p1124803012710"></a>createGeoip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row17596987249"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p02481830162712"><a name="zh-cn_topic_0110861280_p02481830162712"></a><a name="zh-cn_topic_0110861280_p02481830162712"></a>修改地理位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p924883015278"><a name="zh-cn_topic_0110861280_p924883015278"></a><a name="zh-cn_topic_0110861280_p924883015278"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p10248123012718"><a name="zh-cn_topic_0110861280_p10248123012718"></a><a name="zh-cn_topic_0110861280_p10248123012718"></a>modifyGeoip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row3596386243"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p224918305271"><a name="zh-cn_topic_0110861280_p224918305271"></a><a name="zh-cn_topic_0110861280_p224918305271"></a>删除地理位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p62491030112719"><a name="zh-cn_topic_0110861280_p62491030112719"></a><a name="zh-cn_topic_0110861280_p62491030112719"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p224923092716"><a name="zh-cn_topic_0110861280_p224923092716"></a><a name="zh-cn_topic_0110861280_p224923092716"></a>deleteGeoip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row185961180248"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1524914309275"><a name="zh-cn_topic_0110861280_p1524914309275"></a><a name="zh-cn_topic_0110861280_p1524914309275"></a>创建威胁情报访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p42491630122714"><a name="zh-cn_topic_0110861280_p42491630122714"></a><a name="zh-cn_topic_0110861280_p42491630122714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p92491430132711"><a name="zh-cn_topic_0110861280_p92491430132711"></a><a name="zh-cn_topic_0110861280_p92491430132711"></a>createIp-reputation</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1259611820249"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1024919306275"><a name="zh-cn_topic_0110861280_p1024919306275"></a><a name="zh-cn_topic_0110861280_p1024919306275"></a>修改威胁情报访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p124993092716"><a name="zh-cn_topic_0110861280_p124993092716"></a><a name="zh-cn_topic_0110861280_p124993092716"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p12249630152714"><a name="zh-cn_topic_0110861280_p12249630152714"></a><a name="zh-cn_topic_0110861280_p12249630152714"></a>modifyIp-reputation</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row25961089249"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1524916306273"><a name="zh-cn_topic_0110861280_p1524916306273"></a><a name="zh-cn_topic_0110861280_p1524916306273"></a>删除威胁情报访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p18249930112717"><a name="zh-cn_topic_0110861280_p18249930112717"></a><a name="zh-cn_topic_0110861280_p18249930112717"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p52491730142720"><a name="zh-cn_topic_0110861280_p52491730142720"></a><a name="zh-cn_topic_0110861280_p52491730142720"></a>deleteIp-reputation</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row65961813241"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p14249930162720"><a name="zh-cn_topic_0110861280_p14249930162720"></a><a name="zh-cn_topic_0110861280_p14249930162720"></a>创建反爬虫规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1924912309278"><a name="zh-cn_topic_0110861280_p1924912309278"></a><a name="zh-cn_topic_0110861280_p1924912309278"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p2024973042715"><a name="zh-cn_topic_0110861280_p2024973042715"></a><a name="zh-cn_topic_0110861280_p2024973042715"></a>createAnticrawler</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row175971681245"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p15250730182715"><a name="zh-cn_topic_0110861280_p15250730182715"></a><a name="zh-cn_topic_0110861280_p15250730182715"></a>修改反爬虫规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p825083015279"><a name="zh-cn_topic_0110861280_p825083015279"></a><a name="zh-cn_topic_0110861280_p825083015279"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p15250183082710"><a name="zh-cn_topic_0110861280_p15250183082710"></a><a name="zh-cn_topic_0110861280_p15250183082710"></a>modifyAnticrawler</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row165979818243"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p19250130182711"><a name="zh-cn_topic_0110861280_p19250130182711"></a><a name="zh-cn_topic_0110861280_p19250130182711"></a>删除反爬虫规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1825053016277"><a name="zh-cn_topic_0110861280_p1825053016277"></a><a name="zh-cn_topic_0110861280_p1825053016277"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p14250103018279"><a name="zh-cn_topic_0110861280_p14250103018279"></a><a name="zh-cn_topic_0110861280_p14250103018279"></a>deleteAnticrawler</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row95971818246"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p10250183072716"><a name="zh-cn_topic_0110861280_p10250183072716"></a><a name="zh-cn_topic_0110861280_p10250183072716"></a>创建防敏感信息泄露规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1925053032714"><a name="zh-cn_topic_0110861280_p1925053032714"></a><a name="zh-cn_topic_0110861280_p1925053032714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p125053015278"><a name="zh-cn_topic_0110861280_p125053015278"></a><a name="zh-cn_topic_0110861280_p125053015278"></a>createAntileakage</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row4597581248"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p16250183092710"><a name="zh-cn_topic_0110861280_p16250183092710"></a><a name="zh-cn_topic_0110861280_p16250183092710"></a>修改防敏感信息泄露规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p18250153042714"><a name="zh-cn_topic_0110861280_p18250153042714"></a><a name="zh-cn_topic_0110861280_p18250153042714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1325193018273"><a name="zh-cn_topic_0110861280_p1325193018273"></a><a name="zh-cn_topic_0110861280_p1325193018273"></a>modifyAntileakage</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row19597178122412"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p11251230182711"><a name="zh-cn_topic_0110861280_p11251230182711"></a><a name="zh-cn_topic_0110861280_p11251230182711"></a>删除防敏感信息泄露规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p162516301274"><a name="zh-cn_topic_0110861280_p162516301274"></a><a name="zh-cn_topic_0110861280_p162516301274"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1251430132711"><a name="zh-cn_topic_0110861280_p1251430132711"></a><a name="zh-cn_topic_0110861280_p1251430132711"></a>deleteAntileakage</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row13597178162413"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p125123032712"><a name="zh-cn_topic_0110861280_p125123032712"></a><a name="zh-cn_topic_0110861280_p125123032712"></a>批量创建CC规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p02512308274"><a name="zh-cn_topic_0110861280_p02512308274"></a><a name="zh-cn_topic_0110861280_p02512308274"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1425193042715"><a name="zh-cn_topic_0110861280_p1425193042715"></a><a name="zh-cn_topic_0110861280_p1425193042715"></a>batchCreateCc</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row17597389244"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1525113017273"><a name="zh-cn_topic_0110861280_p1525113017273"></a><a name="zh-cn_topic_0110861280_p1525113017273"></a>批量修改CC规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p72511330162714"><a name="zh-cn_topic_0110861280_p72511330162714"></a><a name="zh-cn_topic_0110861280_p72511330162714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1325163011273"><a name="zh-cn_topic_0110861280_p1325163011273"></a><a name="zh-cn_topic_0110861280_p1325163011273"></a>batchUpdateCc</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row12579125402315"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p725183062718"><a name="zh-cn_topic_0110861280_p725183062718"></a><a name="zh-cn_topic_0110861280_p725183062718"></a>批量删除CC规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p9251123017273"><a name="zh-cn_topic_0110861280_p9251123017273"></a><a name="zh-cn_topic_0110861280_p9251123017273"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p125115304271"><a name="zh-cn_topic_0110861280_p125115304271"></a><a name="zh-cn_topic_0110861280_p125115304271"></a>batchDeleteCc</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row155809547236"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p125118306279"><a name="zh-cn_topic_0110861280_p125118306279"></a><a name="zh-cn_topic_0110861280_p125118306279"></a>批量创建精准防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p52511330122719"><a name="zh-cn_topic_0110861280_p52511330122719"></a><a name="zh-cn_topic_0110861280_p52511330122719"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p3251113013276"><a name="zh-cn_topic_0110861280_p3251113013276"></a><a name="zh-cn_topic_0110861280_p3251113013276"></a>batchCreateCustom</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row165801054112316"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p425223014274"><a name="zh-cn_topic_0110861280_p425223014274"></a><a name="zh-cn_topic_0110861280_p425223014274"></a>批量修改精准防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1252183092713"><a name="zh-cn_topic_0110861280_p1252183092713"></a><a name="zh-cn_topic_0110861280_p1252183092713"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p725273062710"><a name="zh-cn_topic_0110861280_p725273062710"></a><a name="zh-cn_topic_0110861280_p725273062710"></a>batchUpdateCustom</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1758025432316"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p725218307274"><a name="zh-cn_topic_0110861280_p725218307274"></a><a name="zh-cn_topic_0110861280_p725218307274"></a>批量删除精准防护规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p102521330162711"><a name="zh-cn_topic_0110861280_p102521330162711"></a><a name="zh-cn_topic_0110861280_p102521330162711"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p52522302278"><a name="zh-cn_topic_0110861280_p52522302278"></a><a name="zh-cn_topic_0110861280_p52522302278"></a>batchDeleteCustom</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row12580454132320"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p425216309270"><a name="zh-cn_topic_0110861280_p425216309270"></a><a name="zh-cn_topic_0110861280_p425216309270"></a>批量创建IP黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p22521130102710"><a name="zh-cn_topic_0110861280_p22521130102710"></a><a name="zh-cn_topic_0110861280_p22521130102710"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p9252143012716"><a name="zh-cn_topic_0110861280_p9252143012716"></a><a name="zh-cn_topic_0110861280_p9252143012716"></a>batchCreateWhiteblackip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1458075452313"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p925353082711"><a name="zh-cn_topic_0110861280_p925353082711"></a><a name="zh-cn_topic_0110861280_p925353082711"></a>批量修改IP黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p7253203011278"><a name="zh-cn_topic_0110861280_p7253203011278"></a><a name="zh-cn_topic_0110861280_p7253203011278"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1125373019275"><a name="zh-cn_topic_0110861280_p1125373019275"></a><a name="zh-cn_topic_0110861280_p1125373019275"></a>batchUpdateWhiteblackip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row10580175452316"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1225373012271"><a name="zh-cn_topic_0110861280_p1225373012271"></a><a name="zh-cn_topic_0110861280_p1225373012271"></a>批量删除IP黑白名单规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p192533302279"><a name="zh-cn_topic_0110861280_p192533302279"></a><a name="zh-cn_topic_0110861280_p192533302279"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p625323062712"><a name="zh-cn_topic_0110861280_p625323062712"></a><a name="zh-cn_topic_0110861280_p625323062712"></a>batchDeleteWhiteblackip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1858017541233"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p42539309270"><a name="zh-cn_topic_0110861280_p42539309270"></a><a name="zh-cn_topic_0110861280_p42539309270"></a>批量创建地理位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p3253530112711"><a name="zh-cn_topic_0110861280_p3253530112711"></a><a name="zh-cn_topic_0110861280_p3253530112711"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p132537306274"><a name="zh-cn_topic_0110861280_p132537306274"></a><a name="zh-cn_topic_0110861280_p132537306274"></a>batchCreateGeoip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row10186755192210"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1925343012711"><a name="zh-cn_topic_0110861280_p1925343012711"></a><a name="zh-cn_topic_0110861280_p1925343012711"></a>批量修改地理位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p6253163017270"><a name="zh-cn_topic_0110861280_p6253163017270"></a><a name="zh-cn_topic_0110861280_p6253163017270"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p9253103017279"><a name="zh-cn_topic_0110861280_p9253103017279"></a><a name="zh-cn_topic_0110861280_p9253103017279"></a>batchUpdateGeoip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row11868552221"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p122537308276"><a name="zh-cn_topic_0110861280_p122537308276"></a><a name="zh-cn_topic_0110861280_p122537308276"></a>批量删除地理位置访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p82531330162714"><a name="zh-cn_topic_0110861280_p82531330162714"></a><a name="zh-cn_topic_0110861280_p82531330162714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p525433010275"><a name="zh-cn_topic_0110861280_p525433010275"></a><a name="zh-cn_topic_0110861280_p525433010275"></a>batchDeleteGeoip</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row7186195515221"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1254173012719"><a name="zh-cn_topic_0110861280_p1254173012719"></a><a name="zh-cn_topic_0110861280_p1254173012719"></a>批量创建威胁情报访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p22541130172718"><a name="zh-cn_topic_0110861280_p22541130172718"></a><a name="zh-cn_topic_0110861280_p22541130172718"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p825453082714"><a name="zh-cn_topic_0110861280_p825453082714"></a><a name="zh-cn_topic_0110861280_p825453082714"></a>batchCreateIp-reputation</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row31867558229"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1925493019270"><a name="zh-cn_topic_0110861280_p1925493019270"></a><a name="zh-cn_topic_0110861280_p1925493019270"></a>批量修改威胁情报访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p11260113015276"><a name="zh-cn_topic_0110861280_p11260113015276"></a><a name="zh-cn_topic_0110861280_p11260113015276"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p92601530162713"><a name="zh-cn_topic_0110861280_p92601530162713"></a><a name="zh-cn_topic_0110861280_p92601530162713"></a>batchUpdateIp-reputation</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1318685562211"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p10262153042719"><a name="zh-cn_topic_0110861280_p10262153042719"></a><a name="zh-cn_topic_0110861280_p10262153042719"></a>批量删除威胁情报访问控制规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p5263163014274"><a name="zh-cn_topic_0110861280_p5263163014274"></a><a name="zh-cn_topic_0110861280_p5263163014274"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1926313012716"><a name="zh-cn_topic_0110861280_p1926313012716"></a><a name="zh-cn_topic_0110861280_p1926313012716"></a>batchDeleteIp-reputation</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row17186175519220"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p926383092711"><a name="zh-cn_topic_0110861280_p926383092711"></a><a name="zh-cn_topic_0110861280_p926383092711"></a>批量创建/刷新网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p326316302276"><a name="zh-cn_topic_0110861280_p326316302276"></a><a name="zh-cn_topic_0110861280_p326316302276"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p2263153042712"><a name="zh-cn_topic_0110861280_p2263153042712"></a><a name="zh-cn_topic_0110861280_p2263153042712"></a>batchCreateAntitamper</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row138221133152320"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p62631430142710"><a name="zh-cn_topic_0110861280_p62631430142710"></a><a name="zh-cn_topic_0110861280_p62631430142710"></a>批量开启/关闭网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p20263030142718"><a name="zh-cn_topic_0110861280_p20263030142718"></a><a name="zh-cn_topic_0110861280_p20263030142718"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p5264143032713"><a name="zh-cn_topic_0110861280_p5264143032713"></a><a name="zh-cn_topic_0110861280_p5264143032713"></a>batchUpdateAntitamper</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row78222330232"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p112647305272"><a name="zh-cn_topic_0110861280_p112647305272"></a><a name="zh-cn_topic_0110861280_p112647305272"></a>批量删除网页防篡改规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p12641230152714"><a name="zh-cn_topic_0110861280_p12641230152714"></a><a name="zh-cn_topic_0110861280_p12641230152714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p15264143092714"><a name="zh-cn_topic_0110861280_p15264143092714"></a><a name="zh-cn_topic_0110861280_p15264143092714"></a>batchDeleteAntitamper</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row6822433202319"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p19264030142712"><a name="zh-cn_topic_0110861280_p19264030142712"></a><a name="zh-cn_topic_0110861280_p19264030142712"></a>批量创建防敏感信息泄露规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p162642030142713"><a name="zh-cn_topic_0110861280_p162642030142713"></a><a name="zh-cn_topic_0110861280_p162642030142713"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1926419302272"><a name="zh-cn_topic_0110861280_p1926419302272"></a><a name="zh-cn_topic_0110861280_p1926419302272"></a>batchCreateAntileakage</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1482293317233"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1326413020275"><a name="zh-cn_topic_0110861280_p1326413020275"></a><a name="zh-cn_topic_0110861280_p1326413020275"></a>批量修改防敏感信息泄露规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p2264133019272"><a name="zh-cn_topic_0110861280_p2264133019272"></a><a name="zh-cn_topic_0110861280_p2264133019272"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1265830172717"><a name="zh-cn_topic_0110861280_p1265830172717"></a><a name="zh-cn_topic_0110861280_p1265830172717"></a>batchUpdateAntileakage</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row148231933152317"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1526563014275"><a name="zh-cn_topic_0110861280_p1526563014275"></a><a name="zh-cn_topic_0110861280_p1526563014275"></a>批量删除防敏感信息泄露规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1626593019275"><a name="zh-cn_topic_0110861280_p1626593019275"></a><a name="zh-cn_topic_0110861280_p1626593019275"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1526533013276"><a name="zh-cn_topic_0110861280_p1526533013276"></a><a name="zh-cn_topic_0110861280_p1526533013276"></a>batchDeleteAntileakage</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row17823173313237"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p14265163014276"><a name="zh-cn_topic_0110861280_p14265163014276"></a><a name="zh-cn_topic_0110861280_p14265163014276"></a>批量创建全局白名单（原误报屏蔽）规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p172651030172711"><a name="zh-cn_topic_0110861280_p172651030172711"></a><a name="zh-cn_topic_0110861280_p172651030172711"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p92651330172711"><a name="zh-cn_topic_0110861280_p92651330172711"></a><a name="zh-cn_topic_0110861280_p92651330172711"></a>batchCreateIgnore</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row7824113316234"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p16265630132712"><a name="zh-cn_topic_0110861280_p16265630132712"></a><a name="zh-cn_topic_0110861280_p16265630132712"></a>批量修改全局白名单（原误报屏蔽）</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1026513012710"><a name="zh-cn_topic_0110861280_p1026513012710"></a><a name="zh-cn_topic_0110861280_p1026513012710"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p202661330152714"><a name="zh-cn_topic_0110861280_p202661330152714"></a><a name="zh-cn_topic_0110861280_p202661330152714"></a>batchUpdateIgnore</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row10825143332311"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p42661330112719"><a name="zh-cn_topic_0110861280_p42661330112719"></a><a name="zh-cn_topic_0110861280_p42661330112719"></a>批量删除全局白名单（原误报屏蔽）</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p726683062720"><a name="zh-cn_topic_0110861280_p726683062720"></a><a name="zh-cn_topic_0110861280_p726683062720"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p142661130112719"><a name="zh-cn_topic_0110861280_p142661130112719"></a><a name="zh-cn_topic_0110861280_p142661130112719"></a>batchDeleteIgnore</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row20825933182314"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p9266123014277"><a name="zh-cn_topic_0110861280_p9266123014277"></a><a name="zh-cn_topic_0110861280_p9266123014277"></a>批量创建隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p2267183016272"><a name="zh-cn_topic_0110861280_p2267183016272"></a><a name="zh-cn_topic_0110861280_p2267183016272"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p15267430142717"><a name="zh-cn_topic_0110861280_p15267430142717"></a><a name="zh-cn_topic_0110861280_p15267430142717"></a>batchCreatePrivacy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row118269333239"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1426753010278"><a name="zh-cn_topic_0110861280_p1426753010278"></a><a name="zh-cn_topic_0110861280_p1426753010278"></a>批量修改隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1326723013270"><a name="zh-cn_topic_0110861280_p1326723013270"></a><a name="zh-cn_topic_0110861280_p1326723013270"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p0267143011279"><a name="zh-cn_topic_0110861280_p0267143011279"></a><a name="zh-cn_topic_0110861280_p0267143011279"></a>batchUpdatePrivacy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1082614334239"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p10267143016272"><a name="zh-cn_topic_0110861280_p10267143016272"></a><a name="zh-cn_topic_0110861280_p10267143016272"></a>批量删除隐私屏蔽规则</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1126793052714"><a name="zh-cn_topic_0110861280_p1126793052714"></a><a name="zh-cn_topic_0110861280_p1126793052714"></a>policy</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1926793014278"><a name="zh-cn_topic_0110861280_p1926793014278"></a><a name="zh-cn_topic_0110861280_p1926793014278"></a>batchDeletePrivacy</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row20826113332315"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p5268430122716"><a name="zh-cn_topic_0110861280_p5268430122716"></a><a name="zh-cn_topic_0110861280_p5268430122716"></a>创建告警通知</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p82682305279"><a name="zh-cn_topic_0110861280_p82682305279"></a><a name="zh-cn_topic_0110861280_p82682305279"></a>alertNoticeConfig</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p6268330112715"><a name="zh-cn_topic_0110861280_p6268330112715"></a><a name="zh-cn_topic_0110861280_p6268330112715"></a>createAlertNoticeConfig</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row682683312233"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p92682030142719"><a name="zh-cn_topic_0110861280_p92682030142719"></a><a name="zh-cn_topic_0110861280_p92682030142719"></a>修改告警通知</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p16268730142711"><a name="zh-cn_topic_0110861280_p16268730142711"></a><a name="zh-cn_topic_0110861280_p16268730142711"></a>alertNoticeConfig</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p026823032717"><a name="zh-cn_topic_0110861280_p026823032717"></a><a name="zh-cn_topic_0110861280_p026823032717"></a>modifyAlertNoticeConfig</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1482713362319"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p32681030122711"><a name="zh-cn_topic_0110861280_p32681030122711"></a><a name="zh-cn_topic_0110861280_p32681030122711"></a>删除告警通知</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p826813092717"><a name="zh-cn_topic_0110861280_p826813092717"></a><a name="zh-cn_topic_0110861280_p826813092717"></a>alertNoticeConfig</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p42682030142713"><a name="zh-cn_topic_0110861280_p42682030142713"></a><a name="zh-cn_topic_0110861280_p42682030142713"></a>deleteAlertNoticeConfig</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row11827183352314"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p172681530152710"><a name="zh-cn_topic_0110861280_p172681530152710"></a><a name="zh-cn_topic_0110861280_p172681530152710"></a>批量删除告警通知</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p132685309272"><a name="zh-cn_topic_0110861280_p132685309272"></a><a name="zh-cn_topic_0110861280_p132685309272"></a>alertNoticeConfig</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p5268183042718"><a name="zh-cn_topic_0110861280_p5268183042718"></a><a name="zh-cn_topic_0110861280_p5268183042718"></a>batchDeleteAlertNoticeConfig</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1882716337238"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p9268143019279"><a name="zh-cn_topic_0110861280_p9268143019279"></a><a name="zh-cn_topic_0110861280_p9268143019279"></a>删除独享实例</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1426818301272"><a name="zh-cn_topic_0110861280_p1426818301272"></a><a name="zh-cn_topic_0110861280_p1426818301272"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p10268193042713"><a name="zh-cn_topic_0110861280_p10268193042713"></a><a name="zh-cn_topic_0110861280_p10268193042713"></a>deleteInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row128281333192317"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1026863014278"><a name="zh-cn_topic_0110861280_p1026863014278"></a><a name="zh-cn_topic_0110861280_p1026863014278"></a>创建独享实例</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p18268163092717"><a name="zh-cn_topic_0110861280_p18268163092717"></a><a name="zh-cn_topic_0110861280_p18268163092717"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p152681301271"><a name="zh-cn_topic_0110861280_p152681301271"></a><a name="zh-cn_topic_0110861280_p152681301271"></a>createInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row68282033142316"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p13269153022718"><a name="zh-cn_topic_0110861280_p13269153022718"></a><a name="zh-cn_topic_0110861280_p13269153022718"></a>更新独享实例</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p5269230112713"><a name="zh-cn_topic_0110861280_p5269230112713"></a><a name="zh-cn_topic_0110861280_p5269230112713"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1226953082715"><a name="zh-cn_topic_0110861280_p1226953082715"></a><a name="zh-cn_topic_0110861280_p1226953082715"></a>upgradeInstance</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row282823302317"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1269630182716"><a name="zh-cn_topic_0110861280_p1269630182716"></a><a name="zh-cn_topic_0110861280_p1269630182716"></a>修改实例名</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p112694304273"><a name="zh-cn_topic_0110861280_p112694304273"></a><a name="zh-cn_topic_0110861280_p112694304273"></a>instance</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p62696302276"><a name="zh-cn_topic_0110861280_p62696302276"></a><a name="zh-cn_topic_0110861280_p62696302276"></a>alterInstanceName</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row6187195592213"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1269203032716"><a name="zh-cn_topic_0110861280_p1269203032716"></a><a name="zh-cn_topic_0110861280_p1269203032716"></a>添加地址组</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1126919306274"><a name="zh-cn_topic_0110861280_p1126919306274"></a><a name="zh-cn_topic_0110861280_p1126919306274"></a>ip-group</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p526963013278"><a name="zh-cn_topic_0110861280_p526963013278"></a><a name="zh-cn_topic_0110861280_p526963013278"></a>createIPGroup</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row19187755142214"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p192691430182714"><a name="zh-cn_topic_0110861280_p192691430182714"></a><a name="zh-cn_topic_0110861280_p192691430182714"></a>修改地址组</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p112699300275"><a name="zh-cn_topic_0110861280_p112699300275"></a><a name="zh-cn_topic_0110861280_p112699300275"></a>ip-group</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p14269143042720"><a name="zh-cn_topic_0110861280_p14269143042720"></a><a name="zh-cn_topic_0110861280_p14269143042720"></a>modifyIPGroup</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row121873551227"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p11270430152710"><a name="zh-cn_topic_0110861280_p11270430152710"></a><a name="zh-cn_topic_0110861280_p11270430152710"></a>删除地址组</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p152701930132718"><a name="zh-cn_topic_0110861280_p152701930132718"></a><a name="zh-cn_topic_0110861280_p152701930132718"></a>ip-group</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p10270230182711"><a name="zh-cn_topic_0110861280_p10270230182711"></a><a name="zh-cn_topic_0110861280_p10270230182711"></a>deleteIPGroup</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row31873551223"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1927013082717"><a name="zh-cn_topic_0110861280_p1927013082717"></a><a name="zh-cn_topic_0110861280_p1927013082717"></a>创建引用表</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p9270183032715"><a name="zh-cn_topic_0110861280_p9270183032715"></a><a name="zh-cn_topic_0110861280_p9270183032715"></a>valueList</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p192701630192719"><a name="zh-cn_topic_0110861280_p192701630192719"></a><a name="zh-cn_topic_0110861280_p192701630192719"></a>createValueList</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row1118725522218"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p122706301274"><a name="zh-cn_topic_0110861280_p122706301274"></a><a name="zh-cn_topic_0110861280_p122706301274"></a>修改引用表</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p19270830142715"><a name="zh-cn_topic_0110861280_p19270830142715"></a><a name="zh-cn_topic_0110861280_p19270830142715"></a>valueList</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1527003017272"><a name="zh-cn_topic_0110861280_p1527003017272"></a><a name="zh-cn_topic_0110861280_p1527003017272"></a>modifyValueList</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row31871055122215"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1727053052716"><a name="zh-cn_topic_0110861280_p1727053052716"></a><a name="zh-cn_topic_0110861280_p1727053052716"></a>删除引用表</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1127033017272"><a name="zh-cn_topic_0110861280_p1127033017272"></a><a name="zh-cn_topic_0110861280_p1127033017272"></a>valueList</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p4270193072713"><a name="zh-cn_topic_0110861280_p4270193072713"></a><a name="zh-cn_topic_0110861280_p4270193072713"></a>deleteValueList</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row61879554226"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1027003018272"><a name="zh-cn_topic_0110861280_p1027003018272"></a><a name="zh-cn_topic_0110861280_p1027003018272"></a>创建安全报告模板</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p17271630172714"><a name="zh-cn_topic_0110861280_p17271630172714"></a><a name="zh-cn_topic_0110861280_p17271630172714"></a>SecurityReport</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p7271203062710"><a name="zh-cn_topic_0110861280_p7271203062710"></a><a name="zh-cn_topic_0110861280_p7271203062710"></a>createSecurityReportSubscription</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row8187155519229"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p12271183062716"><a name="zh-cn_topic_0110861280_p12271183062716"></a><a name="zh-cn_topic_0110861280_p12271183062716"></a>修改安全报告模板</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p1027173062720"><a name="zh-cn_topic_0110861280_p1027173062720"></a><a name="zh-cn_topic_0110861280_p1027173062720"></a>SecurityReport</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p327193062715"><a name="zh-cn_topic_0110861280_p327193062715"></a><a name="zh-cn_topic_0110861280_p327193062715"></a>updateSecurityReportSubscription</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row318895572211"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p8271123011279"><a name="zh-cn_topic_0110861280_p8271123011279"></a><a name="zh-cn_topic_0110861280_p8271123011279"></a>删除安全报告模板</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p13271630192718"><a name="zh-cn_topic_0110861280_p13271630192718"></a><a name="zh-cn_topic_0110861280_p13271630192718"></a>SecurityReport</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1827120305272"><a name="zh-cn_topic_0110861280_p1827120305272"></a><a name="zh-cn_topic_0110861280_p1827120305272"></a>deleteSecurityReportSubscription</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row8188105517228"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p52716307272"><a name="zh-cn_topic_0110861280_p52716307272"></a><a name="zh-cn_topic_0110861280_p52716307272"></a>购买内容安全检测</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p9271173072713"><a name="zh-cn_topic_0110861280_p9271173072713"></a><a name="zh-cn_topic_0110861280_p9271173072713"></a>content_security</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p15271113016273"><a name="zh-cn_topic_0110861280_p15271113016273"></a><a name="zh-cn_topic_0110861280_p15271113016273"></a>openPostpaidContentSecurity</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row4188955172215"><td class="cellrowborder" valign="top" width="27.48274827482748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p52711730122720"><a name="zh-cn_topic_0110861280_p52711730122720"></a><a name="zh-cn_topic_0110861280_p52711730122720"></a>批量购买内容安全检测</p>
</td>
<td class="cellrowborder" valign="top" width="32.97329732973297%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p112712300278"><a name="zh-cn_topic_0110861280_p112712300278"></a><a name="zh-cn_topic_0110861280_p112712300278"></a>content_security</p>
</td>
<td class="cellrowborder" valign="top" width="39.54395439543954%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p4271143052714"><a name="zh-cn_topic_0110861280_p4271143052714"></a><a name="zh-cn_topic_0110861280_p4271143052714"></a>batchCreateContentSecurityTask</p>
</td>
</tr>
</tbody>
</table>

