# WAF监控指标说明<a name="waf_01_0372"></a>

## 功能说明<a name="section1563963116197"></a>

本节定义了Web应用防火墙上报云监控服务的监控指标的命名空间，监控指标列表和维度定义，用户可以通过云监控服务提供管理控制台或API接口来检索Web应用防火墙产生的监控指标和告警信息。

## 命名空间<a name="section20825105342312"></a>

SYS.WAF

>![](public_sys-resources/icon-note.gif) **说明：** 
>命名空间是对一组资源和对象的抽象整合。在同一个集群内可创建不同的命名空间，不同命名空间中的数据彼此隔离。使得它们既可以共享同一个集群的服务，也能够互不干扰。

## 云模式监控指标<a name="section114891410174716"></a>

**表 1**  WAF云模式支持的监控指标

<a name="table5331155094045"></a>
<table><thead align="left"><tr id="r6d6536c2fee4445b882b399175533125"><th class="cellrowborder" valign="top" width="14.81%" id="mcps1.2.7.1.1"><p id="p5968173414918"><a name="p5968173414918"></a><a name="p5968173414918"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="16.939999999999998%" id="mcps1.2.7.1.2"><p id="a017c9e13e1a147b8a9a338f5b361d780"><a name="a017c9e13e1a147b8a9a338f5b361d780"></a><a name="a017c9e13e1a147b8a9a338f5b361d780"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="25.669999999999998%" id="mcps1.2.7.1.3"><p id="aa6e36222233e4ceca1f310b2d5d69052"><a name="aa6e36222233e4ceca1f310b2d5d69052"></a><a name="aa6e36222233e4ceca1f310b2d5d69052"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="15.299999999999999%" id="mcps1.2.7.1.4"><p id="a23532e771f30464eabd4f59c5d499a69"><a name="a23532e771f30464eabd4f59c5d499a69"></a><a name="a23532e771f30464eabd4f59c5d499a69"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="12.91%" id="mcps1.2.7.1.5"><p id="ab18fef49a82249fb986811640525e62c"><a name="ab18fef49a82249fb986811640525e62c"></a><a name="ab18fef49a82249fb986811640525e62c"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="14.37%" id="mcps1.2.7.1.6"><p id="p12742162275016"><a name="p12742162275016"></a><a name="p12742162275016"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row11559523163011"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p1555918230302"><a name="p1555918230302"></a><a name="p1555918230302"></a>requests</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p16129847103016"><a name="p16129847103016"></a><a name="p16129847103016"></a>请求量</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p11559102383012"><a name="p11559102383012"></a><a name="p11559102383012"></a>该指标用于统计测量对象近5分钟内WAF返回的请求量的总数。</p>
<p id="p3151132311325"><a name="p3151132311325"></a><a name="p3151132311325"></a>单位：次</p>
<p id="p17231124119324"><a name="p17231124119324"></a><a name="p17231124119324"></a>采集方式：统计防护域名请求量的总数</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p4628124310339"><a name="p4628124310339"></a><a name="p4628124310339"></a>≥0 次</p>
<p id="p56291437339"><a name="p56291437339"></a><a name="p56291437339"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p13559523113012"><a name="p13559523113012"></a><a name="p13559523113012"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p856032313016"><a name="p856032313016"></a><a name="p856032313016"></a>5分钟</p>
</td>
</tr>
<tr id="row11751310105853"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p1096813424914"><a name="p1096813424914"></a><a name="p1096813424914"></a>waf_http_2xx</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p16962113716286"><a name="p16962113716286"></a><a name="p16962113716286"></a>WAF返回码（2XX）</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p18955054185816"><a name="p18955054185816"></a><a name="p18955054185816"></a>该指标用于统计测量对象近5分钟内WAF返回的2XX状态码的数量。</p>
<p id="p18371300252"><a name="p18371300252"></a><a name="p18371300252"></a>单位：次</p>
<p id="p81621051181018"><a name="p81621051181018"></a><a name="p81621051181018"></a>采集方式：统计WAF引擎返回的2XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p15955125415812"><a name="p15955125415812"></a><a name="p15955125415812"></a>≥0 次</p>
<p id="p6465120181510"><a name="p6465120181510"></a><a name="p6465120181510"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p5975181854814"><a name="p5975181854814"></a><a name="p5975181854814"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p295519548580"><a name="p295519548580"></a><a name="p295519548580"></a>5分钟</p>
</td>
</tr>
<tr id="rbeb3eabf461745118034bbe719999f2e"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p29686344492"><a name="p29686344492"></a><a name="p29686344492"></a>waf_http_3xx</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p2309172035320"><a name="p2309172035320"></a><a name="p2309172035320"></a>WAF返回码（3XX）</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p1830811209539"><a name="p1830811209539"></a><a name="p1830811209539"></a>该指标用于统计测量对象近5分钟内WAF返回的3XX状态码的数量。</p>
<p id="p365513407255"><a name="p365513407255"></a><a name="p365513407255"></a>单位：次</p>
<p id="p45771939171417"><a name="p45771939171417"></a><a name="p45771939171417"></a>采集方式：统计WAF引擎返回的3XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p469544115719"><a name="p469544115719"></a><a name="p469544115719"></a>≥0 次</p>
<p id="p575312291620"><a name="p575312291620"></a><a name="p575312291620"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p844910149486"><a name="p844910149486"></a><a name="p844910149486"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p146781523581"><a name="p146781523581"></a><a name="p146781523581"></a>5分钟</p>
</td>
</tr>
<tr id="rc84866e781ec41cd8b7b65d87b668031"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p14969634144919"><a name="p14969634144919"></a><a name="p14969634144919"></a>waf_http_4xx</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p630412205532"><a name="p630412205532"></a><a name="p630412205532"></a>WAF返回码（4XX）</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p15302420135317"><a name="p15302420135317"></a><a name="p15302420135317"></a>该指标用于统计测量对象近5分钟内WAF返回的4XX状态码的数量。</p>
<p id="p1034454103819"><a name="p1034454103819"></a><a name="p1034454103819"></a>单位：次</p>
<p id="p1376543351815"><a name="p1376543351815"></a><a name="p1376543351815"></a>采集方式：统计WAF引擎返回的4XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p2222204515716"><a name="p2222204515716"></a><a name="p2222204515716"></a>≥0 次</p>
<p id="p1876493016168"><a name="p1876493016168"></a><a name="p1876493016168"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p158516984810"><a name="p158516984810"></a><a name="p158516984810"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p7339165715819"><a name="p7339165715819"></a><a name="p7339165715819"></a>5分钟</p>
</td>
</tr>
<tr id="r52d01ca6b8604b4faf8e54c50d9cf4e6"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p89691334194911"><a name="p89691334194911"></a><a name="p89691334194911"></a>waf_http_5xx</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p2298172010531"><a name="p2298172010531"></a><a name="p2298172010531"></a>WAF返回码（5XX）</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p15297920135316"><a name="p15297920135316"></a><a name="p15297920135316"></a>该指标用于统计测量对象近5分钟内WAF返回的5XX状态码的数量。</p>
<p id="p17998194310259"><a name="p17998194310259"></a><a name="p17998194310259"></a>单位：次</p>
<p id="p826518584197"><a name="p826518584197"></a><a name="p826518584197"></a>采集方式：统计WAF引擎返回的5XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p181278451006"><a name="p181278451006"></a><a name="p181278451006"></a>≥0 次</p>
<p id="p204771343167"><a name="p204771343167"></a><a name="p204771343167"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p1084232481"><a name="p1084232481"></a><a name="p1084232481"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p131272456010"><a name="p131272456010"></a><a name="p131272456010"></a>5分钟</p>
</td>
</tr>
<tr id="rdea637b7e93d4ba8bbcc7a1bf49db3df"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p189691534154917"><a name="p189691534154917"></a><a name="p189691534154917"></a>waf_fused_counts</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p20292820185311"><a name="p20292820185311"></a><a name="p20292820185311"></a>WAF熔断量</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p22900201539"><a name="p22900201539"></a><a name="p22900201539"></a>该指标用于统计测量对象近5分钟内被WAF熔断保护的请求数量。</p>
<p id="p85005478253"><a name="p85005478253"></a><a name="p85005478253"></a>单位：次</p>
<p id="p0541175732011"><a name="p0541175732011"></a><a name="p0541175732011"></a>采集方式：统计防护域名被熔断保护的请求数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p5100103413217"><a name="p5100103413217"></a><a name="p5100103413217"></a>≥0 次</p>
<p id="p39161537141610"><a name="p39161537141610"></a><a name="p39161537141610"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p1667195694716"><a name="p1667195694716"></a><a name="p1667195694716"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p67411751816"><a name="p67411751816"></a><a name="p67411751816"></a>5分钟</p>
</td>
</tr>
<tr id="rda8e47b833a04312b35d502b1facb425"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p39692340495"><a name="p39692340495"></a><a name="p39692340495"></a>inbound_traffic</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p17286920155314"><a name="p17286920155314"></a><a name="p17286920155314"></a>入网总流量</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p1028452085315"><a name="p1028452085315"></a><a name="p1028452085315"></a>该指标用于统计测量对象近5分钟内总入带宽的大小。</p>
<p id="p17524295228"><a name="p17524295228"></a><a name="p17524295228"></a>单位：Mbit</p>
<p id="p77097398213"><a name="p77097398213"></a><a name="p77097398213"></a>采集方式：统计近5分钟内总入带宽的大小</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p1728322025317"><a name="p1728322025317"></a><a name="p1728322025317"></a>≥0 Mbit</p>
<p id="p65342040171618"><a name="p65342040171618"></a><a name="p65342040171618"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p5949154994714"><a name="p5949154994714"></a><a name="p5949154994714"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p6477202416319"><a name="p6477202416319"></a><a name="p6477202416319"></a>5分钟</p>
</td>
</tr>
<tr id="row7121841551"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p171221541356"><a name="p171221541356"></a><a name="p171221541356"></a>outbound_traffic</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p161221841457"><a name="p161221841457"></a><a name="p161221841457"></a>出网总流量</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p012219411955"><a name="p012219411955"></a><a name="p012219411955"></a>该指标用于统计测量对象近5分钟内总出带宽的大小。</p>
<p id="p1867319166296"><a name="p1867319166296"></a><a name="p1867319166296"></a>单位：Mbit</p>
<p id="p186738166292"><a name="p186738166292"></a><a name="p186738166292"></a>采集方式：统计近5分钟内总出带宽的大小</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p65591521868"><a name="p65591521868"></a><a name="p65591521868"></a>≥0 Mbit</p>
<p id="p1848016466169"><a name="p1848016466169"></a><a name="p1848016466169"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p1017063613478"><a name="p1017063613478"></a><a name="p1017063613478"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p115591621462"><a name="p115591621462"></a><a name="p115591621462"></a>5分钟</p>
</td>
</tr>
<tr id="row173551054163813"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p1899182533918"><a name="p1899182533918"></a><a name="p1899182533918"></a>waf_process_time_0</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p2113112264120"><a name="p2113112264120"></a><a name="p2113112264120"></a>WAF处理时延-区间[0-10ms)</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p1869325613417"><a name="p1869325613417"></a><a name="p1869325613417"></a>该指标用于统计测量对象近5分钟内WAF处理时延在区间[0-10ms)内的总数量。</p>
<p id="p15958111834218"><a name="p15958111834218"></a><a name="p15958111834218"></a>单位：次</p>
<p id="p7691425511"><a name="p7691425511"></a><a name="p7691425511"></a>采集方式：统计近5分钟内WAF处理时延在区间[0-10ms)内的总数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p165046282504"><a name="p165046282504"></a><a name="p165046282504"></a>≥0 次</p>
<p id="p2504528125019"><a name="p2504528125019"></a><a name="p2504528125019"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p650402820506"><a name="p650402820506"></a><a name="p650402820506"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p650432835019"><a name="p650432835019"></a><a name="p650432835019"></a>5分钟</p>
</td>
</tr>
<tr id="row3100105913383"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p19991112516396"><a name="p19991112516396"></a><a name="p19991112516396"></a>waf_process_time_10</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p7113112212410"><a name="p7113112212410"></a><a name="p7113112212410"></a>WAF处理时延-区间[10-20ms)</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p1569365613414"><a name="p1569365613414"></a><a name="p1569365613414"></a>该指标用于统计测量对象近5分钟内WAF处理时延在区间[10-20ms)内的总数量。</p>
<p id="p155695218421"><a name="p155695218421"></a><a name="p155695218421"></a>单位：次</p>
<p id="p97374718516"><a name="p97374718516"></a><a name="p97374718516"></a>采集方式：统计近5分钟内WAF处理时延在区间[10-20ms)内的总数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p142741429135015"><a name="p142741429135015"></a><a name="p142741429135015"></a>≥0 次</p>
<p id="p727432995015"><a name="p727432995015"></a><a name="p727432995015"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p20275172925014"><a name="p20275172925014"></a><a name="p20275172925014"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p92751729195015"><a name="p92751729195015"></a><a name="p92751729195015"></a>5分钟</p>
</td>
</tr>
<tr id="row8807186193920"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p599110259391"><a name="p599110259391"></a><a name="p599110259391"></a>waf_process_time_20</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p13113192219411"><a name="p13113192219411"></a><a name="p13113192219411"></a>WAF处理时延-区间[20-50ms)</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p14693155620417"><a name="p14693155620417"></a><a name="p14693155620417"></a>该指标用于统计测量对象近5分钟内WAF处理时延在区间[20-50ms)内的总数量。</p>
<p id="p1818132464216"><a name="p1818132464216"></a><a name="p1818132464216"></a>单位：次</p>
<p id="p732871015514"><a name="p732871015514"></a><a name="p732871015514"></a>采集方式：统计近5分钟内WAF处理时延在区间[20-50ms)内的总数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p161543307507"><a name="p161543307507"></a><a name="p161543307507"></a>≥0 次</p>
<p id="p181548303505"><a name="p181548303505"></a><a name="p181548303505"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p1915473095014"><a name="p1915473095014"></a><a name="p1915473095014"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p1915493018508"><a name="p1915493018508"></a><a name="p1915493018508"></a>5分钟</p>
</td>
</tr>
<tr id="row48071863397"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p099114250395"><a name="p099114250395"></a><a name="p099114250395"></a>waf_process_time_50</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p151134221411"><a name="p151134221411"></a><a name="p151134221411"></a>WAF处理时延-区间[50-100ms)</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p1069385615415"><a name="p1069385615415"></a><a name="p1069385615415"></a>该指标用于统计测量对象近5分钟内WAF处理时延在区间[50-100ms)内的总数量。</p>
<p id="p1477422715425"><a name="p1477422715425"></a><a name="p1477422715425"></a>单位：次</p>
<p id="p1834751314510"><a name="p1834751314510"></a><a name="p1834751314510"></a>采集方式：统计近5分钟内WAF处理时延在区间[50-100ms)内的总数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p891731205010"><a name="p891731205010"></a><a name="p891731205010"></a>≥0 次</p>
<p id="p13911831145012"><a name="p13911831145012"></a><a name="p13911831145012"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p9911131165017"><a name="p9911131165017"></a><a name="p9911131165017"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p691631165016"><a name="p691631165016"></a><a name="p691631165016"></a>5分钟</p>
</td>
</tr>
<tr id="row5177511113915"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p1399122514393"><a name="p1399122514393"></a><a name="p1399122514393"></a>waf_process_time_100</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p91131222174119"><a name="p91131222174119"></a><a name="p91131222174119"></a>WAF处理时延-区间[100-1000ms)</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p76931556174112"><a name="p76931556174112"></a><a name="p76931556174112"></a>该指标用于统计测量对象近5分钟内WAF处理时延在区间[100-1000ms)内的总数量。</p>
<p id="p975131194212"><a name="p975131194212"></a><a name="p975131194212"></a>单位：次</p>
<p id="p7331612514"><a name="p7331612514"></a><a name="p7331612514"></a>采集方式：统计近5分钟内WAF处理时延在区间[100-1000ms)内的总数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p11761132185016"><a name="p11761132185016"></a><a name="p11761132185016"></a>≥0 次</p>
<p id="p676132195014"><a name="p676132195014"></a><a name="p676132195014"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p676332165016"><a name="p676332165016"></a><a name="p676332165016"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p107613215503"><a name="p107613215503"></a><a name="p107613215503"></a>5分钟</p>
</td>
</tr>
<tr id="row19178121116391"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p179911025123910"><a name="p179911025123910"></a><a name="p179911025123910"></a>waf_process_time_1000</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p1113112215412"><a name="p1113112215412"></a><a name="p1113112215412"></a>WAF处理时延-区间[1000+ms)</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p069375617415"><a name="p069375617415"></a><a name="p069375617415"></a>该指标用于统计测量对象近5分钟内WAF处理时延在区间[1000+ms)内的总数量。</p>
<p id="p10835733164217"><a name="p10835733164217"></a><a name="p10835733164217"></a>单位：次</p>
<p id="p154981719145119"><a name="p154981719145119"></a><a name="p154981719145119"></a>采集方式：统计近5分钟内WAF处理时延在区间[1000+ms)内的总数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p16130534155015"><a name="p16130534155015"></a><a name="p16130534155015"></a>≥0 次</p>
<p id="p213153435010"><a name="p213153435010"></a><a name="p213153435010"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p11316344502"><a name="p11316344502"></a><a name="p11316344502"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p9131143415016"><a name="p9131143415016"></a><a name="p9131143415016"></a>5分钟</p>
</td>
</tr>
<tr id="row6178101103914"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p14708664013"><a name="p14708664013"></a><a name="p14708664013"></a>qps_peak</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p611342224116"><a name="p611342224116"></a><a name="p611342224116"></a>QPS峰值</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p6693115684116"><a name="p6693115684116"></a><a name="p6693115684116"></a>该指标用于统计近5分钟内防护域名的QPS峰值。</p>
<p id="p1120918383425"><a name="p1120918383425"></a><a name="p1120918383425"></a>单位：次</p>
<p id="p1798410221510"><a name="p1798410221510"></a><a name="p1798410221510"></a>采集方式：统计近5分钟内防护域名的QPS峰值</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p158821634185017"><a name="p158821634185017"></a><a name="p158821634185017"></a>≥0 次</p>
<p id="p1788203417501"><a name="p1788203417501"></a><a name="p1788203417501"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p588216346505"><a name="p588216346505"></a><a name="p588216346505"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p1988293445011"><a name="p1988293445011"></a><a name="p1988293445011"></a>5分钟</p>
</td>
</tr>
<tr id="row3179181119399"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p847019619402"><a name="p847019619402"></a><a name="p847019619402"></a>qps_mean</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p161131922164118"><a name="p161131922164118"></a><a name="p161131922164118"></a>QPS均值</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p469325615412"><a name="p469325615412"></a><a name="p469325615412"></a>该指标用于统计近5分钟内防护域名的QPS均值。</p>
<p id="p1964414154214"><a name="p1964414154214"></a><a name="p1964414154214"></a>单位：次</p>
<p id="p14362161975516"><a name="p14362161975516"></a><a name="p14362161975516"></a>采集方式：统计近5分钟内防护域名的QPS均值</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p18991336155012"><a name="p18991336155012"></a><a name="p18991336155012"></a>≥0 次</p>
<p id="p899193695011"><a name="p899193695011"></a><a name="p899193695011"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p999183625014"><a name="p999183625014"></a><a name="p999183625014"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p69919369500"><a name="p69919369500"></a><a name="p69919369500"></a>5分钟</p>
</td>
</tr>
<tr id="row644113663913"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p2470469409"><a name="p2470469409"></a><a name="p2470469409"></a>waf_http_0</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p411319228417"><a name="p411319228417"></a><a name="p411319228417"></a>无返回的WAF状态码</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p9693185644113"><a name="p9693185644113"></a><a name="p9693185644113"></a>该指标用于统计测量对象近5分钟内WAF无返回的状态响应码的数量。</p>
<p id="p2728544184211"><a name="p2728544184211"></a><a name="p2728544184211"></a>单位：次</p>
<p id="p180526155111"><a name="p180526155111"></a><a name="p180526155111"></a>采集方式：统计近5分钟内WAF无返回的状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p11640537135016"><a name="p11640537135016"></a><a name="p11640537135016"></a>≥0 次</p>
<p id="p3640837205013"><a name="p3640837205013"></a><a name="p3640837205013"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p196404379506"><a name="p196404379506"></a><a name="p196404379506"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p10640113719504"><a name="p10640113719504"></a><a name="p10640113719504"></a>5分钟</p>
</td>
</tr>
<tr id="row1644736153920"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p10470961404"><a name="p10470961404"></a><a name="p10470961404"></a>upstream_code_2xx</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p711372294119"><a name="p711372294119"></a><a name="p711372294119"></a>业务返回码</p>
<p id="p1113162219414"><a name="p1113162219414"></a><a name="p1113162219414"></a>（2XX）</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p1469315634118"><a name="p1469315634118"></a><a name="p1469315634118"></a>该指标用于统计测量对象近5分钟内业务返回的2XX系列状态响应码的数量。</p>
<p id="p1294374714429"><a name="p1294374714429"></a><a name="p1294374714429"></a>单位：次</p>
<p id="p12478143014512"><a name="p12478143014512"></a><a name="p12478143014512"></a>采集方式：统计近5分钟内业务返回的2XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p11480173817507"><a name="p11480173817507"></a><a name="p11480173817507"></a>≥0 次</p>
<p id="p16480538105013"><a name="p16480538105013"></a><a name="p16480538105013"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p20480153815017"><a name="p20480153815017"></a><a name="p20480153815017"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p19480173819509"><a name="p19480173819509"></a><a name="p19480173819509"></a>5分钟</p>
</td>
</tr>
<tr id="row1263414429398"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p647014624015"><a name="p647014624015"></a><a name="p647014624015"></a>upstream_code_3xx</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p3113182264110"><a name="p3113182264110"></a><a name="p3113182264110"></a>业务返回码</p>
<p id="p1911317229415"><a name="p1911317229415"></a><a name="p1911317229415"></a>（3XX）</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p19693125604115"><a name="p19693125604115"></a><a name="p19693125604115"></a>该指标用于统计测量对象近5分钟内业务返回的3XX系列状态响应码的数量。</p>
<p id="p2029035317427"><a name="p2029035317427"></a><a name="p2029035317427"></a>单位：次</p>
<p id="p1993318338512"><a name="p1993318338512"></a><a name="p1993318338512"></a>采集方式：统计近5分钟内业务返回的3XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p18304113995010"><a name="p18304113995010"></a><a name="p18304113995010"></a>≥0 次</p>
<p id="p23041039145016"><a name="p23041039145016"></a><a name="p23041039145016"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p123041239195019"><a name="p123041239195019"></a><a name="p123041239195019"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p1930414396506"><a name="p1930414396506"></a><a name="p1930414396506"></a>5分钟</p>
</td>
</tr>
<tr id="row4634104293910"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p74704674011"><a name="p74704674011"></a><a name="p74704674011"></a>upstream_code_4xx</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p1113422174116"><a name="p1113422174116"></a><a name="p1113422174116"></a>业务返回码</p>
<p id="p14113142234119"><a name="p14113142234119"></a><a name="p14113142234119"></a>（4XX）</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p136931756104120"><a name="p136931756104120"></a><a name="p136931756104120"></a>该指标用于统计测量对象近5分钟内业务返回的4XX系列状态响应码的数量。</p>
<p id="p86721756164213"><a name="p86721756164213"></a><a name="p86721756164213"></a>单位：次</p>
<p id="p1557317429515"><a name="p1557317429515"></a><a name="p1557317429515"></a>采集方式：统计近5分钟内业务返回的4XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p202461041145011"><a name="p202461041145011"></a><a name="p202461041145011"></a>≥0 次</p>
<p id="p424664114500"><a name="p424664114500"></a><a name="p424664114500"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p2024684125012"><a name="p2024684125012"></a><a name="p2024684125012"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p142461041125017"><a name="p142461041125017"></a><a name="p142461041125017"></a>5分钟</p>
</td>
</tr>
<tr id="row66341142153911"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p747010654010"><a name="p747010654010"></a><a name="p747010654010"></a>upstream_code_5xx</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p0113622194110"><a name="p0113622194110"></a><a name="p0113622194110"></a>业务返回码</p>
<p id="p3113132224116"><a name="p3113132224116"></a><a name="p3113132224116"></a>（5XX）</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p1469345618419"><a name="p1469345618419"></a><a name="p1469345618419"></a>该指标用于统计近5分钟内业务返回的5XX系列状态响应码的数量。</p>
<p id="p889525924213"><a name="p889525924213"></a><a name="p889525924213"></a>单位：次</p>
<p id="p15941845115112"><a name="p15941845115112"></a><a name="p15941845115112"></a>采集方式：统计近5分钟内业务返回的5XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p2091864118504"><a name="p2091864118504"></a><a name="p2091864118504"></a>≥0 次</p>
<p id="p119181041125018"><a name="p119181041125018"></a><a name="p119181041125018"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p18918134112505"><a name="p18918134112505"></a><a name="p18918134112505"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p6919204113505"><a name="p6919204113505"></a><a name="p6919204113505"></a>5分钟</p>
</td>
</tr>
<tr id="row263444218391"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p134709618401"><a name="p134709618401"></a><a name="p134709618401"></a>upstream_code_0</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p911462264111"><a name="p911462264111"></a><a name="p911462264111"></a>无返回的业务状态码</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p2693115617411"><a name="p2693115617411"></a><a name="p2693115617411"></a>该指标用于统计测量对象近5分钟内业务无返回的状态响应码的数量。</p>
<p id="p738923164320"><a name="p738923164320"></a><a name="p738923164320"></a>单位：次</p>
<p id="p161824497513"><a name="p161824497513"></a><a name="p161824497513"></a>采集方式：统计近5分钟内业务无返回的状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p1799174275010"><a name="p1799174275010"></a><a name="p1799174275010"></a>≥0 次</p>
<p id="p10799154211504"><a name="p10799154211504"></a><a name="p10799154211504"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p197994421505"><a name="p197994421505"></a><a name="p197994421505"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p2799342125015"><a name="p2799342125015"></a><a name="p2799342125015"></a>5分钟</p>
</td>
</tr>
<tr id="row81515418405"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p154701863404"><a name="p154701863404"></a><a name="p154701863404"></a>inbound_traffic_peak</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p01141722144114"><a name="p01141722144114"></a><a name="p01141722144114"></a>入网流量的峰值</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p86931656194110"><a name="p86931656194110"></a><a name="p86931656194110"></a>该指标用于统计近5分钟内防护域名入网流量的峰值。</p>
<p id="p1945316615434"><a name="p1945316615434"></a><a name="p1945316615434"></a>单位：Mbit/s</p>
<p id="p0551525513"><a name="p0551525513"></a><a name="p0551525513"></a>采集方式：统计近5分钟内防护域名入网流量的峰值</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p2065804485019"><a name="p2065804485019"></a><a name="p2065804485019"></a>≥0 Mbit/s</p>
<p id="p14659744195014"><a name="p14659744195014"></a><a name="p14659744195014"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p36591448502"><a name="p36591448502"></a><a name="p36591448502"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p1565994435018"><a name="p1565994435018"></a><a name="p1565994435018"></a>5分钟</p>
</td>
</tr>
<tr id="row415220412401"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p1461617124019"><a name="p1461617124019"></a><a name="p1461617124019"></a>inbound_traffic_mean</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p19114522174114"><a name="p19114522174114"></a><a name="p19114522174114"></a>入网流量的均值</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p869310562418"><a name="p869310562418"></a><a name="p869310562418"></a>该指标用于统计近5分钟内防护域名入网流量的均值。</p>
<p id="p15292615164311"><a name="p15292615164311"></a><a name="p15292615164311"></a>单位：Mbit/s</p>
<p id="p10616175715112"><a name="p10616175715112"></a><a name="p10616175715112"></a>采集方式：统计近5分钟内防护域名入网流量的均值</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p3362104545018"><a name="p3362104545018"></a><a name="p3362104545018"></a>≥0 Mbit/s</p>
<p id="p12362845175019"><a name="p12362845175019"></a><a name="p12362845175019"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p103626452507"><a name="p103626452507"></a><a name="p103626452507"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p03621745175018"><a name="p03621745175018"></a><a name="p03621745175018"></a>5分钟</p>
</td>
</tr>
<tr id="row9152114194011"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p761517144016"><a name="p761517144016"></a><a name="p761517144016"></a>outbound_traffic_peak</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p711482214119"><a name="p711482214119"></a><a name="p711482214119"></a>出网流量的峰值</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p19693185615411"><a name="p19693185615411"></a><a name="p19693185615411"></a>该指标用于统计近5分钟内防护域名出网流量的峰值。</p>
<p id="p1724319217434"><a name="p1724319217434"></a><a name="p1724319217434"></a>单位：Mbit/s</p>
<p id="p19209557519"><a name="p19209557519"></a><a name="p19209557519"></a>采集方式：统计近5分钟内防护域名出网流量的峰值</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p16243144765013"><a name="p16243144765013"></a><a name="p16243144765013"></a>≥0 Mbit/s</p>
<p id="p202431747205014"><a name="p202431747205014"></a><a name="p202431747205014"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p20243547145013"><a name="p20243547145013"></a><a name="p20243547145013"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p152431947115012"><a name="p152431947115012"></a><a name="p152431947115012"></a>5分钟</p>
</td>
</tr>
<tr id="row201526417409"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p96151719401"><a name="p96151719401"></a><a name="p96151719401"></a>outbound_traffic_mean</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p1511492218414"><a name="p1511492218414"></a><a name="p1511492218414"></a>出网流量的均值</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p0693175694115"><a name="p0693175694115"></a><a name="p0693175694115"></a>该指标用于统计近5分钟内防护域名出网流量的均值。</p>
<p id="p499182611439"><a name="p499182611439"></a><a name="p499182611439"></a>单位：Mbit/s</p>
<p id="p178730105211"><a name="p178730105211"></a><a name="p178730105211"></a>采集方式：统计近5分钟内防护域名出网流量的均值</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p112534816501"><a name="p112534816501"></a><a name="p112534816501"></a>≥0 Mbit/s</p>
<p id="p2252483507"><a name="p2252483507"></a><a name="p2252483507"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p22544805016"><a name="p22544805016"></a><a name="p22544805016"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p22517482509"><a name="p22517482509"></a><a name="p22517482509"></a>5分钟</p>
</td>
</tr>
<tr id="row53241119141418"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p1446820452142"><a name="p1446820452142"></a><a name="p1446820452142"></a>attacks</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p11468184514144"><a name="p11468184514144"></a><a name="p11468184514144"></a>攻击总次数</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p596820579239"><a name="p596820579239"></a><a name="p596820579239"></a>该指标用于统计近5分钟内防护域名攻击请求量的总数。</p>
<p id="p1468445151418"><a name="p1468445151418"></a><a name="p1468445151418"></a>单位：次</p>
<p id="p164681445191413"><a name="p164681445191413"></a><a name="p164681445191413"></a>采集方式：统计近5分钟内防护域名攻击请求量的总数</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p4468144541410"><a name="p4468144541410"></a><a name="p4468144541410"></a>≥0 次</p>
<p id="p44689459147"><a name="p44689459147"></a><a name="p44689459147"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p2468114521415"><a name="p2468114521415"></a><a name="p2468114521415"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p1846864501414"><a name="p1846864501414"></a><a name="p1846864501414"></a>5分钟</p>
</td>
</tr>
<tr id="row14465142514144"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p178421121162119"><a name="p178421121162119"></a><a name="p178421121162119"></a>crawlers</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p1196619462145"><a name="p1196619462145"></a><a name="p1196619462145"></a>爬虫攻击次数</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p1188151252518"><a name="p1188151252518"></a><a name="p1188151252518"></a>该指标用于统计近5分钟内防护域名爬虫攻击请求量的总数。</p>
<p id="p14966546141419"><a name="p14966546141419"></a><a name="p14966546141419"></a>单位：次</p>
<p id="p1996612460148"><a name="p1996612460148"></a><a name="p1996612460148"></a>采集方式：统计近5分钟内防护域名爬虫攻击请求量的总数</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p4966946141419"><a name="p4966946141419"></a><a name="p4966946141419"></a>≥0 次</p>
<p id="p12966846141415"><a name="p12966846141415"></a><a name="p12966846141415"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p8966184661415"><a name="p8966184661415"></a><a name="p8966184661415"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p11966154681413"><a name="p11966154681413"></a><a name="p11966154681413"></a>5分钟</p>
</td>
</tr>
<tr id="row7514233181419"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p987104831411"><a name="p987104831411"></a><a name="p987104831411"></a>base_protection_counts</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p6980159152215"><a name="p6980159152215"></a><a name="p6980159152215"></a>web基础防护次数</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p987194819147"><a name="p987194819147"></a><a name="p987194819147"></a>该指标用于统计近5分钟内由Web基础防护规则防护的攻击数量。</p>
<p id="p9872487147"><a name="p9872487147"></a><a name="p9872487147"></a>单位：次</p>
<p id="p128712488145"><a name="p128712488145"></a><a name="p128712488145"></a>采集方式：统计近5分钟内由Web基础防护规则防护的攻击数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p1887848101415"><a name="p1887848101415"></a><a name="p1887848101415"></a>≥0 次</p>
<p id="p68717487144"><a name="p68717487144"></a><a name="p68717487144"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p487048131420"><a name="p487048131420"></a><a name="p487048131420"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p58734812140"><a name="p58734812140"></a><a name="p58734812140"></a>5分钟</p>
</td>
</tr>
<tr id="row358153831418"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p14949175014141"><a name="p14949175014141"></a><a name="p14949175014141"></a>precise_protection_counts</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p3949050131414"><a name="p3949050131414"></a><a name="p3949050131414"></a>精准防护次数</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p1494917508144"><a name="p1494917508144"></a><a name="p1494917508144"></a>该指标用于统计近5分钟内由精准防护规则防护的攻击数量。</p>
<p id="p1594945071416"><a name="p1594945071416"></a><a name="p1594945071416"></a>单位：次</p>
<p id="p294917505145"><a name="p294917505145"></a><a name="p294917505145"></a>采集方式：统计近5分钟内由精准防护规则防护的攻击数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p39501350111418"><a name="p39501350111418"></a><a name="p39501350111418"></a>≥0 次</p>
<p id="p99508509149"><a name="p99508509149"></a><a name="p99508509149"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p29508506144"><a name="p29508506144"></a><a name="p29508506144"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p79502501148"><a name="p79502501148"></a><a name="p79502501148"></a>5分钟</p>
</td>
</tr>
<tr id="row981164391411"><td class="cellrowborder" valign="top" width="14.81%" headers="mcps1.2.7.1.1 "><p id="p17240135216148"><a name="p17240135216148"></a><a name="p17240135216148"></a>cc_protection_counts</p>
</td>
<td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.2.7.1.2 "><p id="p82401952111418"><a name="p82401952111418"></a><a name="p82401952111418"></a>cc防护次数</p>
</td>
<td class="cellrowborder" valign="top" width="25.669999999999998%" headers="mcps1.2.7.1.3 "><p id="p763184671510"><a name="p763184671510"></a><a name="p763184671510"></a>该指标用于统计近5分钟内由CC防护规则防护的攻击数量。</p>
<p id="p364846101513"><a name="p364846101513"></a><a name="p364846101513"></a>单位：次</p>
<p id="p764124621513"><a name="p764124621513"></a><a name="p764124621513"></a>采集方式：统计近5分钟内由CC防护规则防护的攻击数量。</p>
</td>
<td class="cellrowborder" valign="top" width="15.299999999999999%" headers="mcps1.2.7.1.4 "><p id="p20241152141415"><a name="p20241152141415"></a><a name="p20241152141415"></a>≥0 次</p>
<p id="p11241352101412"><a name="p11241352101412"></a><a name="p11241352101412"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="12.91%" headers="mcps1.2.7.1.5 "><p id="p1524115241420"><a name="p1524115241420"></a><a name="p1524115241420"></a>防护域名</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p3241155218143"><a name="p3241155218143"></a><a name="p3241155218143"></a>5分钟</p>
</td>
</tr>
</tbody>
</table>

