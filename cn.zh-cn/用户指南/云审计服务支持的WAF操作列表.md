# 云审计服务支持的WAF操作列表<a name="waf_01_0059"></a>

云审计服务（Cloud Trace Service，CTS）记录了Web应用防火墙相关的操作事件，方便用户日后的查询、审计和回溯，具体请参见云审计服务用户指南。

云审计服务支持的WAF操作列表如[表1](#table5821116193525)所示。

**表 1**  云审计服务支持的WAF操作列表

<a name="table5821116193525"></a>
<table><thead align="left"><tr id="zh-cn_topic_0110861280_row5331520193525"><th class="cellrowborder" valign="top" width="45.93%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0110861280_p1074968493525"><a name="zh-cn_topic_0110861280_p1074968493525"></a><a name="zh-cn_topic_0110861280_p1074968493525"></a>操作名称</p>
</th>
<th class="cellrowborder" valign="top" width="20.74%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0110861280_p6541807593525"><a name="zh-cn_topic_0110861280_p6541807593525"></a><a name="zh-cn_topic_0110861280_p6541807593525"></a>资源类型</p>
</th>
<th class="cellrowborder" valign="top" width="33.33%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0110861280_p6437271493525"><a name="zh-cn_topic_0110861280_p6437271493525"></a><a name="zh-cn_topic_0110861280_p6437271493525"></a>事件名称</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0110861280_row57394824144948"><td class="cellrowborder" valign="top" width="45.93%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p18469135144948"><a name="zh-cn_topic_0110861280_p18469135144948"></a><a name="zh-cn_topic_0110861280_p18469135144948"></a>创建Web应用防火墙防护实例</p>
</td>
<td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p19604987144948"><a name="zh-cn_topic_0110861280_p19604987144948"></a><a name="zh-cn_topic_0110861280_p19604987144948"></a>WAF Instance</p>
</td>
<td class="cellrowborder" valign="top" width="33.33%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p44500148144948"><a name="zh-cn_topic_0110861280_p44500148144948"></a><a name="zh-cn_topic_0110861280_p44500148144948"></a>createWaf</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row37389779145024"><td class="cellrowborder" valign="top" width="45.93%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p8673288145024"><a name="zh-cn_topic_0110861280_p8673288145024"></a><a name="zh-cn_topic_0110861280_p8673288145024"></a>删除Web应用防火墙防护实例</p>
</td>
<td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p31447750145024"><a name="zh-cn_topic_0110861280_p31447750145024"></a><a name="zh-cn_topic_0110861280_p31447750145024"></a>WAF Instance</p>
</td>
<td class="cellrowborder" valign="top" width="33.33%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p64239796145024"><a name="zh-cn_topic_0110861280_p64239796145024"></a><a name="zh-cn_topic_0110861280_p64239796145024"></a>deleteWaf</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row4248352193525"><td class="cellrowborder" valign="top" width="45.93%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p1861315293525"><a name="zh-cn_topic_0110861280_p1861315293525"></a><a name="zh-cn_topic_0110861280_p1861315293525"></a>开启Web应用防火墙防护</p>
</td>
<td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p3127033293525"><a name="zh-cn_topic_0110861280_p3127033293525"></a><a name="zh-cn_topic_0110861280_p3127033293525"></a>WAF Instance</p>
</td>
<td class="cellrowborder" valign="top" width="33.33%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p6501217293729"><a name="zh-cn_topic_0110861280_p6501217293729"></a><a name="zh-cn_topic_0110861280_p6501217293729"></a>openWaf</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row4616713393525"><td class="cellrowborder" valign="top" width="45.93%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p4855028793525"><a name="zh-cn_topic_0110861280_p4855028793525"></a><a name="zh-cn_topic_0110861280_p4855028793525"></a>停止Web应用防火墙防护</p>
</td>
<td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p4025916193525"><a name="zh-cn_topic_0110861280_p4025916193525"></a><a name="zh-cn_topic_0110861280_p4025916193525"></a>WAF Instance</p>
</td>
<td class="cellrowborder" valign="top" width="33.33%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p3976662893525"><a name="zh-cn_topic_0110861280_p3976662893525"></a><a name="zh-cn_topic_0110861280_p3976662893525"></a>stopWaf</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row546871714510"><td class="cellrowborder" valign="top" width="45.93%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p4031292414510"><a name="zh-cn_topic_0110861280_p4031292414510"></a><a name="zh-cn_topic_0110861280_p4031292414510"></a>接入Web应用防火墙防护</p>
</td>
<td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p4412143614510"><a name="zh-cn_topic_0110861280_p4412143614510"></a><a name="zh-cn_topic_0110861280_p4412143614510"></a>WAF Instance</p>
</td>
<td class="cellrowborder" valign="top" width="33.33%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p1706658114510"><a name="zh-cn_topic_0110861280_p1706658114510"></a><a name="zh-cn_topic_0110861280_p1706658114510"></a>accessWaf</p>
</td>
</tr>
<tr id="zh-cn_topic_0110861280_row2235533793525"><td class="cellrowborder" valign="top" width="45.93%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0110861280_p6595189693525"><a name="zh-cn_topic_0110861280_p6595189693525"></a><a name="zh-cn_topic_0110861280_p6595189693525"></a>更新Web应用防火墙防护策略</p>
</td>
<td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0110861280_p4050335593525"><a name="zh-cn_topic_0110861280_p4050335593525"></a><a name="zh-cn_topic_0110861280_p4050335593525"></a>Policy</p>
</td>
<td class="cellrowborder" valign="top" width="33.33%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0110861280_p5954633193525"><a name="zh-cn_topic_0110861280_p5954633193525"></a><a name="zh-cn_topic_0110861280_p5954633193525"></a>updateWafPolicy</p>
</td>
</tr>
</tbody>
</table>

