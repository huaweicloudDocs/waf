# 配置威胁情报访问控制拦截/放行指定目标IP库平台内的来源IP<a name="waf_01_0553"></a>

基于互联网数据中心\(Internet Data Center, 简称IDC\)机房的IP库进行访问控制，可选择的IP库平台，包括：鹏博士、谷歌公司、腾讯、美团网等其他平台。配置后，当目标IP库平台内的来源IP向域名下任意路径发起访问请求时，将触发控制规则，即拦截、放行或者仅记录请求。

>![](public_sys-resources/icon-notice.gif) **须知：** 
>威胁情报访问控制功能现处于公测阶段，如需使用请[提交工单](https://support.huaweicloud.com/usermanual-ticket/zh-cn_topic_0127038618.html)申请开通。

## 前提条件<a name="section6191346144914"></a>

已添加防护网站。

## 约束条件<a name="section17523141010224"></a>

-   “云模式“仅专业版和铂金版支持威胁情报访问控制规则。
-   独享模式仅2022年9月及之后的版本支持配置威胁情报访问控制规则，独享引擎版本详情请参见[独享引擎版本迭代](管理独享引擎.md#section7942164410131)。
-   ELB模式不支持配置威胁情报访问控制规则。

## 操作步骤<a name="section236175520494"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  单击管理控制台左上角的![](figures/icon-region-27.jpg)，选择区域或项目。
3.  单击页面左上方的![](figures/icon-Service-39.png)，选择“安全与合规  \>  Web应用防火墙 WAF“。
4.  在左侧导航树中，选择“防护策略“，进入“防护策略“页面。
5.  单击目标策略名称，进入目标策略的防护配置页面。
6.  选择“威胁情报访问控制“配置框，用户可根据自己的需要开启或关闭威胁情报访问控制防护策略。
    -   ![](figures/icon-enable-26.png)：开启状态。
    -   ![](figures/icon-disable.png)：关闭状态。

7.  在规则列表的左上方，单击“添加规则“。
8.  在弹出的对话框中，添加威胁情报访问控制规则，参数说明如[表1](#table831172911312)所示。

    **图 1**  添加威胁情报访问控制规则<a name="fig09717543125"></a>  
    ![](figures/添加威胁情报访问控制规则.png "添加威胁情报访问控制规则")

    **表 1**  参数说明

    <a name="table831172911312"></a>
    <table><thead align="left"><tr id="row7311172918131"><th class="cellrowborder" valign="top" width="22.732273227322732%" id="mcps1.2.4.1.1"><p id="p2046911299201"><a name="p2046911299201"></a><a name="p2046911299201"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.934393439343935%" id="mcps1.2.4.1.2"><p id="p1646915299201"><a name="p1646915299201"></a><a name="p1646915299201"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p18470929192015"><a name="p18470929192015"></a><a name="p18470929192015"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15312029131317"><td class="cellrowborder" valign="top" width="22.732273227322732%" headers="mcps1.2.4.1.1 "><p id="p584751481415"><a name="p584751481415"></a><a name="p584751481415"></a>规则名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.934393439343935%" headers="mcps1.2.4.1.2 "><p id="p331218298139"><a name="p331218298139"></a><a name="p331218298139"></a>自定义规则名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p13312172913133"><a name="p13312172913133"></a><a name="p13312172913133"></a>WAFtest</p>
    </td>
    </tr>
    <tr id="row153121629191311"><td class="cellrowborder" valign="top" width="22.732273227322732%" headers="mcps1.2.4.1.1 "><p id="p112857448140"><a name="p112857448140"></a><a name="p112857448140"></a>规则描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.934393439343935%" headers="mcps1.2.4.1.2 "><p id="p343853654512"><a name="p343853654512"></a><a name="p343853654512"></a>可选参数，设置该规则的备注信息。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1438193610452"><a name="p1438193610452"></a><a name="p1438193610452"></a>--</p>
    </td>
    </tr>
    <tr id="row23124296131"><td class="cellrowborder" valign="top" width="22.732273227322732%" headers="mcps1.2.4.1.1 "><p id="p103122293133"><a name="p103122293133"></a><a name="p103122293133"></a>信息类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.934393439343935%" headers="mcps1.2.4.1.2 "><p id="p14312192981317"><a name="p14312192981317"></a><a name="p14312192981317"></a>在下拉框中选择<span class="parmvalue" id="parmvalue10209919181613"><a name="parmvalue10209919181613"></a><a name="parmvalue10209919181613"></a>“IDC数据中心”</span>，并勾选IDC机房的IP库平台。</p>
    <p id="p12677627151713"><a name="p12677627151713"></a><a name="p12677627151713"></a>可勾选IDC机房的IP库平台，包括：鹏博士、谷歌公司、腾讯、美团网等其他平台。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p13124297133"><a name="p13124297133"></a><a name="p13124297133"></a>IDC数据中心</p>
    <p id="p1499895012321"><a name="p1499895012321"></a><a name="p1499895012321"></a>华为</p>
    </td>
    </tr>
    <tr id="row3312142971318"><td class="cellrowborder" valign="top" width="22.732273227322732%" headers="mcps1.2.4.1.1 "><p id="p1531282914137"><a name="p1531282914137"></a><a name="p1531282914137"></a>防护动作</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.934393439343935%" headers="mcps1.2.4.1.2 "><p id="p17797165213472"><a name="p17797165213472"></a><a name="p17797165213472"></a>可以根据需要选择<span class="parmvalue" id="parmvalue4797452204711"><a name="parmvalue4797452204711"></a><a name="parmvalue4797452204711"></a>“拦截”</span>、<span class="parmvalue" id="parmvalue879755254717"><a name="parmvalue879755254717"></a><a name="parmvalue879755254717"></a>“放行”</span>或者<span class="parmvalue" id="parmvalue079795264716"><a name="parmvalue079795264716"></a><a name="parmvalue079795264716"></a>“仅记录”</span>。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p631282918138"><a name="p631282918138"></a><a name="p631282918138"></a>放行</p>
    </td>
    </tr>
    </tbody>
    </table>

9.  单击“确认“，添加的威胁情报访问控制规则将展示在规则列表中。
    -   规则添加成功后，默认的“规则状态“为“已开启“，若您暂时不想使该规则生效，可在目标规则所在行的“操作“列，单击“关闭“。
    -   若需要修改添加的威胁情报访问控制规则时，可单击待修改的威胁情报访问控制规则所在行的“修改“。
    -   若需要删除用户自行添加的威胁情报访问控制规则时，可单击待删除的威胁情报访问控制规则所在行的“删除“。