## 独享引擎实例监控指标<a name="section126297421061"></a>

**表 2**  WAF独享引擎实例支持的监控指标

<a name="table462994215614"></a>
<table><thead align="left"><tr id="row36301742562"><th class="cellrowborder" valign="top" width="10.37%" id="mcps1.2.7.1.1"><p id="p7630642264"><a name="p7630642264"></a><a name="p7630642264"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="18.509999999999998%" id="mcps1.2.7.1.2"><p id="p16630184216610"><a name="p16630184216610"></a><a name="p16630184216610"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="21.4%" id="mcps1.2.7.1.3"><p id="p14630164213615"><a name="p14630164213615"></a><a name="p14630164213615"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="15.43%" id="mcps1.2.7.1.4"><p id="p1463054212620"><a name="p1463054212620"></a><a name="p1463054212620"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="19.919999999999998%" id="mcps1.2.7.1.5"><p id="p1163010423615"><a name="p1163010423615"></a><a name="p1163010423615"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="14.37%" id="mcps1.2.7.1.6"><p id="p7630184214613"><a name="p7630184214613"></a><a name="p7630184214613"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row963014421563"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p963074216615"><a name="p963074216615"></a><a name="p963074216615"></a>cpu_util</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p763054212615"><a name="p763054212615"></a><a name="p763054212615"></a>CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p9573153618499"><a name="p9573153618499"></a><a name="p9573153618499"></a>该指标用于统计测量对象的CPU利用率。</p>
<p id="p1886173810387"><a name="p1886173810387"></a><a name="p1886173810387"></a>单位：百分比</p>
<p id="p1386538163810"><a name="p1386538163810"></a><a name="p1386538163810"></a>采集方式：100%减去空闲CPU占比</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p146307422619"><a name="p146307422619"></a><a name="p146307422619"></a>0～100 %</p>
<p id="p108112563410"><a name="p108112563410"></a><a name="p108112563410"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p104741022165014"><a name="p104741022165014"></a><a name="p104741022165014"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p463011426612"><a name="p463011426612"></a><a name="p463011426612"></a>1分钟</p>
</td>
</tr>
<tr id="row14630042160"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p637215118818"><a name="p637215118818"></a><a name="p637215118818"></a>mem_util</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p203695110817"><a name="p203695110817"></a><a name="p203695110817"></a>内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p33669116815"><a name="p33669116815"></a><a name="p33669116815"></a>该指标用于统计测量对象的内存利用率。</p>
<p id="p1599592693912"><a name="p1599592693912"></a><a name="p1599592693912"></a>单位：百分比</p>
<p id="p159951626153916"><a name="p159951626153916"></a><a name="p159951626153916"></a>采集方式：100%减去空闲内存占比</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p1681844145716"><a name="p1681844145716"></a><a name="p1681844145716"></a>0～100 %</p>
<p id="p207708544340"><a name="p207708544340"></a><a name="p207708544340"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p1844122505011"><a name="p1844122505011"></a><a name="p1844122505011"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p119366518911"><a name="p119366518911"></a><a name="p119366518911"></a>1分钟</p>
</td>
</tr>
<tr id="row86311542368"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p1135716119812"><a name="p1135716119812"></a><a name="p1135716119812"></a>disk_util</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p1435221118819"><a name="p1435221118819"></a><a name="p1435221118819"></a>磁盘使用率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p163500111813"><a name="p163500111813"></a><a name="p163500111813"></a>该指标用于统计测量对象的磁盘利用率。</p>
<p id="p11562163819427"><a name="p11562163819427"></a><a name="p11562163819427"></a>单位：百分比</p>
<p id="p17562738164216"><a name="p17562738164216"></a><a name="p17562738164216"></a>采集方式：100%减去空闲磁盘占比</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p136501947994"><a name="p136501947994"></a><a name="p136501947994"></a>0～100 %</p>
<p id="p1024495718348"><a name="p1024495718348"></a><a name="p1024495718348"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p1790292885016"><a name="p1790292885016"></a><a name="p1790292885016"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p20169135311912"><a name="p20169135311912"></a><a name="p20169135311912"></a>1分钟</p>
</td>
</tr>
<tr id="row1763113422066"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p153403111482"><a name="p153403111482"></a><a name="p153403111482"></a>disk_avail_size</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p19337311281"><a name="p19337311281"></a><a name="p19337311281"></a>磁盘可用空间</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p8335141114816"><a name="p8335141114816"></a><a name="p8335141114816"></a>该指标用于统计测量对象的磁盘可用空间。</p>
<p id="p4869151718433"><a name="p4869151718433"></a><a name="p4869151718433"></a>单位：byte、KB、MB、GB、TB、PB</p>
<p id="p1086981744316"><a name="p1086981744316"></a><a name="p1086981744316"></a>采集方式：空闲磁盘空间大小</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p3332111117817"><a name="p3332111117817"></a><a name="p3332111117817"></a>≥0 byte</p>
<p id="p1449140183516"><a name="p1449140183516"></a><a name="p1449140183516"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p10603933125013"><a name="p10603933125013"></a><a name="p10603933125013"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p1232818115812"><a name="p1232818115812"></a><a name="p1232818115812"></a>1分钟</p>
</td>
</tr>
<tr id="row763116421567"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p53251611584"><a name="p53251611584"></a><a name="p53251611584"></a>disk_read_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p132315118810"><a name="p132315118810"></a><a name="p132315118810"></a>磁盘读速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p16320121111814"><a name="p16320121111814"></a><a name="p16320121111814"></a>该指标用于统计测量对象每秒从磁盘读取的字节数。</p>
<p id="p1516513824610"><a name="p1516513824610"></a><a name="p1516513824610"></a>单位：byte/s、KB/s、MB/s、GB/s</p>
<p id="p5771413204613"><a name="p5771413204613"></a><a name="p5771413204613"></a>采集方式：每秒从磁盘读取的字节数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p831741119819"><a name="p831741119819"></a><a name="p831741119819"></a>≥0 byte/s</p>
<p id="p18982393513"><a name="p18982393513"></a><a name="p18982393513"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p32641939185010"><a name="p32641939185010"></a><a name="p32641939185010"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p83131011489"><a name="p83131011489"></a><a name="p83131011489"></a>1分钟</p>
</td>
</tr>
<tr id="row1663154218617"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p163101011487"><a name="p163101011487"></a><a name="p163101011487"></a>disk_write_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p1730851115814"><a name="p1730851115814"></a><a name="p1730851115814"></a>磁盘写速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p1130510119817"><a name="p1130510119817"></a><a name="p1130510119817"></a>该指标用于统计测量对象每秒写入磁盘的字节数。</p>
<p id="p72925141496"><a name="p72925141496"></a><a name="p72925141496"></a>单位：byte/s、KB/s、MB/s、GB/s</p>
<p id="p5292314154920"><a name="p5292314154920"></a><a name="p5292314154920"></a>采集方式：每秒写入磁盘的字节数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p430214116813"><a name="p430214116813"></a><a name="p430214116813"></a>≥0 byte/s</p>
<p id="p43571564358"><a name="p43571564358"></a><a name="p43571564358"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p5195124511503"><a name="p5195124511503"></a><a name="p5195124511503"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p132962111788"><a name="p132962111788"></a><a name="p132962111788"></a>1分钟</p>
</td>
</tr>
<tr id="row863264211610"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p129419113817"><a name="p129419113817"></a><a name="p129419113817"></a>disk_read_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p429221111810"><a name="p429221111810"></a><a name="p429221111810"></a>磁盘读操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p1528941113815"><a name="p1528941113815"></a><a name="p1528941113815"></a>该指标用于统计测量对象每秒从磁盘读取的请求数。</p>
<p id="p5560141110501"><a name="p5560141110501"></a><a name="p5560141110501"></a>单位：请求/秒</p>
<p id="p1556071119508"><a name="p1556071119508"></a><a name="p1556071119508"></a>采集方式：每秒磁盘处理的读取请求数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p182871111582"><a name="p182871111582"></a><a name="p182871111582"></a>≥0 request/s</p>
<p id="p1261739113510"><a name="p1261739113510"></a><a name="p1261739113510"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p696331518504"><a name="p696331518504"></a><a name="p696331518504"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p172814111885"><a name="p172814111885"></a><a name="p172814111885"></a>1分钟</p>
</td>
</tr>
<tr id="row10661141522015"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p1661915142017"><a name="p1661915142017"></a><a name="p1661915142017"></a>disk_write_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p126611155203"><a name="p126611155203"></a><a name="p126611155203"></a>磁盘写操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p66611415172020"><a name="p66611415172020"></a><a name="p66611415172020"></a>该指标用于统计测量对象每秒写入数据到磁盘的请求次数。</p>
<p id="p19621014105214"><a name="p19621014105214"></a><a name="p19621014105214"></a>单位：请求/秒</p>
<p id="p19621914125210"><a name="p19621914125210"></a><a name="p19621914125210"></a>采集方式：每秒磁盘处理的写入请求数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p3661131512204"><a name="p3661131512204"></a><a name="p3661131512204"></a>≥0 request/s</p>
<p id="p12274412123516"><a name="p12274412123516"></a><a name="p12274412123516"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p102841710145011"><a name="p102841710145011"></a><a name="p102841710145011"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p566171519202"><a name="p566171519202"></a><a name="p566171519202"></a>1分钟</p>
</td>
</tr>
<tr id="row11369539194517"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p73691839104514"><a name="p73691839104514"></a><a name="p73691839104514"></a>network_incoming_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p13691439154516"><a name="p13691439154516"></a><a name="p13691439154516"></a>网络流入速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p19369639104517"><a name="p19369639104517"></a><a name="p19369639104517"></a>该指标用于统计测量对象每秒流入测量对象的网络流量。</p>
<p id="p7911010105320"><a name="p7911010105320"></a><a name="p7911010105320"></a>单位：</p>
<p id="p8431252185318"><a name="p8431252185318"></a><a name="p8431252185318"></a>byte/s、KB/s、MB/s、GB/s</p>
<p id="p12911410185312"><a name="p12911410185312"></a><a name="p12911410185312"></a>采集方式：每秒从网络适配器输入的流量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p13693392452"><a name="p13693392452"></a><a name="p13693392452"></a>≥0 byte/s</p>
<p id="p69261428193516"><a name="p69261428193516"></a><a name="p69261428193516"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p20115121355016"><a name="p20115121355016"></a><a name="p20115121355016"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p936913395454"><a name="p936913395454"></a><a name="p936913395454"></a>1分钟</p>
</td>
</tr>
<tr id="row533155715464"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p1533255784610"><a name="p1533255784610"></a><a name="p1533255784610"></a>network_outgoing_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p933210573465"><a name="p933210573465"></a><a name="p933210573465"></a>网络流出速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p153321957114617"><a name="p153321957114617"></a><a name="p153321957114617"></a>该指标用于统计测量对象每秒流出测量对象的网络流量。</p>
<p id="p1787213110548"><a name="p1787213110548"></a><a name="p1787213110548"></a>单位：</p>
<p id="p13872101125413"><a name="p13872101125413"></a><a name="p13872101125413"></a>byte/s、KB/s、MB/s、GB/s</p>
<p id="p79742017175417"><a name="p79742017175417"></a><a name="p79742017175417"></a>采集方式：每秒从网络适配器输出的流量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p103321757184613"><a name="p103321757184613"></a><a name="p103321757184613"></a>≥0 byte/s</p>
<p id="p19821113116359"><a name="p19821113116359"></a><a name="p19821113116359"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p9936365504"><a name="p9936365504"></a><a name="p9936365504"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p10332957104614"><a name="p10332957104614"></a><a name="p10332957104614"></a>1分钟</p>
</td>
</tr>
<tr id="row127181339125010"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p147181139165011"><a name="p147181139165011"></a><a name="p147181139165011"></a>network_incoming_packets_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p1171813391506"><a name="p1171813391506"></a><a name="p1171813391506"></a>网络流入包速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p14718239175016"><a name="p14718239175016"></a><a name="p14718239175016"></a>该指标用于统计测量对象每秒流入测量对象的数据包数量。</p>
<p id="p117392116559"><a name="p117392116559"></a><a name="p117392116559"></a>单位：</p>
<p id="p117401111105516"><a name="p117401111105516"></a><a name="p117401111105516"></a>packet/s</p>
<p id="p13740311125518"><a name="p13740311125518"></a><a name="p13740311125518"></a>采集方式：每秒从网络适配器流入的数据包数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p14718203995013"><a name="p14718203995013"></a><a name="p14718203995013"></a>≥0 packet/s</p>
<p id="p8514194312359"><a name="p8514194312359"></a><a name="p8514194312359"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p15568330503"><a name="p15568330503"></a><a name="p15568330503"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p17718639105013"><a name="p17718639105013"></a><a name="p17718639105013"></a>1分钟</p>
</td>
</tr>
<tr id="row3877122685111"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p138788263518"><a name="p138788263518"></a><a name="p138788263518"></a>network_outgoing_packets_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p38787265513"><a name="p38787265513"></a><a name="p38787265513"></a>网络流出包速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p1987812695112"><a name="p1987812695112"></a><a name="p1987812695112"></a>该指标用于统计测量对象每秒流出测量对象的数据包数量。</p>
<p id="p560734195612"><a name="p560734195612"></a><a name="p560734195612"></a>单位：</p>
<p id="p06075414568"><a name="p06075414568"></a><a name="p06075414568"></a>packet/s</p>
<p id="p196072048563"><a name="p196072048563"></a><a name="p196072048563"></a>采集方式：每秒从网络适配器流出的数据包数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p15878726175113"><a name="p15878726175113"></a><a name="p15878726175113"></a>≥0 packet/s</p>
<p id="p44441810133616"><a name="p44441810133616"></a><a name="p44441810133616"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p5113125813499"><a name="p5113125813499"></a><a name="p5113125813499"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p287842616510"><a name="p287842616510"></a><a name="p287842616510"></a>1分钟</p>
</td>
</tr>
<tr id="row1799819611525"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p1499819612529"><a name="p1499819612529"></a><a name="p1499819612529"></a>concurrent_connections</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p3999116195220"><a name="p3999116195220"></a><a name="p3999116195220"></a>并发连接数</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p159991468525"><a name="p159991468525"></a><a name="p159991468525"></a>该指标用于统计测量对象当前处理的并发连接数量。</p>
<p id="p1172113105812"><a name="p1172113105812"></a><a name="p1172113105812"></a>单位：count</p>
<p id="p1950565045710"><a name="p1950565045710"></a><a name="p1950565045710"></a>采集方式：系统当前的并发连接数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p199936155212"><a name="p199936155212"></a><a name="p199936155212"></a>≥0 count</p>
<p id="p13571132311364"><a name="p13571132311364"></a><a name="p13571132311364"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p974385474915"><a name="p974385474915"></a><a name="p974385474915"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p89999612526"><a name="p89999612526"></a><a name="p89999612526"></a>1分钟</p>
</td>
</tr>
<tr id="row16004433528"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p0601174320529"><a name="p0601174320529"></a><a name="p0601174320529"></a>active_connections</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p156011943135210"><a name="p156011943135210"></a><a name="p156011943135210"></a>活跃连接数</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p16011043155217"><a name="p16011043155217"></a><a name="p16011043155217"></a>该指标用于统计测量对象当前打开的连接数量。</p>
<p id="p9889237593"><a name="p9889237593"></a><a name="p9889237593"></a>单位：count</p>
<p id="p389123105919"><a name="p389123105919"></a><a name="p389123105919"></a>采集方式：系统当前的活跃连接数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p14258172713532"><a name="p14258172713532"></a><a name="p14258172713532"></a>≥0 count</p>
<p id="p15588426133616"><a name="p15588426133616"></a><a name="p15588426133616"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p27395519491"><a name="p27395519491"></a><a name="p27395519491"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p7601143165215"><a name="p7601143165215"></a><a name="p7601143165215"></a>1分钟</p>
</td>
</tr>
<tr id="row179171934185512"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.2.7.1.1 "><p id="p5918103414553"><a name="p5918103414553"></a><a name="p5918103414553"></a>latest_policy_sync_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.2.7.1.2 "><p id="p20918183455517"><a name="p20918183455517"></a><a name="p20918183455517"></a>最近一次策略同步的耗时</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.2.7.1.3 "><p id="p1691815346555"><a name="p1691815346555"></a><a name="p1691815346555"></a>该指标用于统计测量对象最近一次同步WAF策略的耗时。</p>
<p id="p17413633522"><a name="p17413633522"></a><a name="p17413633522"></a>单位：ms</p>
<p id="p1280252213218"><a name="p1280252213218"></a><a name="p1280252213218"></a>采集方式：最近一次同步WAF策略的耗时</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.2.7.1.4 "><p id="p79181734105516"><a name="p79181734105516"></a><a name="p79181734105516"></a>≥0 ms</p>
<p id="p593315283615"><a name="p593315283615"></a><a name="p593315283615"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.2.7.1.5 "><p id="p15932134714495"><a name="p15932134714495"></a><a name="p15932134714495"></a>独享引擎实例</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.6 "><p id="p19181434155510"><a name="p19181434155510"></a><a name="p19181434155510"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 维度<a name="section1918213124512"></a>

