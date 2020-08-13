# 配置TLS最低版本和加密套件<a name="waf_01_0169"></a>

安全传输层协议（Transport Layer Security，TLS）在两个通信应用程序之间提供保密性和数据完整性。HTTPS协议是由TLS+HTTP协议构建的可进行加密传输、身份认证的网络协议，当防护网站的“对外协议“为“HTTPS“时，您可以通过WAF为网站设置最低TLS版本和加密套件（多种加密算法的集合），对于低于最低TLS版本的请求，将无法正常访问网站，以满足行业客户的安全需求。

当防护网站的“对外协议“为“HTTP“时，HTTP协议不涉及TLS，请忽略该章节。

WAF默认配置的最低TLS版本为TLS v1.0，加密套件为默认加密套件（安全性一般），为了确保网站安全，建议您将网站的最低TLS版本和TLS加密套件配置为安全性更高TLS版本和加密套件。

## 前提条件<a name="section1032870191810"></a>

-   已添加防护网站。
-   防护网站的“对外协议“使用了HTTPS协议。

## 加密套件兼容性说明<a name="section1645404816720"></a>

WAF提供的TLS加密套件对于高版本的浏览器及客户端都可以兼容，不能兼容部分老版本的浏览器，以TLS v1.0协议为例，加密套件不兼容的浏览器及客户端参考说明如[表1](#table893015311885)所示。

>![](public_sys-resources/icon-notice.gif) **须知：** 
>建议您以实际客户端环境测试的兼容情况为准，避免影响现网业务。

**表 1**  加密套件不兼容的浏览器/客户端参考说明（TLS v1.0）

<a name="table893015311885"></a>
<table><thead align="left"><tr id="row119311731483"><th class="cellrowborder" valign="top" width="26.97%" id="mcps1.2.7.1.1"><p id="p169317318818"><a name="p169317318818"></a><a name="p169317318818"></a>浏览器/客户端</p>
</th>
<th class="cellrowborder" valign="top" width="17.349999999999998%" id="mcps1.2.7.1.2"><p id="p16232173741215"><a name="p16232173741215"></a><a name="p16232173741215"></a>默认加密套件</p>
</th>
<th class="cellrowborder" valign="top" width="13.36%" id="mcps1.2.7.1.3"><p id="p1734308125"><a name="p1734308125"></a><a name="p1734308125"></a>加密套件1</p>
</th>
<th class="cellrowborder" valign="top" width="13.389999999999999%" id="mcps1.2.7.1.4"><p id="p9221420111214"><a name="p9221420111214"></a><a name="p9221420111214"></a>加密套件2</p>
</th>
<th class="cellrowborder" valign="top" width="14.610000000000001%" id="mcps1.2.7.1.5"><p id="p5507251111210"><a name="p5507251111210"></a><a name="p5507251111210"></a>加密套件3</p>
</th>
<th class="cellrowborder" valign="top" width="14.32%" id="mcps1.2.7.1.6"><p id="p8955202983919"><a name="p8955202983919"></a><a name="p8955202983919"></a>加密套件4</p>
</th>
</tr>
</thead>
<tbody><tr id="row13746162393812"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p137461823173811"><a name="p137461823173811"></a><a name="p137461823173811"></a>Google Chrome 63 /macOS High Sierra 10.13.2</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p2747152373817"><a name="p2747152373817"></a><a name="p2747152373817"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p5747223133817"><a name="p5747223133817"></a><a name="p5747223133817"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p6747123133815"><a name="p6747123133815"></a><a name="p6747123133815"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p15747112317385"><a name="p15747112317385"></a><a name="p15747112317385"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p204345121401"><a name="p204345121401"></a><a name="p204345121401"></a>×</p>
</td>
</tr>
<tr id="row1493112317816"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p5421103816173"><a name="p5421103816173"></a><a name="p5421103816173"></a>Google Chrome 49/ Windows XP SP3</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p19270181182214"><a name="p19270181182214"></a><a name="p19270181182214"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p1426971152217"><a name="p1426971152217"></a><a name="p1426971152217"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p626820172213"><a name="p626820172213"></a><a name="p626820172213"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p326719192217"><a name="p326719192217"></a><a name="p326719192217"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p043461211400"><a name="p043461211400"></a><a name="p043461211400"></a>×</p>
</td>
</tr>
<tr id="row493112311784"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p51066113319"><a name="p51066113319"></a><a name="p51066113319"></a>Internet Explorer</p>
<p id="p1493119312816"><a name="p1493119312816"></a><a name="p1493119312816"></a>6/Windows XP</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p82651215227"><a name="p82651215227"></a><a name="p82651215227"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p1026513162211"><a name="p1026513162211"></a><a name="p1026513162211"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p1826451162212"><a name="p1826451162212"></a><a name="p1826451162212"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p126331152210"><a name="p126331152210"></a><a name="p126331152210"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p24341312194018"><a name="p24341312194018"></a><a name="p24341312194018"></a>×</p>
</td>
</tr>
<tr id="row12932153114810"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p3525161062616"><a name="p3525161062616"></a><a name="p3525161062616"></a>Internet Explorer</p>
<p id="p6932431781"><a name="p6932431781"></a><a name="p6932431781"></a>8/Windows XP</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p112622182217"><a name="p112622182217"></a><a name="p112622182217"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p226151122214"><a name="p226151122214"></a><a name="p226151122214"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p192609182219"><a name="p192609182219"></a><a name="p192609182219"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p625816114220"><a name="p625816114220"></a><a name="p625816114220"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p12434112194011"><a name="p12434112194011"></a><a name="p12434112194011"></a>×</p>
</td>
</tr>
<tr id="row59327312819"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p17386310131819"><a name="p17386310131819"></a><a name="p17386310131819"></a>Safari 6/iOS 6.0.1</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p102571816227"><a name="p102571816227"></a><a name="p102571816227"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p1825613122212"><a name="p1825613122212"></a><a name="p1825613122212"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p22555142212"><a name="p22555142212"></a><a name="p22555142212"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p152131711225"><a name="p152131711225"></a><a name="p152131711225"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p443421214402"><a name="p443421214402"></a><a name="p443421214402"></a>√</p>
</td>
</tr>
<tr id="row1352661317186"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p16527141314182"><a name="p16527141314182"></a><a name="p16527141314182"></a>Safari 7/iOS 7.1</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p1152701381813"><a name="p1152701381813"></a><a name="p1152701381813"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p14527181381812"><a name="p14527181381812"></a><a name="p14527181381812"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p7527161319186"><a name="p7527161319186"></a><a name="p7527161319186"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p25271136180"><a name="p25271136180"></a><a name="p25271136180"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p15435201219407"><a name="p15435201219407"></a><a name="p15435201219407"></a>√</p>
</td>
</tr>
<tr id="row49883179189"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p398841761811"><a name="p398841761811"></a><a name="p398841761811"></a>Safari 7/OS X 10.9</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p14988161719188"><a name="p14988161719188"></a><a name="p14988161719188"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p119886174181"><a name="p119886174181"></a><a name="p119886174181"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p1098851771817"><a name="p1098851771817"></a><a name="p1098851771817"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p1798841771813"><a name="p1798841771813"></a><a name="p1798841771813"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p134351512144014"><a name="p134351512144014"></a><a name="p134351512144014"></a>√</p>
</td>
</tr>
<tr id="row322742921817"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p17227729151815"><a name="p17227729151815"></a><a name="p17227729151815"></a>Safari 8/iOS 8.4</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p11228112912187"><a name="p11228112912187"></a><a name="p11228112912187"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p1922812931819"><a name="p1922812931819"></a><a name="p1922812931819"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p822811294187"><a name="p822811294187"></a><a name="p822811294187"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p522842931817"><a name="p522842931817"></a><a name="p522842931817"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p043571214404"><a name="p043571214404"></a><a name="p043571214404"></a>√</p>
</td>
</tr>
<tr id="row499015324184"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p1899183241819"><a name="p1899183241819"></a><a name="p1899183241819"></a>Safari 8/OS X 10.10</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p199113329184"><a name="p199113329184"></a><a name="p199113329184"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p149911332181816"><a name="p149911332181816"></a><a name="p149911332181816"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p1999173217182"><a name="p1999173217182"></a><a name="p1999173217182"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p199153211182"><a name="p199153211182"></a><a name="p199153211182"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p1143571215406"><a name="p1143571215406"></a><a name="p1143571215406"></a>√</p>
</td>
</tr>
<tr id="row19291110171920"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p8543161312619"><a name="p8543161312619"></a><a name="p8543161312619"></a>Internet Explorer</p>
<p id="p1229110171915"><a name="p1229110171915"></a><a name="p1229110171915"></a>7/Windows Vista</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p10291608199"><a name="p10291608199"></a><a name="p10291608199"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p529111011914"><a name="p529111011914"></a><a name="p529111011914"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p1029110141916"><a name="p1029110141916"></a><a name="p1029110141916"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p1291503192"><a name="p1291503192"></a><a name="p1291503192"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p12435111234014"><a name="p12435111234014"></a><a name="p12435111234014"></a>√</p>
</td>
</tr>
<tr id="row243482441911"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p15911915172618"><a name="p15911915172618"></a><a name="p15911915172618"></a>Internet Explorer</p>
<p id="p7434424151910"><a name="p7434424151910"></a><a name="p7434424151910"></a>8～10/Windows 7</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p9434162411198"><a name="p9434162411198"></a><a name="p9434162411198"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p18434112417198"><a name="p18434112417198"></a><a name="p18434112417198"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p843419243197"><a name="p843419243197"></a><a name="p843419243197"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p0434192451918"><a name="p0434192451918"></a><a name="p0434192451918"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p20435171216408"><a name="p20435171216408"></a><a name="p20435171216408"></a>√</p>
</td>
</tr>
<tr id="row19932121113195"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p17665143017260"><a name="p17665143017260"></a><a name="p17665143017260"></a>Internet Explorer</p>
<p id="p1793321161912"><a name="p1793321161912"></a><a name="p1793321161912"></a>10/Windows Phone 8.0</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p1493321117194"><a name="p1493321117194"></a><a name="p1493321117194"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p8933911191919"><a name="p8933911191919"></a><a name="p8933911191919"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p1933161171918"><a name="p1933161171918"></a><a name="p1933161171918"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p2933131111195"><a name="p2933131111195"></a><a name="p2933131111195"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p94358121409"><a name="p94358121409"></a><a name="p94358121409"></a>√</p>
</td>
</tr>
<tr id="row780362131911"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p18033211194"><a name="p18033211194"></a><a name="p18033211194"></a>Java 7u25</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p180322114194"><a name="p180322114194"></a><a name="p180322114194"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p148031021161912"><a name="p148031021161912"></a><a name="p148031021161912"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p1080302171910"><a name="p1080302171910"></a><a name="p1080302171910"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p980352121915"><a name="p980352121915"></a><a name="p980352121915"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p04351212164018"><a name="p04351212164018"></a><a name="p04351212164018"></a>√</p>
</td>
</tr>
<tr id="row89175614197"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p8101956111912"><a name="p8101956111912"></a><a name="p8101956111912"></a>OpenSSL 0.9.8y</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p17101256101917"><a name="p17101256101917"></a><a name="p17101256101917"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p1910145619199"><a name="p1910145619199"></a><a name="p1910145619199"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p121085671917"><a name="p121085671917"></a><a name="p121085671917"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p1910115617191"><a name="p1910115617191"></a><a name="p1910115617191"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p18435131264017"><a name="p18435131264017"></a><a name="p18435131264017"></a>×</p>
</td>
</tr>
<tr id="row178987528195"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p16898155271915"><a name="p16898155271915"></a><a name="p16898155271915"></a>Safari 5.1.9/OS X 10.6.8</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p289812524194"><a name="p289812524194"></a><a name="p289812524194"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p171018543422"><a name="p171018543422"></a><a name="p171018543422"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="p489875231912"><a name="p489875231912"></a><a name="p489875231912"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p389855211194"><a name="p389855211194"></a><a name="p389855211194"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p17435812114012"><a name="p17435812114012"></a><a name="p17435812114012"></a>√</p>
</td>
</tr>
<tr id="row921993612203"><td class="cellrowborder" valign="top" width="26.97%" headers="mcps1.2.7.1.1 "><p id="p3219636162010"><a name="p3219636162010"></a><a name="p3219636162010"></a>Safari 6.0.4/OS X 10.8.4</p>
</td>
<td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.2.7.1.2 "><p id="p18219123614206"><a name="p18219123614206"></a><a name="p18219123614206"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.36%" headers="mcps1.2.7.1.3 "><p id="p18219153617201"><a name="p18219153617201"></a><a name="p18219153617201"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="13.389999999999999%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0110861186_p15507150319"><a name="zh-cn_topic_0110861186_p15507150319"></a><a name="zh-cn_topic_0110861186_p15507150319"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="14.610000000000001%" headers="mcps1.2.7.1.5 "><p id="p198152058144213"><a name="p198152058144213"></a><a name="p198152058144213"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.32%" headers="mcps1.2.7.1.6 "><p id="p95301713405"><a name="p95301713405"></a><a name="p95301713405"></a>√</p>
</td>
</tr>
</tbody>
</table>

## 操作步骤<a name="section127762575214"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入网站配置页面入口，如[图1](#waf_01_0002_fig172535820151)所示。

    **图 1**  网站列表入口<a name="waf_01_0002_fig172535820151"></a>  
    ![](figures/网站列表入口.png "网站列表入口")

3.  在目标网站所在行的“防护网站“列中，单击目标网站，进入网站基本信息页面。
4.  在“TLS配置“所在行，单击![](figures/icon-edit.jpg)，如[图2](#fig139001072302)所示。

    **图 2**  修改TLS配置<a name="fig139001072302"></a>  
    ![](figures/修改TLS配置.png "修改TLS配置")

5.  在弹出的“TLS配置“对话框中，选择最低TLS版本和加密套件，如[图3](#fig1518314493518)所示，加密套件相关说明如[表2](#table17733717165019)所示。

    **图 3** “TLS配置“对话框<a name="fig1518314493518"></a>  
    ![](figures/TLS配置对话框.png "TLS配置对话框")

    选择“最低TLS版本“，相关说明如下：

    -   默认为TLS v1.0版本，TLS v1.0及以上版本的请求可以访问域名。
    -   选择TLS v1.1版本时，TLS v1.1及以上版本的请求可以访问域名。
    -   选择TLS v1.2版本时，TLS v1.2及以上版本的请求可以访问域名。

    **表 2**  加密套件说明

    <a name="table17733717165019"></a>
    <table><thead align="left"><tr id="row1487913215612"><th class="cellrowborder" valign="top" width="20.830000000000002%" id="mcps1.2.4.1.1"><p id="p6879102195613"><a name="p6879102195613"></a><a name="p6879102195613"></a>加密套件名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.160000000000004%" id="mcps1.2.4.1.2"><p id="p98791626560"><a name="p98791626560"></a><a name="p98791626560"></a>加密算法</p>
    </th>
    <th class="cellrowborder" valign="top" width="39.01%" id="mcps1.2.4.1.3"><p id="p1623713189516"><a name="p1623713189516"></a><a name="p1623713189516"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1687918217567"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p1587916216560"><a name="p1587916216560"></a><a name="p1587916216560"></a>默认加密套件</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p88797218568"><a name="p88797218568"></a><a name="p88797218568"></a>ECDHE-RSA-AES256-SHA384:AES256-SHA256:RC4:HIGH:!MD5:!aNULL:!eNULL:!NULL:!DH:!EDH:!AESGCM</p>
    </td>
    <td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><p id="p1638915377711"><a name="p1638915377711"></a><a name="p1638915377711"></a>默认配置。</p>
    <a name="ul5894331187"></a><a name="ul5894331187"></a><ul id="ul5894331187"><li>兼容性：较好，支持的客户端较为广泛</li><li>安全性：一般</li></ul>
    </td>
    </tr>
    <tr id="row108791825563"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p588032195610"><a name="p588032195610"></a><a name="p588032195610"></a>加密套件1</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p208804235612"><a name="p208804235612"></a><a name="p208804235612"></a>ECDHE-ECDSA-AES256-GCM-SHA384:HIGH:!MEDIUM:!LOW:!aNULL:!eNULL:!DES:!MD5:!PSK:!RC4:!kRSA:!SRP:!3DES:!DSS:!EXP:!CAMELLIA:@STRENGTH</p>
    </td>
    <td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><p id="p162561042181013"><a name="p162561042181013"></a><a name="p162561042181013"></a>推荐配置。</p>
    <a name="ul1251115812815"></a><a name="ul1251115812815"></a><ul id="ul1251115812815"><li>兼容性：较好</li><li>安全性：较高</li></ul>
    </td>
    </tr>
    <tr id="row134001337195610"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p154011373568"><a name="p154011373568"></a><a name="p154011373568"></a>加密套件2</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p4401037105613"><a name="p4401037105613"></a><a name="p4401037105613"></a>EECDH+AESGCM:EDH+AESGCM</p>
    </td>
    <td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><a name="ul1994313292913"></a><a name="ul1994313292913"></a><ul id="ul1994313292913"><li>兼容性：一般，严格符合PCI DSS的FS要求，较低版本浏览器可能无法访问。</li><li>安全性：高</li></ul>
    </td>
    </tr>
    <tr id="row1293124610566"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p99324616566"><a name="p99324616566"></a><a name="p99324616566"></a>加密套件3</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p19334616563"><a name="p19334616563"></a><a name="p19334616563"></a>ECDHE-RSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-SHA384:RC4:HIGH:!MD5:!aNULL:!eNULL:!NULL:!DH:!EDH</p>
    </td>
    <td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><a name="ul9343941131620"></a><a name="ul9343941131620"></a><ul id="ul9343941131620"><li>兼容性：一般，较低版本浏览器可能无法访问。</li><li>安全性：高，支持ECDHE、DHE-GCM、RSA-AES-GCM多种算法。</li></ul>
    </td>
    </tr>
    <tr id="row983711401112"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p1383818401412"><a name="p1383818401412"></a><a name="p1383818401412"></a>加密套件4</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p1083910401818"><a name="p1083910401818"></a><a name="p1083910401818"></a>ECDHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-SHA384:AES256-SHA256:RC4:HIGH:!MD5:!aNULL:!eNULL:!NULL:!EDH</p>
    </td>
    <td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><a name="ul51541821131114"></a><a name="ul51541821131114"></a><ul id="ul51541821131114"><li>兼容性：较好，支持的客户端较为广泛</li><li>安全性：一般，新增支持GCM算法。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

6.  单击“确定“，TLS配置完成。

