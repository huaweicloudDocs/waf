# WAF控制台的权限依赖<a name="waf_01_1111"></a>

WAF对其他云服务有诸多依赖关系，因此在您开启IAM系统策略授权后，在WAF Console控制台的各项功能需要配置相应的服务权限后才能正常查看或使用，依赖服务的权限配置均基于您已设置了IAM系统策略授权的WAF FullAccess或WAF ReadOnlyAccess策略权限，详细设置方法请参见[创建用户组并授权使用WAF](创建用户组并授权使用WAF.md)。

## 依赖服务的权限设置<a name="section1574521014310"></a>

如果IAM用户需要在WAF Console控制台拥有相应功能的查看或使用权限，请确认已经对该用户所在的用户组设置了WAF Administrator、WAF FullAccess或WAF ReadOnlyAccess策略的权限，再按照如下[表1](#table5416932173315)增加依赖服务的角色或策略。

**表 1**  WAF Console中依赖服务的角色或策略

<a name="table5416932173315"></a>
<table><thead align="left"><tr id="row04181632173314"><th class="cellrowborder" valign="top" width="24.842484248424842%" id="mcps1.2.4.1.1"><p id="p54181432113311"><a name="p54181432113311"></a><a name="p54181432113311"></a>Console控制台功能</p>
</th>
<th class="cellrowborder" valign="top" width="22.712271227122713%" id="mcps1.2.4.1.2"><p id="p164184327334"><a name="p164184327334"></a><a name="p164184327334"></a>依赖服务</p>
</th>
<th class="cellrowborder" valign="top" width="52.44524452445244%" id="mcps1.2.4.1.3"><p id="p1841813243317"><a name="p1841813243317"></a><a name="p1841813243317"></a>需配置角色/策略</p>
</th>
</tr>
</thead>
<tbody><tr id="row1830313368715"><td class="cellrowborder" valign="top" width="24.842484248424842%" headers="mcps1.2.4.1.1 "><p id="p741873213330"><a name="p741873213330"></a><a name="p741873213330"></a>安全总览</p>
</td>
<td class="cellrowborder" valign="top" width="22.712271227122713%" headers="mcps1.2.4.1.2 "><p id="p124181032103311"><a name="p124181032103311"></a><a name="p124181032103311"></a>企业项目管理服务 EPS</p>
</td>
<td class="cellrowborder" valign="top" width="52.44524452445244%" headers="mcps1.2.4.1.3 "><p id="p24917525719"><a name="p24917525719"></a><a name="p24917525719"></a>需要增加EPS ReadOnlyAccess的系统策略后，才能查看企业项目下总览中数据图表。</p>
</td>
</tr>
<tr id="row6636315143417"><td class="cellrowborder" valign="top" width="24.842484248424842%" headers="mcps1.2.4.1.1 "><p id="p4636121553412"><a name="p4636121553412"></a><a name="p4636121553412"></a>购买WAF实例（独享模式）</p>
</td>
<td class="cellrowborder" valign="top" width="22.712271227122713%" headers="mcps1.2.4.1.2 "><p id="p10102553150"><a name="p10102553150"></a><a name="p10102553150"></a>统一身份认证服务 IAM</p>
<p id="p1563651553418"><a name="p1563651553418"></a><a name="p1563651553418"></a>网络控制台 VPC</p>
<p id="p1945015212359"><a name="p1945015212359"></a><a name="p1945015212359"></a>弹性云服务器 ECS</p>
<p id="p11383115953516"><a name="p11383115953516"></a><a name="p11383115953516"></a>标签管理服务 TMS</p>
</td>
<td class="cellrowborder" valign="top" width="52.44524452445244%" headers="mcps1.2.4.1.3 "><a name="ul19265157137"></a><a name="ul19265157137"></a><ul id="ul19265157137"><li>如果使用IAM用户购买WAF独享模式，需要为该IAM用户创建统一身份认证服务管理权限。首次购买，需要授予IAM3系统角色权限<span class="parmvalue" id="parmvalue59251811183919"><a name="parmvalue59251811183919"></a><a name="parmvalue59251811183919"></a>“Security Administrator”</span>；非首次购买，需要授予IAM3系统策略权限<span class="parmvalue" id="parmvalue1219134192316"><a name="parmvalue1219134192316"></a><a name="parmvalue1219134192316"></a>“IAM ReadOnlyAccess”</span>或授予自定义权限。</li><li>需要增加VPC ReadOnlyAccess的系统策略，才能选择虚拟私有云、子网和安全组。</li><li>如果您选择的<span class="parmname" id="parmname644214431252"><a name="parmname644214431252"></a><a name="parmname644214431252"></a>“普通租户类”</span>，需要增加ECS ReadOnlyAccess的系统策略，才能选择ECS规格。</li><li>需要增加TMS ReadOnlyAccess的系统策略，才能查看预定义标签。</li></ul>
</td>
</tr>
<tr id="row56603226581"><td class="cellrowborder" valign="top" width="24.842484248424842%" headers="mcps1.2.4.1.1 "><p id="p0115242542"><a name="p0115242542"></a><a name="p0115242542"></a>购买WAF实例（专属云）</p>
</td>
<td class="cellrowborder" valign="top" width="22.712271227122713%" headers="mcps1.2.4.1.2 "><p id="p19115124217415"><a name="p19115124217415"></a><a name="p19115124217415"></a>云硬盘 EVS</p>
</td>
<td class="cellrowborder" valign="top" width="52.44524452445244%" headers="mcps1.2.4.1.3 "><p id="p3115142848"><a name="p3115142848"></a><a name="p3115142848"></a>需要增加EVS ReadOnlyAccess的系统策略，获取云硬盘资源的查询权限。</p>
</td>
</tr>
<tr id="row1225821273413"><td class="cellrowborder" valign="top" width="24.842484248424842%" headers="mcps1.2.4.1.1 "><p id="p10259512183414"><a name="p10259512183414"></a><a name="p10259512183414"></a>管理独享引擎</p>
</td>
<td class="cellrowborder" valign="top" width="22.712271227122713%" headers="mcps1.2.4.1.2 "><p id="p1259141233412"><a name="p1259141233412"></a><a name="p1259141233412"></a>网络控制台 VPC</p>
<p id="p12301520193510"><a name="p12301520193510"></a><a name="p12301520193510"></a>弹性公网IP EIP</p>
<p id="p0111315354"><a name="p0111315354"></a><a name="p0111315354"></a>弹性负载均衡 ELB</p>
</td>
<td class="cellrowborder" valign="top" width="52.44524452445244%" headers="mcps1.2.4.1.3 "><a name="ul34143141320"></a><a name="ul34143141320"></a><ul id="ul34143141320"><li>需要增加VPC ReadOnlyAccess的系统策略，才能查询虚拟私有云。</li><li>需要增加EIP ReadOnlyAccess的系统策略，才能查询独享引擎实例绑定的EIP。</li><li>需要增加ELB ReadOnlyAccess的系统策略，才能查询独享引擎实例绑定的ELB信息。</li></ul>
</td>
</tr>
<tr id="row1741953210331"><td class="cellrowborder" valign="top" width="24.842484248424842%" headers="mcps1.2.4.1.1 "><p id="p14192032123317"><a name="p14192032123317"></a><a name="p14192032123317"></a>添加防护网站（ELB模式）</p>
</td>
<td class="cellrowborder" valign="top" width="22.712271227122713%" headers="mcps1.2.4.1.2 "><p id="p17419143220331"><a name="p17419143220331"></a><a name="p17419143220331"></a>弹性负载均衡 ELB</p>
</td>
<td class="cellrowborder" valign="top" width="52.44524452445244%" headers="mcps1.2.4.1.3 "><p id="p57223711211"><a name="p57223711211"></a><a name="p57223711211"></a>需要增加ELB Administrator的系统角色，赋予IAM用户弹性负载均衡服务（ELB）管理员的角色，同时需要增加ELB FullAccess、ELB ReadOnlyAccess的权限，才能查询独享引擎实例绑定的ELB信息。</p>
</td>
</tr>
<tr id="row51001345111218"><td class="cellrowborder" valign="top" width="24.842484248424842%" headers="mcps1.2.4.1.1 "><p id="p510010454123"><a name="p510010454123"></a><a name="p510010454123"></a>实例组管理</p>
</td>
<td class="cellrowborder" valign="top" width="22.712271227122713%" headers="mcps1.2.4.1.2 "><p id="p1310034518122"><a name="p1310034518122"></a><a name="p1310034518122"></a>弹性负载均衡 ELB</p>
</td>
<td class="cellrowborder" valign="top" width="52.44524452445244%" headers="mcps1.2.4.1.3 "><p id="p710164517121"><a name="p710164517121"></a><a name="p710164517121"></a>需要增加ELB ReadOnlyAccess的系统策略，才能查询ELB实例组绑定的ELB信息。</p>
</td>
</tr>
<tr id="row1395692120515"><td class="cellrowborder" valign="top" width="24.842484248424842%" headers="mcps1.2.4.1.1 "><p id="p134181032173310"><a name="p134181032173310"></a><a name="p134181032173310"></a>添加防护网站（云模式、独享模式）</p>
</td>
<td class="cellrowborder" valign="top" width="22.712271227122713%" headers="mcps1.2.4.1.2 "><p id="p6418832103314"><a name="p6418832103314"></a><a name="p6418832103314"></a>云证书管理服务 CCM</p>
</td>
<td class="cellrowborder" rowspan="3" valign="top" width="52.44524452445244%" headers="mcps1.2.4.1.3 "><p id="p741814324334"><a name="p741814324334"></a><a name="p741814324334"></a>需要增加SCM ReadOnlyAccess系统策略，才能查询证书信息。</p>
</td>
</tr>
<tr id="row14419163214337"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1841913320339"><a name="p1841913320339"></a><a name="p1841913320339"></a>修改服务器信息</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1441953283311"><a name="p1441953283311"></a><a name="p1441953283311"></a>云证书管理服务 CCM</p>
</td>
</tr>
<tr id="row54190322336"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p641943263319"><a name="p641943263319"></a><a name="p641943263319"></a>网站设置列表</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p19419532203313"><a name="p19419532203313"></a><a name="p19419532203313"></a>云证书管理服务 CCM</p>
</td>
</tr>
<tr id="row154201032153319"><td class="cellrowborder" valign="top" width="24.842484248424842%" headers="mcps1.2.4.1.1 "><p id="p4420133293317"><a name="p4420133293317"></a><a name="p4420133293317"></a>告警通知</p>
</td>
<td class="cellrowborder" valign="top" width="22.712271227122713%" headers="mcps1.2.4.1.2 "><p id="p6420032113315"><a name="p6420032113315"></a><a name="p6420032113315"></a>消息通知服务 SMN</p>
</td>
<td class="cellrowborder" valign="top" width="52.44524452445244%" headers="mcps1.2.4.1.3 "><p id="p1442073253310"><a name="p1442073253310"></a><a name="p1442073253310"></a>需要增加SMN ReadOnlyAccess的系统策略，才能获取消息通知服务的主题群组。</p>
</td>
</tr>
<tr id="row142013243315"><td class="cellrowborder" valign="top" width="24.842484248424842%" headers="mcps1.2.4.1.1 "><p id="p17420832123311"><a name="p17420832123311"></a><a name="p17420832123311"></a>开启全量日志</p>
</td>
<td class="cellrowborder" valign="top" width="22.712271227122713%" headers="mcps1.2.4.1.2 "><p id="p13420103253313"><a name="p13420103253313"></a><a name="p13420103253313"></a>云日志服务 LTS</p>
</td>
<td class="cellrowborder" valign="top" width="52.44524452445244%" headers="mcps1.2.4.1.3 "><p id="p18420123233320"><a name="p18420123233320"></a><a name="p18420123233320"></a>需要增加LTS ReadOnlyAccess的系统策略，才能选择在云日志服务中创建的日志组和日志流名称。</p>
</td>
</tr>
</tbody>
</table>

