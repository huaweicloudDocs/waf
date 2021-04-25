# 配置PCI DSS/3DS合规与TLS<a name="waf_01_0169"></a>

安全传输层协议（Transport Layer Security，TLS）在两个通信应用程序之间提供保密性和数据完整性。HTTPS协议是由TLS+HTTP协议构建的可进行加密传输、身份认证的网络协议。当防护网站的部署模式为“云模式“或“独享模式“且“对外协议“为“HTTPS“时，您可以通过WAF为网站设置最低TLS版本和加密套件（多种加密算法的集合），对于低于最低TLS版本的请求，将无法正常访问网站，以满足行业客户的安全需求。

WAF默认配置的最低TLS版本为TLS v1.0，加密套件为加密套件1，为了确保网站安全，建议您将网站的最低TLS版本和TLS加密套件配置为安全性更高TLS版本和加密套件。

同时，WAF支持开启PCI DSS和PCI 3DS合规认证功能，开启合规认证后，最低TLS版本将设置为TLS v1.2，以满足PCI DSS和PCI 3DS合规认证要求。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果您已开通企业项目，您可以在“企业项目“下拉列表中选择您所在的企业项目，为该企业项目下的域名配置PCI DSS/3DS合规与TLS。

## 前提条件<a name="section7175429781"></a>

-   防护网站的部署模式为“云模式“或“独享模式“。
-   防护网站的“对外协议“使用了HTTPS协议。

## 约束条件<a name="section1119411227134"></a>

当防护网站的“对外协议“为“HTTP“时，HTTP协议不涉及TLS，请忽略该章节。

## 应用场景<a name="section1645404816720"></a>

