# WAF监控指标说明<a name="waf_01_0372"></a>

## 功能说明<a name="section1563963116197"></a>

本节定义了Web应用防火墙上报云监控服务的监控指标的命名空间，监控指标列表和维度定义，用户可以通过云监控服务提供管理控制台或API接口来检索Web应用防火墙产生的监控指标和告警信息。

## 命名空间<a name="section20825105342312"></a>

SYS.WAF

>![](public_sys-resources/icon-note.gif) **说明：** 
>命名空间是对一组资源和对象的抽象整合。在同一个集群内可创建不同的命名空间，不同命名空间中的数据彼此隔离。使得它们既可以共享同一个集群的服务，也能够互不干扰。

## 独享引擎实例监控指标<a name="section126297421061"></a>

<a name="table462994215614"></a>
<table><thead align="left"><tr id="row36301742562"><th class="cellrowborder" valign="top" width="10.37%" id="mcps1.1.7.1.1"><p id="p7630642264"><a name="p7630642264"></a><a name="p7630642264"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="18.509999999999998%" id="mcps1.1.7.1.2"><p id="p16630184216610"><a name="p16630184216610"></a><a name="p16630184216610"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="21.4%" id="mcps1.1.7.1.3"><p id="p14630164213615"><a name="p14630164213615"></a><a name="p14630164213615"></a>含义</p>
</th>
<th class="cellrowborder" valign="top" width="15.43%" id="mcps1.1.7.1.4"><p id="p1463054212620"><a name="p1463054212620"></a><a name="p1463054212620"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="19.919999999999998%" id="mcps1.1.7.1.5"><p id="p1163010423615"><a name="p1163010423615"></a><a name="p1163010423615"></a>测量对象&amp;维度</p>
</th>
<th class="cellrowborder" valign="top" width="14.37%" id="mcps1.1.7.1.6"><p id="p7630184214613"><a name="p7630184214613"></a><a name="p7630184214613"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row963014421563"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p963074216615"><a name="p963074216615"></a><a name="p963074216615"></a>cpu_util</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p763054212615"><a name="p763054212615"></a><a name="p763054212615"></a>CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p9573153618499"><a name="p9573153618499"></a><a name="p9573153618499"></a>该指标用于统计测量对象的CPU利用率。</p>
<p id="p1886173810387"><a name="p1886173810387"></a><a name="p1886173810387"></a>单位：百分比</p>
<p id="p1386538163810"><a name="p1386538163810"></a><a name="p1386538163810"></a>采集方式：100%减去空闲CPU占比</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p146307422619"><a name="p146307422619"></a><a name="p146307422619"></a>0～100 %</p>
<p id="p108112563410"><a name="p108112563410"></a><a name="p108112563410"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul056144418211"></a><a name="ul056144418211"></a><ul id="ul056144418211"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p463011426612"><a name="p463011426612"></a><a name="p463011426612"></a>1分钟</p>
</td>
</tr>
<tr id="row14630042160"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p637215118818"><a name="p637215118818"></a><a name="p637215118818"></a>mem_util</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p203695110817"><a name="p203695110817"></a><a name="p203695110817"></a>内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p33669116815"><a name="p33669116815"></a><a name="p33669116815"></a>该指标用于统计测量对象的内存利用率。</p>
<p id="p1599592693912"><a name="p1599592693912"></a><a name="p1599592693912"></a>单位：百分比</p>
<p id="p159951626153916"><a name="p159951626153916"></a><a name="p159951626153916"></a>采集方式：100%减去空闲内存占比</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p1681844145716"><a name="p1681844145716"></a><a name="p1681844145716"></a>0～100 %</p>
<p id="p207708544340"><a name="p207708544340"></a><a name="p207708544340"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul1855262712483"></a><a name="ul1855262712483"></a><ul id="ul1855262712483"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p119366518911"><a name="p119366518911"></a><a name="p119366518911"></a>1分钟</p>
</td>
</tr>
<tr id="row86311542368"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p1135716119812"><a name="p1135716119812"></a><a name="p1135716119812"></a>disk_util</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p1435221118819"><a name="p1435221118819"></a><a name="p1435221118819"></a>磁盘使用率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p163500111813"><a name="p163500111813"></a><a name="p163500111813"></a>该指标用于统计测量对象的磁盘利用率。</p>
<p id="p11562163819427"><a name="p11562163819427"></a><a name="p11562163819427"></a>单位：百分比</p>
<p id="p17562738164216"><a name="p17562738164216"></a><a name="p17562738164216"></a>采集方式：100%减去空闲磁盘占比</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p136501947994"><a name="p136501947994"></a><a name="p136501947994"></a>0～100 %</p>
<p id="p1024495718348"><a name="p1024495718348"></a><a name="p1024495718348"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul1627113290489"></a><a name="ul1627113290489"></a><ul id="ul1627113290489"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p20169135311912"><a name="p20169135311912"></a><a name="p20169135311912"></a>1分钟</p>
</td>
</tr>
<tr id="row1763113422066"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p153403111482"><a name="p153403111482"></a><a name="p153403111482"></a>disk_avail_size</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p19337311281"><a name="p19337311281"></a><a name="p19337311281"></a>磁盘可用空间</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p8335141114816"><a name="p8335141114816"></a><a name="p8335141114816"></a>该指标用于统计测量对象的磁盘可用空间。</p>
<p id="p4869151718433"><a name="p4869151718433"></a><a name="p4869151718433"></a>单位：byte、KB、MB、GB、TB、PB</p>
<p id="p1086981744316"><a name="p1086981744316"></a><a name="p1086981744316"></a>采集方式：空闲磁盘空间大小</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p3332111117817"><a name="p3332111117817"></a><a name="p3332111117817"></a>≥0 byte</p>
<p id="p1449140183516"><a name="p1449140183516"></a><a name="p1449140183516"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul10113331104819"></a><a name="ul10113331104819"></a><ul id="ul10113331104819"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p1232818115812"><a name="p1232818115812"></a><a name="p1232818115812"></a>1分钟</p>
</td>
</tr>
<tr id="row763116421567"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p53251611584"><a name="p53251611584"></a><a name="p53251611584"></a>disk_read_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p132315118810"><a name="p132315118810"></a><a name="p132315118810"></a>磁盘读速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p16320121111814"><a name="p16320121111814"></a><a name="p16320121111814"></a>该指标用于统计测量对象每秒从磁盘读取的字节数。</p>
<p id="p1516513824610"><a name="p1516513824610"></a><a name="p1516513824610"></a>单位：byte/s、KB/s、MB/s、GB/s</p>
<p id="p5771413204613"><a name="p5771413204613"></a><a name="p5771413204613"></a>采集方式：每秒从磁盘读取的字节数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p831741119819"><a name="p831741119819"></a><a name="p831741119819"></a>≥0 byte/s</p>
<p id="p18982393513"><a name="p18982393513"></a><a name="p18982393513"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul4519123216485"></a><a name="ul4519123216485"></a><ul id="ul4519123216485"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p83131011489"><a name="p83131011489"></a><a name="p83131011489"></a>1分钟</p>
</td>
</tr>
<tr id="row1663154218617"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p163101011487"><a name="p163101011487"></a><a name="p163101011487"></a>disk_write_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p1730851115814"><a name="p1730851115814"></a><a name="p1730851115814"></a>磁盘写速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p1130510119817"><a name="p1130510119817"></a><a name="p1130510119817"></a>该指标用于统计测量对象每秒写入磁盘的字节数。</p>
<p id="p72925141496"><a name="p72925141496"></a><a name="p72925141496"></a>单位：byte/s、KB/s、MB/s、GB/s</p>
<p id="p5292314154920"><a name="p5292314154920"></a><a name="p5292314154920"></a>采集方式：每秒写入磁盘的字节数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p430214116813"><a name="p430214116813"></a><a name="p430214116813"></a>≥0 byte/s</p>
<p id="p43571564358"><a name="p43571564358"></a><a name="p43571564358"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul14411736104812"></a><a name="ul14411736104812"></a><ul id="ul14411736104812"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p132962111788"><a name="p132962111788"></a><a name="p132962111788"></a>1分钟</p>
</td>
</tr>
<tr id="row863264211610"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p129419113817"><a name="p129419113817"></a><a name="p129419113817"></a>disk_read_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p429221111810"><a name="p429221111810"></a><a name="p429221111810"></a>磁盘读操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p1528941113815"><a name="p1528941113815"></a><a name="p1528941113815"></a>该指标用于统计测量对象每秒从磁盘读取的字节数。</p>
<p id="p5560141110501"><a name="p5560141110501"></a><a name="p5560141110501"></a>单位：请求/秒</p>
<p id="p1556071119508"><a name="p1556071119508"></a><a name="p1556071119508"></a>采集方式：每秒磁盘处理的读取请求数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p182871111582"><a name="p182871111582"></a><a name="p182871111582"></a>≥0 request/s</p>
<p id="p1261739113510"><a name="p1261739113510"></a><a name="p1261739113510"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul14117173813487"></a><a name="ul14117173813487"></a><ul id="ul14117173813487"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p172814111885"><a name="p172814111885"></a><a name="p172814111885"></a>1分钟</p>
</td>
</tr>
<tr id="row10661141522015"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p1661915142017"><a name="p1661915142017"></a><a name="p1661915142017"></a>disk_write_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p126611155203"><a name="p126611155203"></a><a name="p126611155203"></a>磁盘写操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p66611415172020"><a name="p66611415172020"></a><a name="p66611415172020"></a>该指标用于统计测量对象每秒写入数据到磁盘的请求次数。</p>
<p id="p19621014105214"><a name="p19621014105214"></a><a name="p19621014105214"></a>单位：请求/秒</p>
<p id="p19621914125210"><a name="p19621914125210"></a><a name="p19621914125210"></a>采集方式：每秒磁盘处理的写入请求数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p3661131512204"><a name="p3661131512204"></a><a name="p3661131512204"></a>≥0 request/s</p>
<p id="p12274412123516"><a name="p12274412123516"></a><a name="p12274412123516"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul840314013485"></a><a name="ul840314013485"></a><ul id="ul840314013485"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p566171519202"><a name="p566171519202"></a><a name="p566171519202"></a>1分钟</p>
</td>
</tr>
<tr id="row11369539194517"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p73691839104514"><a name="p73691839104514"></a><a name="p73691839104514"></a>network_incoming_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p13691439154516"><a name="p13691439154516"></a><a name="p13691439154516"></a>网络流入速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p19369639104517"><a name="p19369639104517"></a><a name="p19369639104517"></a>该指标用于统计测量对象每秒流入测量对象的网络流量。</p>
<p id="p7911010105320"><a name="p7911010105320"></a><a name="p7911010105320"></a>单位：</p>
<p id="p8431252185318"><a name="p8431252185318"></a><a name="p8431252185318"></a>byte/s、KB/s、MB/s、GB/s</p>
<p id="p12911410185312"><a name="p12911410185312"></a><a name="p12911410185312"></a>采集方式：每秒从网络适配器输入的流量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p13693392452"><a name="p13693392452"></a><a name="p13693392452"></a>≥0 byte/s</p>
<p id="p69261428193516"><a name="p69261428193516"></a><a name="p69261428193516"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul1336914210486"></a><a name="ul1336914210486"></a><ul id="ul1336914210486"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p936913395454"><a name="p936913395454"></a><a name="p936913395454"></a>1分钟</p>
</td>
</tr>
<tr id="row533155715464"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p1533255784610"><a name="p1533255784610"></a><a name="p1533255784610"></a>network_outgoing_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p933210573465"><a name="p933210573465"></a><a name="p933210573465"></a>网络流出速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p153321957114617"><a name="p153321957114617"></a><a name="p153321957114617"></a>该指标用于统计测量对象每秒流出测量对象的网络流量。</p>
<p id="p1787213110548"><a name="p1787213110548"></a><a name="p1787213110548"></a>单位：</p>
<p id="p13872101125413"><a name="p13872101125413"></a><a name="p13872101125413"></a>byte/s、KB/s、MB/s、GB/s</p>
<p id="p79742017175417"><a name="p79742017175417"></a><a name="p79742017175417"></a>采集方式：每秒从网络适配器输出的流量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p103321757184613"><a name="p103321757184613"></a><a name="p103321757184613"></a>≥0 byte/s</p>
<p id="p19821113116359"><a name="p19821113116359"></a><a name="p19821113116359"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul157611436488"></a><a name="ul157611436488"></a><ul id="ul157611436488"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p10332957104614"><a name="p10332957104614"></a><a name="p10332957104614"></a>1分钟</p>
</td>
</tr>
<tr id="row127181339125010"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p147181139165011"><a name="p147181139165011"></a><a name="p147181139165011"></a>network_incoming_packets_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p1171813391506"><a name="p1171813391506"></a><a name="p1171813391506"></a>网络流入包速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p14718239175016"><a name="p14718239175016"></a><a name="p14718239175016"></a>该指标用于统计测量对象每秒流入测量对象的数据包数量。</p>
<p id="p117392116559"><a name="p117392116559"></a><a name="p117392116559"></a>单位：</p>
<p id="p117401111105516"><a name="p117401111105516"></a><a name="p117401111105516"></a>byte/s、KB/s、MB/s、GB/s</p>
<p id="p13740311125518"><a name="p13740311125518"></a><a name="p13740311125518"></a>采集方式：每秒从网络适配器流入的数据包数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p14718203995013"><a name="p14718203995013"></a><a name="p14718203995013"></a>≥0 byte/s</p>
<p id="p8514194312359"><a name="p8514194312359"></a><a name="p8514194312359"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul1486444504817"></a><a name="ul1486444504817"></a><ul id="ul1486444504817"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p17718639105013"><a name="p17718639105013"></a><a name="p17718639105013"></a>1分钟</p>
</td>
</tr>
<tr id="row3877122685111"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p138788263518"><a name="p138788263518"></a><a name="p138788263518"></a>network_outgoing_packets_rate</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p38787265513"><a name="p38787265513"></a><a name="p38787265513"></a>网络流出包速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p1987812695112"><a name="p1987812695112"></a><a name="p1987812695112"></a>该指标用于统计测量对象每秒流出测量对象的数据包数量。</p>
<p id="p560734195612"><a name="p560734195612"></a><a name="p560734195612"></a>单位：</p>
<p id="p06075414568"><a name="p06075414568"></a><a name="p06075414568"></a>byte/s、KB/s、MB/s、GB/s</p>
<p id="p196072048563"><a name="p196072048563"></a><a name="p196072048563"></a>采集方式：每秒从网络适配器流出的数据包数</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p15878726175113"><a name="p15878726175113"></a><a name="p15878726175113"></a>≥0 byte/s</p>
<p id="p44441810133616"><a name="p44441810133616"></a><a name="p44441810133616"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul3329164818488"></a><a name="ul3329164818488"></a><ul id="ul3329164818488"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p287842616510"><a name="p287842616510"></a><a name="p287842616510"></a>1分钟</p>
</td>
</tr>
<tr id="row1799819611525"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p1499819612529"><a name="p1499819612529"></a><a name="p1499819612529"></a>concurrent_connections</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p3999116195220"><a name="p3999116195220"></a><a name="p3999116195220"></a>并发连接数</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p159991468525"><a name="p159991468525"></a><a name="p159991468525"></a>该指标用于统计测量对象当前处理的并发连接数量。</p>
<p id="p1172113105812"><a name="p1172113105812"></a><a name="p1172113105812"></a>单位：count</p>
<p id="p1950565045710"><a name="p1950565045710"></a><a name="p1950565045710"></a>采集方式：系统当前的并发连接数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p199936155212"><a name="p199936155212"></a><a name="p199936155212"></a>≥0 count</p>
<p id="p13571132311364"><a name="p13571132311364"></a><a name="p13571132311364"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul14203050114810"></a><a name="ul14203050114810"></a><ul id="ul14203050114810"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p89999612526"><a name="p89999612526"></a><a name="p89999612526"></a>1分钟</p>
</td>
</tr>
<tr id="row16004433528"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p0601174320529"><a name="p0601174320529"></a><a name="p0601174320529"></a>active_connections</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p156011943135210"><a name="p156011943135210"></a><a name="p156011943135210"></a>活跃连接数</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p16011043155217"><a name="p16011043155217"></a><a name="p16011043155217"></a>该指标用于统计测量对象当前打开的连接数量。</p>
<p id="p9889237593"><a name="p9889237593"></a><a name="p9889237593"></a>单位：count</p>
<p id="p389123105919"><a name="p389123105919"></a><a name="p389123105919"></a>采集方式：系统当前的活跃连接数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p14258172713532"><a name="p14258172713532"></a><a name="p14258172713532"></a>≥0 count</p>
<p id="p15588426133616"><a name="p15588426133616"></a><a name="p15588426133616"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul19919175114483"></a><a name="ul19919175114483"></a><ul id="ul19919175114483"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p7601143165215"><a name="p7601143165215"></a><a name="p7601143165215"></a>1分钟</p>
</td>
</tr>
<tr id="row179171934185512"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p5918103414553"><a name="p5918103414553"></a><a name="p5918103414553"></a>latest_policy_sync_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p20918183455517"><a name="p20918183455517"></a><a name="p20918183455517"></a>最近一次策略同步的耗时</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p1691815346555"><a name="p1691815346555"></a><a name="p1691815346555"></a>该指标用于统计测量对象最近一次同步WAF策略的耗时。</p>
<p id="p17413633522"><a name="p17413633522"></a><a name="p17413633522"></a>单位：ms</p>
<p id="p1280252213218"><a name="p1280252213218"></a><a name="p1280252213218"></a>采集方式：最近一次同步WAF策略的耗时</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p79181734105516"><a name="p79181734105516"></a><a name="p79181734105516"></a>≥0 ms</p>
<p id="p593315283615"><a name="p593315283615"></a><a name="p593315283615"></a>值类型：Int</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul143810301141"></a><a name="ul143810301141"></a><ul id="ul143810301141"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p19181434155510"><a name="p19181434155510"></a><a name="p19181434155510"></a>1分钟</p>
</td>
</tr>
<tr id="row167261016579"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p16672111055715"><a name="p16672111055715"></a><a name="p16672111055715"></a>query_per_second</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p18673131019579"><a name="p18673131019579"></a><a name="p18673131019579"></a>7层查询速率</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p767331025710"><a name="p767331025710"></a><a name="p767331025710"></a>该指标用于统计测量对象当前处理请求的速率。</p>
<p id="p67016748"><a name="p67016748"></a><a name="p67016748"></a>单位：count/s</p>
<p id="p1574161744"><a name="p1574161744"></a><a name="p1574161744"></a>采集方式：WAF引擎处理请求的速率</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p6673161015710"><a name="p6673161015710"></a><a name="p6673161015710"></a>≥0 count/s</p>
<p id="p513462033712"><a name="p513462033712"></a><a name="p513462033712"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul1793442812510"></a><a name="ul1793442812510"></a><ul id="ul1793442812510"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p167318108577"><a name="p167318108577"></a><a name="p167318108577"></a>1分钟</p>
</td>
</tr>
<tr id="row10320455312"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p17314511314"><a name="p17314511314"></a><a name="p17314511314"></a>http_2xx</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p123945333"><a name="p123945333"></a><a name="p123945333"></a>7层协议返回码（2XX）</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p1630451934"><a name="p1630451934"></a><a name="p1630451934"></a>该指标用于统计测量对象当前7层协议2XX系列状态响应码的数量。</p>
<p id="p209251481150"><a name="p209251481150"></a><a name="p209251481150"></a>单位：count</p>
<p id="p9925184819511"><a name="p9925184819511"></a><a name="p9925184819511"></a>采集方式：WAF引擎返回的2XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p0982151118418"><a name="p0982151118418"></a><a name="p0982151118418"></a>≥0 count</p>
<p id="p3320122163710"><a name="p3320122163710"></a><a name="p3320122163710"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul15919487713"></a><a name="ul15919487713"></a><ul id="ul15919487713"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p173445031"><a name="p173445031"></a><a name="p173445031"></a>1分钟</p>
</td>
</tr>
<tr id="row12286229414"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p1829132212414"><a name="p1829132212414"></a><a name="p1829132212414"></a>http_3xx</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p1429162220410"><a name="p1429162220410"></a><a name="p1429162220410"></a>7层协议返回码（3XX）</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p32911221419"><a name="p32911221419"></a><a name="p32911221419"></a>该指标用于统计测量对象当前7层协议3XX系列状态响应码的数量。</p>
<p id="p13360104416119"><a name="p13360104416119"></a><a name="p13360104416119"></a>单位：count</p>
<p id="p936034418112"><a name="p936034418112"></a><a name="p936034418112"></a>采集方式：WAF引擎返回的3XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p141481635127"><a name="p141481635127"></a><a name="p141481635127"></a>≥0 count</p>
<p id="p12187122543716"><a name="p12187122543716"></a><a name="p12187122543716"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul459011311387"></a><a name="ul459011311387"></a><ul id="ul459011311387"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p1829162211416"><a name="p1829162211416"></a><a name="p1829162211416"></a>1分钟</p>
</td>
</tr>
<tr id="row18175121851"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p08172012459"><a name="p08172012459"></a><a name="p08172012459"></a>http_4xx</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p58171121959"><a name="p58171121959"></a><a name="p58171121959"></a>7层协议返回码（4XX）</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p18172121157"><a name="p18172121157"></a><a name="p18172121157"></a>该指标用于统计测量对象当前7层协议4XX系列状态响应码的数量。</p>
<p id="p3601162431219"><a name="p3601162431219"></a><a name="p3601162431219"></a>单位：count</p>
<p id="p66011424111211"><a name="p66011424111211"></a><a name="p66011424111211"></a>采集方式：WAF引擎返回的4XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p128421612124"><a name="p128421612124"></a><a name="p128421612124"></a>≥0 count</p>
<p id="p61335282379"><a name="p61335282379"></a><a name="p61335282379"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul528615335819"></a><a name="ul528615335819"></a><ul id="ul528615335819"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p781721212511"><a name="p781721212511"></a><a name="p781721212511"></a>1分钟</p>
</td>
</tr>
<tr id="row13835181462"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p168354111615"><a name="p168354111615"></a><a name="p168354111615"></a>http_5xx</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p08351010615"><a name="p08351010615"></a><a name="p08351010615"></a>7层协议返回码（5XX）</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p168352012616"><a name="p168352012616"></a><a name="p168352012616"></a>该指标用于统计测量对象当前7层协议5XX系列状态响应码的数量。</p>
<p id="p98391441191213"><a name="p98391441191213"></a><a name="p98391441191213"></a>单位：count</p>
<p id="p2083934112123"><a name="p2083934112123"></a><a name="p2083934112123"></a>采集方式：WAF引擎返回的5XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p43514107127"><a name="p43514107127"></a><a name="p43514107127"></a>≥0 count</p>
<p id="p182841130113716"><a name="p182841130113716"></a><a name="p182841130113716"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul1594911341383"></a><a name="ul1594911341383"></a><ul id="ul1594911341383"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p168359114616"><a name="p168359114616"></a><a name="p168359114616"></a>1分钟</p>
</td>
</tr>
<tr id="row013216343610"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p0132634261"><a name="p0132634261"></a><a name="p0132634261"></a>http_response_time</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p01327341566"><a name="p01327341566"></a><a name="p01327341566"></a>7层协议响应时间</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p713319341065"><a name="p713319341065"></a><a name="p713319341065"></a>该指标用于统计周期内测量对象处理所有请求的平均响应时间。</p>
<p id="p128052010143"><a name="p128052010143"></a><a name="p128052010143"></a>单位：ms</p>
<p id="p369712813142"><a name="p369712813142"></a><a name="p369712813142"></a>采集方式：WAF引擎处理的所有请求的平均响应时间</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p31337340612"><a name="p31337340612"></a><a name="p31337340612"></a>≥0 ms</p>
<p id="p133691733163720"><a name="p133691733163720"></a><a name="p133691733163720"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul1310734917148"></a><a name="ul1310734917148"></a><ul id="ul1310734917148"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p11331734864"><a name="p11331734864"></a><a name="p11331734864"></a>1分钟</p>
</td>
</tr>
<tr id="row175931010675"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p459310107711"><a name="p459310107711"></a><a name="p459310107711"></a>waf_attack_counts</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p1859351017711"><a name="p1859351017711"></a><a name="p1859351017711"></a>Web攻击拦截量</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p16593181016717"><a name="p16593181016717"></a><a name="p16593181016717"></a>该指标用于统计周期内测量对象的WAF引擎拦截的攻击数量。</p>
<p id="p1554414232170"><a name="p1554414232170"></a><a name="p1554414232170"></a>单位：count</p>
<p id="p125441423201712"><a name="p125441423201712"></a><a name="p125441423201712"></a>采集方式：WAF引擎每分钟内拦截的攻击量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p11593101018714"><a name="p11593101018714"></a><a name="p11593101018714"></a>≥0 count</p>
<p id="p4581163563713"><a name="p4581163563713"></a><a name="p4581163563713"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul17949034121813"></a><a name="ul17949034121813"></a><ul id="ul17949034121813"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p759317101272"><a name="p759317101272"></a><a name="p759317101272"></a>1分钟</p>
</td>
</tr>
<tr id="row1274615457718"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p17746245173"><a name="p17746245173"></a><a name="p17746245173"></a>waf_attack_percentage</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p157467451171"><a name="p157467451171"></a><a name="p157467451171"></a>Web攻击拦截占比</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p1874634516711"><a name="p1874634516711"></a><a name="p1874634516711"></a>该指标用于统计周期内测量对象的WAF引擎拦截的攻击数量和总请求数之比。</p>
<p id="p920720576231"><a name="p920720576231"></a><a name="p920720576231"></a>单位：百分比</p>
<p id="p14207145715233"><a name="p14207145715233"></a><a name="p14207145715233"></a>采集方式：WAF引擎每分钟内拦截的攻击数量和总请求数之比</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p177471145377"><a name="p177471145377"></a><a name="p177471145377"></a>0～100%</p>
<p id="p1982413716377"><a name="p1982413716377"></a><a name="p1982413716377"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul23241414202616"></a><a name="ul23241414202616"></a><ul id="ul23241414202616"><li>测量对象：独享引擎实例</li><li>测量维度：instance_id</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p187471145774"><a name="p187471145774"></a><a name="p187471145774"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 云模式监控指标<a name="section114891410174716"></a>

