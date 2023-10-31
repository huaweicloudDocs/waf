# 修改或删除黑白名单IP地址组<a name="waf_01_0358"></a>

您可以通过修改或删除IP地址，管理IP地址组信息。

>![](public_sys-resources/icon-note.gif) **说明：** 
>如果您已开通企业项目，您需要在“企业项目“下拉列表中选择您所在的企业项目并确保已开通操作权限，才能修改或删除该企业项目下的地址组。

## 前提条件<a name="section8174172016525"></a>

已成功创建地址组。

## 约束条件<a name="section757514461272"></a>

-   修改IP地址组时，请确保IP地址组中的IP/IP地址段未添加到其他IP地址组，重复添加同一IP/IP地址段会导致添加IP地址组失败。
-   如果地址组已被黑白名单规则引用，删除地址组前需要解除该地址组与黑白名单规则的绑定关系。

## 操作步骤<a name="section721145410437"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  在左侧导航树中，选择“对象管理  \>  地址组管理“，进入“地址组管理“页面。
3.  选择“我的地址组“页签，进入地址组页面。
4.  在地址组列表中，查看地址组信息。

    **表 1**  参数说明

    <a name="table125091352115811"></a>
    <table><thead align="left"><tr id="row4505152195819"><th class="cellrowborder" valign="top" width="22.18%" id="mcps1.2.3.1.1"><p id="p350545218587"><a name="p350545218587"></a><a name="p350545218587"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="77.82%" id="mcps1.2.3.1.2"><p id="p10505352195814"><a name="p10505352195814"></a><a name="p10505352195814"></a>参数说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row158301572206"><td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.3.1.1 "><p id="p13692818162020"><a name="p13692818162020"></a><a name="p13692818162020"></a>地址组名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.82%" headers="mcps1.2.3.1.2 "><p id="p283119762014"><a name="p283119762014"></a><a name="p283119762014"></a>用户自定义的地址组名称。</p>
    </td>
    </tr>
    <tr id="row9677145842019"><td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.3.1.1 "><p id="p15200127192020"><a name="p15200127192020"></a><a name="p15200127192020"></a>IP/IP段</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.82%" headers="mcps1.2.3.1.2 "><p id="p102002027192020"><a name="p102002027192020"></a><a name="p102002027192020"></a>地址组添加的IP地址/IP地址段。</p>
    </td>
    </tr>
    <tr id="row10507205205815"><td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.3.1.1 "><p id="p7505852195810"><a name="p7505852195810"></a><a name="p7505852195810"></a>应用规则</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.82%" headers="mcps1.2.3.1.2 "><p id="p150595215814"><a name="p150595215814"></a><a name="p150595215814"></a>引用地址组的防护规则。</p>
    </td>
    </tr>
    <tr id="row19507135285819"><td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.3.1.1 "><p id="p1350711523585"><a name="p1350711523585"></a><a name="p1350711523585"></a>备注</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.82%" headers="mcps1.2.3.1.2 "><p id="p1917453716273"><a name="p1917453716273"></a><a name="p1917453716273"></a>地址组补充信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

5.  修改或删除IP地址组。
    -   修改地址组

        在目标地址组所在行的“操作“列中，单击“修改“，在弹出的“修改地址组“对话框中，修改地址组名称或IP地址/IP地址段后，单击“确认“。

    -   删除地址组

        在目标地址组所在行的“操作“列中，单击“删除“，在弹出的提示框中，单击“确认“。