WAF默认配置的最低TLS版本为“TLS v1.0“，为了确保网站安全，建议您根据业务实际需求进行配置，推荐配置的最低TLS版本如[表1](#table19196118195712)所示。

**表 1**  推荐配置的最低TLS版本说明

<a name="table19196118195712"></a>
<table><thead align="left"><tr id="row5197583579"><th class="cellrowborder" valign="top" width="32.879999999999995%" id="mcps1.2.4.1.1"><p id="p15197785573"><a name="p15197785573"></a><a name="p15197785573"></a>场景</p>
</th>
<th class="cellrowborder" valign="top" width="27.73%" id="mcps1.2.4.1.2"><p id="p1519715814576"><a name="p1519715814576"></a><a name="p1519715814576"></a>最低TLS版本（推荐）</p>
</th>
<th class="cellrowborder" valign="top" width="39.39%" id="mcps1.2.4.1.3"><p id="p178261451497"><a name="p178261451497"></a><a name="p178261451497"></a>防护效果</p>
</th>
</tr>
</thead>
<tbody><tr id="row101976814577"><td class="cellrowborder" valign="top" width="32.879999999999995%" headers="mcps1.2.4.1.1 "><p id="p1419719865716"><a name="p1419719865716"></a><a name="p1419719865716"></a>网站安全性能要求很高（例如，银行金融、证券、电子商务等有重要商业信息和重要数据的行业）</p>
</td>
<td class="cellrowborder" valign="top" width="27.73%" headers="mcps1.2.4.1.2 "><p id="p4197188175710"><a name="p4197188175710"></a><a name="p4197188175710"></a>TLS v1.2</p>
</td>
<td class="cellrowborder" valign="top" width="39.39%" headers="mcps1.2.4.1.3 "><p id="p18266452494"><a name="p18266452494"></a><a name="p18266452494"></a>WAF将自动拦截TLS v1.0和TLS v1.1协议的访问请求。</p>
</td>
</tr>
<tr id="row4197138135711"><td class="cellrowborder" valign="top" width="32.879999999999995%" headers="mcps1.2.4.1.1 "><p id="p519810810573"><a name="p519810810573"></a><a name="p519810810573"></a>网站安全性能要求一般（例如，中小企业门户网站）</p>
</td>
<td class="cellrowborder" valign="top" width="27.73%" headers="mcps1.2.4.1.2 "><p id="p819813819572"><a name="p819813819572"></a><a name="p819813819572"></a>TLS v1.1</p>
</td>
<td class="cellrowborder" valign="top" width="39.39%" headers="mcps1.2.4.1.3 "><p id="p1382664544918"><a name="p1382664544918"></a><a name="p1382664544918"></a>WAF将自动拦截TLS1.0协议的访问请求。</p>
</td>
</tr>
<tr id="row15198128125718"><td class="cellrowborder" valign="top" width="32.879999999999995%" headers="mcps1.2.4.1.1 "><p id="p1719814815572"><a name="p1719814815572"></a><a name="p1719814815572"></a>客户端APP无安全性要求，可以正常访问网站</p>
</td>
<td class="cellrowborder" valign="top" width="27.73%" headers="mcps1.2.4.1.2 "><p id="p1319814885719"><a name="p1319814885719"></a><a name="p1319814885719"></a>TLS v1.0</p>
</td>
<td class="cellrowborder" valign="top" width="39.39%" headers="mcps1.2.4.1.3 "><p id="p58262045144918"><a name="p58262045144918"></a><a name="p58262045144918"></a>所有的TLS协议都可以访问网站。</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>在配置前TLS前，您可以先[查看网站TLS版本](https://myssl.com/ssl.html)。

WAF推荐配置的加密套件为“加密套件1“，可以满足浏览器兼容性和安全性，各加密套件相关说明如[表2](#table173581645172115)所示。

**表 2**  加密套件说明

<a name="table173581645172115"></a>
<table><thead align="left"><tr id="row735934517212"><th class="cellrowborder" valign="top" width="20.830000000000002%" id="mcps1.2.4.1.1"><p id="p8359184512115"><a name="p8359184512115"></a><a name="p8359184512115"></a>加密套件名称</p>
</th>
<th class="cellrowborder" valign="top" width="40.160000000000004%" id="mcps1.2.4.1.2"><p id="p83591545122111"><a name="p83591545122111"></a><a name="p83591545122111"></a>加密算法</p>
</th>
<th class="cellrowborder" valign="top" width="39.01%" id="mcps1.2.4.1.3"><p id="p143597450216"><a name="p143597450216"></a><a name="p143597450216"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2359154512119"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p7359445102116"><a name="p7359445102116"></a><a name="p7359445102116"></a>默认加密套件</p>
</td>
<td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p143591445192111"><a name="p143591445192111"></a><a name="p143591445192111"></a>ECDHE-RSA-AES256-SHA384:AES256-SHA256:RC4:HIGH:!MD5:!aNULL:!eNULL:!NULL:!DH:!EDH:!AESGCM</p>
</td>
<td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><a name="ul435984513212"></a><a name="ul435984513212"></a><ul id="ul435984513212"><li>兼容性：较好，支持的客户端较为广泛</li><li>安全性：一般</li></ul>
</td>
</tr>
<tr id="row2036074516211"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p936074513218"><a name="p936074513218"></a><a name="p936074513218"></a>加密套件1</p>
</td>
<td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p136024532115"><a name="p136024532115"></a><a name="p136024532115"></a>ECDHE-ECDSA-AES256-GCM-SHA384:HIGH:!MEDIUM:!LOW:!aNULL:!eNULL:!DES:!MD5:!PSK:!RC4:!kRSA:!SRP:!3DES:!DSS:!EXP:!CAMELLIA:@STRENGTH</p>
</td>
<td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><p id="p3360645162112"><a name="p3360645162112"></a><a name="p3360645162112"></a>默认推荐配置。</p>
<a name="ul173601845132114"></a><a name="ul173601845132114"></a><ul id="ul173601845132114"><li>兼容性：较好，支持的客户端较为广泛</li><li>安全性：较高</li></ul>
</td>
</tr>
<tr id="row3360545172111"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p2036019456219"><a name="p2036019456219"></a><a name="p2036019456219"></a>加密套件2</p>
</td>
<td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p836012454211"><a name="p836012454211"></a><a name="p836012454211"></a>EECDH+AESGCM:EDH+AESGCM</p>
</td>
<td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><a name="ul33601445152117"></a><a name="ul33601445152117"></a><ul id="ul33601445152117"><li>兼容性：一般，严格符合PCI DSS的FS要求，较低版本浏览器可能无法访问。</li><li>安全性：高</li></ul>
</td>
</tr>
<tr id="row3360114572113"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p133609451218"><a name="p133609451218"></a><a name="p133609451218"></a>加密套件3</p>
</td>
<td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p73611645192116"><a name="p73611645192116"></a><a name="p73611645192116"></a>ECDHE-RSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-SHA384:RC4:HIGH:!MD5:!aNULL:!eNULL:!NULL:!DH:!EDH</p>
</td>
<td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><a name="ul163611045152110"></a><a name="ul163611045152110"></a><ul id="ul163611045152110"><li>兼容性：一般，较低版本浏览器可能无法访问。</li><li>安全性：高，支持ECDHE、DHE-GCM、RSA-AES-GCM多种算法。</li></ul>
</td>
</tr>
<tr id="row83611245192116"><td class="cellrowborder" valign="top" width="20.830000000000002%" headers="mcps1.2.4.1.1 "><p id="p183611645102111"><a name="p183611645102111"></a><a name="p183611645102111"></a>加密套件4</p>
</td>
<td class="cellrowborder" valign="top" width="40.160000000000004%" headers="mcps1.2.4.1.2 "><p id="p6361134532112"><a name="p6361134532112"></a><a name="p6361134532112"></a>ECDHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES128-GCM-SHA256:ECDHE-RSA-AES256-SHA384:AES256-SHA256:RC4:HIGH:!MD5:!aNULL:!eNULL:!NULL:!EDH</p>
</td>
<td class="cellrowborder" valign="top" width="39.01%" headers="mcps1.2.4.1.3 "><a name="ul12361134522117"></a><a name="ul12361134522117"></a><ul id="ul12361134522117"><li>兼容性：较好，支持的客户端较为广泛</li><li>安全性：一般，新增支持GCM算法。</li></ul>
</td>
</tr>
</tbody>
</table>

WAF提供的TLS加密套件对于高版本的浏览器及客户端都可以兼容，不能兼容部分老版本的浏览器，以TLS v1.0协议为例，加密套件不兼容的浏览器及客户端参考说明如[表3](#table893015311885)所示。

>![](public_sys-resources/icon-notice.gif) **须知：** 
>建议您以实际客户端环境测试的兼容情况为准，避免影响现网业务。

**表 3**  加密套件不兼容的浏览器/客户端参考说明（TLS v1.0）

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

## 系统影响<a name="section43561042125018"></a>

-   PCI DSS
    -   开启PCI DSS合规认证后，不能修改TLS最低版本和加密套件，且最低TLS版本将设置为“TLS v1.2“，加密套件设置为EECDH+AESGCM:EDH+AESGCM。
    -   开启PCI DSS合规认证后，如果您需要修改TLS最低版本和加密套件，请关闭该认证。

-   PCI 3DS
    -   开启PCI 3DS合规认证后，不能修改TLS最低版本，且最低TLS版本将设置为“TLS v1.2“。
    -   开启PCI 3DS合规认证后，您将不能关闭该认证，请根据业务实际需求进行操作。


## 操作步骤<a name="section127762575214"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入网站设置页面入口，如[图1](#waf_01_0002_fig172535820151)所示。

    **图 1**  网站设置入口<a name="waf_01_0002_fig172535820151"></a>  
    ![](figures/网站设置入口.png "网站设置入口")

3.  在目标网站所在行的“防护网站“列中，单击目标网站，进入网站基本信息页面。
4.  在“合规认证“行，可以勾选“PCI DSS“或“PCI 3DS“开启合规认证，也可以在“TLS配置“所在行，单击![](figures/icon-edit.jpg)修改TLS配置，如[图2](#fig158391141135917)所示。

    **图 2**  修改TLS配置<a name="fig158391141135917"></a>  
    ![](figures/修改TLS配置.png "修改TLS配置")

    -   勾选“PCI DSS“，系统弹出“警告“对话框，单击“确定“，开启该合规认证。

        ![](figures/PCIDSS.png)

        >![](public_sys-resources/icon-notice.gif) **须知：** 
        >选择开启PCI DSS合规认证后，您将不能修改TLS最低版本和加密套件。

    -   勾选“PCI 3DS“，系统弹出“警告“对话框，单击“确定“，开启该合规认证。

        ![](figures/PCI3DS.png)

        >![](public_sys-resources/icon-notice.gif) **须知：** 
        >-   选择开启PCI 3DS合规认证后，您将不能修改TLS最低版本。
        >-   选择开启PCI 3DS合规认证后，您将不能关闭该认证，请根据业务实际需求进行操作。


5.  在弹出的“TLS配置“对话框中，选择最低TLS版本和加密套件，如[图3](#fig1518314493518)所示。

    **图 3** “TLS配置“对话框<a name="fig1518314493518"></a>  
    ![](figures/TLS配置对话框.png "TLS配置对话框")

    选择“最低TLS版本“，相关说明如下：

    -   默认为TLS v1.0版本，TLS v1.0及以上版本的请求可以访问域名。
    -   选择TLS v1.1版本时，TLS v1.1及以上版本的请求可以访问域名。
    -   选择TLS v1.2版本时，TLS v1.2及以上版本的请求可以访问域名。

6.  单击“确定“，TLS配置完成。

## 生效条件<a name="section168581723173910"></a>

如果“最低TLS版本“配置为“TLS v1.2“，则TLS v1.2协议可以正常访问网站，TLS v1.1及以下协议不能正常访问网站。

