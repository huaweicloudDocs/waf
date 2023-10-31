# 开启HTTP2协议<a name="waf_01_1170"></a>

如果您的网站需要支持HTTP2协议的访问，可参考本章节开启HTTP2协议。HTTP2协议仅适用于客户端到WAF之间的访问，且“对外协议“必须包含HTTPS才能支持使用。

## 前提条件<a name="section7637101713317"></a>

-   已添加防护网站。
-   配置的“对外协议“包含HTTPS。

## 约束条件<a name="section115301864413"></a>

-   防护网站的部署模式为“云模式“。
-   仅专业版和铂金版支持HTTP2协议。
-   支持HTTP/2协议防护的区域，请参考[功能总览](https://support.huaweicloud.com/function-waf/index.html#)。

## 操作步骤<a name="section1994128112518"></a>

1.  [登录管理控制台](https://console.huaweicloud.com/?locale=zh-cn)。
2.  单击管理控制台左上角的![](figures/icon-region-26.jpg)，选择区域或项目。
3.  单击页面左上方的![](figures/icon-Service-38.png)，选择“安全与合规  \>  Web应用防火墙 WAF“。
4.  在左侧导航树中，选择“网站设置“，进入“网站设置“页面。
5.  在目标网站所在行的“域名“列中，单击目标网站，进入网站基本信息页面。
6.  在“是否使用HTTP2协议“所在行，单击![](figures/icon-edit-85.jpg)，选择“是“并单击“确定“。

