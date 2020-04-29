# 防护日志记录到LTS<a name="waf_01_0172"></a>

云日志服务（Log Tank Service，简称LTS）对于采集的日志数据，通过海量日志数据的分析与处理，可以为您提供一个实时、高效、安全的日志处理能力。WAF支持将攻击日志、访问日志记录到LTS中，当日志记录到LTS后，日志可以长期保存，您可以通过LTS记录的日志数据，快速高效地进行实时决策分析、设备运维管理以及业务趋势分析。

>![](public_sys-resources/icon-note.gif) **说明：**   
>在WAF管理控制台，您可以查看最近30天的防护日志、下载5天内的所有防护域名的防护日志数据。  

## 注意事项<a name="section23158343527"></a>

LTS按流量单独计费。有关LTS的计费详情，请参见[LTS价格详情](https://www.huaweicloud.com/pricing.html#/lts)。

## 前提条件<a name="section18620173633111"></a>

已成功添加防护域名。

## 将防护日志配置到LTS<a name="section1687712815618"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入全量日志配置入口，如[图1](#fig1030319478517)所示。

    **图 1**  全量日志入口<a name="fig1030319478517"></a>  
    ![](figures/全量日志入口.png "全量日志入口")

3.  开启全量日志![](figures/icon-enable.png)，并选择日志组和日志流，如[图2](#fig928951613101)所示，相关参数说明如[表1](#table11535733111515)所示。

    **图 2**  配置全量日志<a name="fig928951613101"></a>  
    ![](figures/配置全量日志.png "配置全量日志")

    **表 1**  全量日志配置参数

    <a name="table11535733111515"></a>
    <table><thead align="left"><tr id="row353613334158"><th class="cellrowborder" valign="top" width="26.12261226122612%" id="mcps1.2.4.1.1"><p id="p1253613311155"><a name="p1253613311155"></a><a name="p1253613311155"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.54405440544054%" id="mcps1.2.4.1.2"><p id="p1953615334156"><a name="p1953615334156"></a><a name="p1953615334156"></a>参数说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p053618337154"><a name="p053618337154"></a><a name="p053618337154"></a>取值样例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15536143321520"><td class="cellrowborder" valign="top" width="26.12261226122612%" headers="mcps1.2.4.1.1 "><p id="p10652523141810"><a name="p10652523141810"></a><a name="p10652523141810"></a>选择日志组</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.54405440544054%" headers="mcps1.2.4.1.2 "><p id="p2065292319189"><a name="p2065292319189"></a><a name="p2065292319189"></a>选择已创建的日志组，或者单击<span class="parmname" id="zh-cn_topic_0161005736_parmname1410684115716"><a name="zh-cn_topic_0161005736_parmname1410684115716"></a><a name="zh-cn_topic_0161005736_parmname1410684115716"></a>“查看日志组”</span>，跳转到LTS管理控制台创建新的日志组。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p153673314156"><a name="p153673314156"></a><a name="p153673314156"></a><span>lts-group-waf</span></p>
    </td>
    </tr>
    <tr id="row15536133111516"><td class="cellrowborder" valign="top" width="26.12261226122612%" headers="mcps1.2.4.1.1 "><p id="p253615332154"><a name="p253615332154"></a><a name="p253615332154"></a>记录攻击日志</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.54405440544054%" headers="mcps1.2.4.1.2 "><p id="p1032182613309"><a name="p1032182613309"></a><a name="p1032182613309"></a>选择已创建的日志流，或者单击<span class="parmname" id="parmname732112269309"><a name="parmname732112269309"></a><a name="parmname732112269309"></a>“查看日志流”</span>，跳转到LTS管理控制台创建新的日志流。</p>
    <p id="p753615332155"><a name="p753615332155"></a><a name="p753615332155"></a>攻击日志记录每一个攻击告警信息，包括攻击事件类型、防护动作、攻击源IP等信息。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p153623314154"><a name="p153623314154"></a><a name="p153623314154"></a><span>lts-topic-waf-attack</span></p>
    </td>
    </tr>
    <tr id="row5536143301512"><td class="cellrowborder" valign="top" width="26.12261226122612%" headers="mcps1.2.4.1.1 "><p id="p115362335150"><a name="p115362335150"></a><a name="p115362335150"></a>记录访问日志</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.54405440544054%" headers="mcps1.2.4.1.2 "><p id="p184795291303"><a name="p184795291303"></a><a name="p184795291303"></a>选择已创建的日志流，或者单击<span class="parmname" id="parmname10479729153016"><a name="parmname10479729153016"></a><a name="parmname10479729153016"></a>“查看日志流”</span>，跳转到LTS管理控制台创建新的日志流。</p>
    <p id="p115361333191515"><a name="p115361333191515"></a><a name="p115361333191515"></a>访问日志记录每一个HTTP访问的关键信息，包括访问时间、访问客户端IP、访问资源URL等信息。</p>
    </td>
    <td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p1353623321510"><a name="p1353623321510"></a><a name="p1353623321510"></a><span>lts-topic-waf-access</span></p>
    </td>
    </tr>
    </tbody>
    </table>

4.  单击“确定“，全量日志配置成功。

    您可以在LTS管理控制台查看WAF的防护日志。


## 在LTS上查看WAF防护日志<a name="section526212134228"></a>

当您将WAF防护日志配置记录到LTS上后，请参考以下操作步骤，在LTS管理控制台查看、分析记录的WAF日志数据。

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  进入日志流入口，如[图3](#fig11902193715135)所示。

    **图 3**  日志流入口<a name="fig11902193715135"></a>  
    ![](figures/日志流入口.png "日志流入口")

3.  查看WAF防护日志。
    -   查看攻击日志
        1.  在日志流列表，单击配置的攻击日志流“lts-topic-waf-attack“，如[图4](#fig472533374310)所示。

            **图 4**  单击攻击日志流名称<a name="fig472533374310"></a>  
            ![](figures/单击攻击日志流名称.png "单击攻击日志流名称")

        2.  查看攻击日志，日志示例如[图5](#fig3630258133613)所示。

            **图 5**  查看攻击日志<a name="fig3630258133613"></a>  
            ![](figures/查看攻击日志.png "查看攻击日志")


    -   查看访问日志
        1.  在日志流列表，单击配置的访问日志流“lts-topic-waf-access“，如[图6](#fig1079183718507)所示。

            **图 6**  单击访问日志流名称<a name="fig1079183718507"></a>  
            ![](figures/单击访问日志流名称.png "单击访问日志流名称")

        2.  查看访问日志，日志示例如[图7](#fig3826175165212)所示。

            **图 7**  查看访问日志<a name="fig3826175165212"></a>  
            ![](figures/查看访问日志.png "查看访问日志")




## 相关操作<a name="section135831244103615"></a>

如果您不需要将攻击日志、访问日志记录到LTS，您可以关闭全量日志。