<a name="table5331155094045"></a>
<table><thead align="left"><tr id="r6d6536c2fee4445b882b399175533125"><th class="cellrowborder" valign="top" width="10.37%" id="mcps1.1.7.1.1"><p id="p5968173414918"><a name="p5968173414918"></a><a name="p5968173414918"></a>指标ID</p>
</th>
<th class="cellrowborder" valign="top" width="18.509999999999998%" id="mcps1.1.7.1.2"><p id="a017c9e13e1a147b8a9a338f5b361d780"><a name="a017c9e13e1a147b8a9a338f5b361d780"></a><a name="a017c9e13e1a147b8a9a338f5b361d780"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="21.4%" id="mcps1.1.7.1.3"><p id="aa6e36222233e4ceca1f310b2d5d69052"><a name="aa6e36222233e4ceca1f310b2d5d69052"></a><a name="aa6e36222233e4ceca1f310b2d5d69052"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="15.43%" id="mcps1.1.7.1.4"><p id="a23532e771f30464eabd4f59c5d499a69"><a name="a23532e771f30464eabd4f59c5d499a69"></a><a name="a23532e771f30464eabd4f59c5d499a69"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="19.919999999999998%" id="mcps1.1.7.1.5"><p id="ab18fef49a82249fb986811640525e62c"><a name="ab18fef49a82249fb986811640525e62c"></a><a name="ab18fef49a82249fb986811640525e62c"></a>测量对象&amp;维度</p>
</th>
<th class="cellrowborder" valign="top" width="14.37%" id="mcps1.1.7.1.6"><p id="p12742162275016"><a name="p12742162275016"></a><a name="p12742162275016"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row11751310105853"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p1096813424914"><a name="p1096813424914"></a><a name="p1096813424914"></a>waf_http_2xx</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p8778164113534"><a name="p8778164113534"></a><a name="p8778164113534"></a>7层协议返回码（2XX）</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p18955054185816"><a name="p18955054185816"></a><a name="p18955054185816"></a>该指标用于统计测量对象近5分钟内2XX状态码的数量。</p>
<p id="p18371300252"><a name="p18371300252"></a><a name="p18371300252"></a>单位：次</p>
<p id="p81621051181018"><a name="p81621051181018"></a><a name="p81621051181018"></a>采集方式：统计WAF引擎返回的2XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p15955125415812"><a name="p15955125415812"></a><a name="p15955125415812"></a>≥0 次</p>
<p id="p6465120181510"><a name="p6465120181510"></a><a name="p6465120181510"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul185320221017"></a><a name="ul185320221017"></a><ul id="ul185320221017"><li>测量对象：防护域名</li><li>测量维度：waf_instance_id（云模式实例）</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p295519548580"><a name="p295519548580"></a><a name="p295519548580"></a>5分钟</p>
</td>
</tr>
<tr id="rbeb3eabf461745118034bbe719999f2e"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p29686344492"><a name="p29686344492"></a><a name="p29686344492"></a>waf_http_3xx</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p2309172035320"><a name="p2309172035320"></a><a name="p2309172035320"></a>7层协议返回码（3XX）</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p1830811209539"><a name="p1830811209539"></a><a name="p1830811209539"></a>该指标用于统计测量对象近5分钟内3XX状态码的数量。</p>
<p id="p365513407255"><a name="p365513407255"></a><a name="p365513407255"></a>单位：次</p>
<p id="p45771939171417"><a name="p45771939171417"></a><a name="p45771939171417"></a>采集方式：统计WAF引擎返回的3XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p469544115719"><a name="p469544115719"></a><a name="p469544115719"></a>≥0 次</p>
<p id="p575312291620"><a name="p575312291620"></a><a name="p575312291620"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul199121453154"></a><a name="ul199121453154"></a><ul id="ul199121453154"><li>测量对象：防护域名</li><li>测量维度：waf_instance_id<p id="p35661015143117"><a name="p35661015143117"></a><a name="p35661015143117"></a>（云模式实例）</p>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p146781523581"><a name="p146781523581"></a><a name="p146781523581"></a>5分钟</p>
</td>
</tr>
<tr id="rc84866e781ec41cd8b7b65d87b668031"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p14969634144919"><a name="p14969634144919"></a><a name="p14969634144919"></a>waf_http_4xx</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p630412205532"><a name="p630412205532"></a><a name="p630412205532"></a>7层协议返回码（4XX）</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p15302420135317"><a name="p15302420135317"></a><a name="p15302420135317"></a>该指标用于统计测量对象近5分钟内4XX状态码的数量。</p>
<p id="p1376543351815"><a name="p1376543351815"></a><a name="p1376543351815"></a>采集方式：统计WAF引擎返回的4XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p2222204515716"><a name="p2222204515716"></a><a name="p2222204515716"></a>≥0 次</p>
<p id="p1876493016168"><a name="p1876493016168"></a><a name="p1876493016168"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul7155748191520"></a><a name="ul7155748191520"></a><ul id="ul7155748191520"><li>测量对象：防护域名</li><li>测量维度：waf_instance_id<p id="p1727910171313"><a name="p1727910171313"></a><a name="p1727910171313"></a>（云模式实例）</p>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p7339165715819"><a name="p7339165715819"></a><a name="p7339165715819"></a>5分钟</p>
</td>
</tr>
<tr id="r52d01ca6b8604b4faf8e54c50d9cf4e6"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p89691334194911"><a name="p89691334194911"></a><a name="p89691334194911"></a>waf_http_5xx</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p2298172010531"><a name="p2298172010531"></a><a name="p2298172010531"></a>7层协议返回码（5XX）</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p15297920135316"><a name="p15297920135316"></a><a name="p15297920135316"></a>该指标用于统计测量对象近5分钟内5XX状态码的数量。</p>
<p id="p17998194310259"><a name="p17998194310259"></a><a name="p17998194310259"></a>单位：次</p>
<p id="p826518584197"><a name="p826518584197"></a><a name="p826518584197"></a>采集方式：统计WAF引擎返回的5XX系列状态响应码的数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p181278451006"><a name="p181278451006"></a><a name="p181278451006"></a>≥0 次</p>
<p id="p204771343167"><a name="p204771343167"></a><a name="p204771343167"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul1270355291518"></a><a name="ul1270355291518"></a><ul id="ul1270355291518"><li>测量对象：防护域名</li><li>测量维度：waf_instance_id<p id="p128271910314"><a name="p128271910314"></a><a name="p128271910314"></a>（云模式实例）</p>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p131272456010"><a name="p131272456010"></a><a name="p131272456010"></a>5分钟</p>
</td>
</tr>
<tr id="rdea637b7e93d4ba8bbcc7a1bf49db3df"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p189691534154917"><a name="p189691534154917"></a><a name="p189691534154917"></a>waf_fused_counts</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p20292820185311"><a name="p20292820185311"></a><a name="p20292820185311"></a>Web熔断量</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p22900201539"><a name="p22900201539"></a><a name="p22900201539"></a>该指标用于统计测量对象近5分钟内被熔断保护的请求数量。</p>
<p id="p85005478253"><a name="p85005478253"></a><a name="p85005478253"></a>单位：次</p>
<p id="p0541175732011"><a name="p0541175732011"></a><a name="p0541175732011"></a>采集方式：统计防护域名被熔断保护的请求数量</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p5100103413217"><a name="p5100103413217"></a><a name="p5100103413217"></a>≥0 次</p>
<p id="p39161537141610"><a name="p39161537141610"></a><a name="p39161537141610"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul3567145561512"></a><a name="ul3567145561512"></a><ul id="ul3567145561512"><li>测量对象：防护域名</li><li>测量维度：waf_instance_id<p id="p265592113117"><a name="p265592113117"></a><a name="p265592113117"></a>（云模式实例）</p>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p67411751816"><a name="p67411751816"></a><a name="p67411751816"></a>5分钟</p>
</td>
</tr>
<tr id="rda8e47b833a04312b35d502b1facb425"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p39692340495"><a name="p39692340495"></a><a name="p39692340495"></a>inbound_traffic</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p17286920155314"><a name="p17286920155314"></a><a name="p17286920155314"></a>入带宽</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p1028452085315"><a name="p1028452085315"></a><a name="p1028452085315"></a>该指标用于统计测量对象近5分钟内总入带宽的大小。</p>
<p id="p17524295228"><a name="p17524295228"></a><a name="p17524295228"></a>单位：Mbit</p>
<p id="p77097398213"><a name="p77097398213"></a><a name="p77097398213"></a>采集方式：统计近5分钟内总入带宽的大小</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p1728322025317"><a name="p1728322025317"></a><a name="p1728322025317"></a>≥0 Mbit</p>
<p id="p65342040171618"><a name="p65342040171618"></a><a name="p65342040171618"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul7435123191618"></a><a name="ul7435123191618"></a><ul id="ul7435123191618"><li>测量对象：防护域名</li><li>测量维度：waf_instance_id<p id="p0918112273114"><a name="p0918112273114"></a><a name="p0918112273114"></a>（云模式实例）</p>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p6477202416319"><a name="p6477202416319"></a><a name="p6477202416319"></a>5分钟</p>
</td>
</tr>
<tr id="row7121841551"><td class="cellrowborder" valign="top" width="10.37%" headers="mcps1.1.7.1.1 "><p id="p171221541356"><a name="p171221541356"></a><a name="p171221541356"></a>outbound_traffic</p>
</td>
<td class="cellrowborder" valign="top" width="18.509999999999998%" headers="mcps1.1.7.1.2 "><p id="p161221841457"><a name="p161221841457"></a><a name="p161221841457"></a>出带宽</p>
</td>
<td class="cellrowborder" valign="top" width="21.4%" headers="mcps1.1.7.1.3 "><p id="p012219411955"><a name="p012219411955"></a><a name="p012219411955"></a>该指标用于统计测量对象近5分钟内总出带宽的大小。</p>
<p id="p1867319166296"><a name="p1867319166296"></a><a name="p1867319166296"></a>单位：Mbit</p>
<p id="p186738166292"><a name="p186738166292"></a><a name="p186738166292"></a>采集方式：统计近5分钟内总出带宽的大小</p>
</td>
<td class="cellrowborder" valign="top" width="15.43%" headers="mcps1.1.7.1.4 "><p id="p65591521868"><a name="p65591521868"></a><a name="p65591521868"></a>≥0 Mbit</p>
<p id="p1848016466169"><a name="p1848016466169"></a><a name="p1848016466169"></a>值类型：Float</p>
</td>
<td class="cellrowborder" valign="top" width="19.919999999999998%" headers="mcps1.1.7.1.5 "><a name="ul94212617169"></a><a name="ul94212617169"></a><ul id="ul94212617169"><li>测量对象：防护域名</li><li>测量维度：waf_instance_id<p id="p1377142413119"><a name="p1377142413119"></a><a name="p1377142413119"></a>（云模式实例）</p>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.1.7.1.6 "><p id="p115591621462"><a name="p115591621462"></a><a name="p115591621462"></a>5分钟</p>
</td>
</tr>
</tbody>
</table>