<a name="table191062135454"></a>
<table><thead align="left"><tr id="row1510812136454"><th class="cellrowborder" valign="top" width="27.229999999999997%" id="mcps1.1.3.1.1"><p id="p14108171313454"><a name="p14108171313454"></a><a name="p14108171313454"></a>Key</p>
</th>
<th class="cellrowborder" valign="top" width="72.77%" id="mcps1.1.3.1.2"><p id="p101081913124514"><a name="p101081913124514"></a><a name="p101081913124514"></a>Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row17108131354510"><td class="cellrowborder" valign="top" width="27.229999999999997%" headers="mcps1.1.3.1.1 "><p id="p910891310453"><a name="p910891310453"></a><a name="p910891310453"></a>instance_id</p>
</td>
<td class="cellrowborder" valign="top" width="72.77%" headers="mcps1.1.3.1.2 "><p id="p343262704613"><a name="p343262704613"></a><a name="p343262704613"></a>WAF独享引擎实例ID</p>
</td>
</tr>
<tr id="row1989487104611"><td class="cellrowborder" valign="top" width="27.229999999999997%" headers="mcps1.1.3.1.1 "><p id="p08945710463"><a name="p08945710463"></a><a name="p08945710463"></a>waf_instance_id</p>
</td>
<td class="cellrowborder" valign="top" width="72.77%" headers="mcps1.1.3.1.2 "><p id="p128942713464"><a name="p128942713464"></a><a name="p128942713464"></a>WAF防护网站ID</p>
</td>
</tr>
</tbody>
</table>

## 监控指标原始数据格式样例<a name="section88294554206"></a>

```
[
    {
        "metric": {
            // 命名空间
            "namespace": "SYS.WAF",
            "dimensions": [
                {
                    // 维度名称，例如防护网站
                    "name": "waf_instance_id",
                    // 该维度下的监控对象ID，例如防护网站ID
                    "value": "082db2f542e0438aa520035b3e99cd99"
                }
            ],
            // 指标ID
            "metric_name": "waf_http_2xx"
        },
        // 生存时间，指标预定义
        "ttl": 172800,
        // 指标值
        "value": 0.0,
        // 指标单位
        "unit": "Count",
        // 指标值类型
        "type": "float",
        // 指标采集时间
        "collect_time": 1637677359778
    }
]
```

