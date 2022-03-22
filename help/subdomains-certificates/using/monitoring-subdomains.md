---
product: campaign
solution: Campaign
title: 監視子網域
description: 監視子域，以確保所有子域都配置正確以與Adobe Campaign協作。
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: fa45ec38ff06a0b02ab724e7ced79b7b5de2c766
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---

# 監視子網域 {#monitoring-subdomains}

監控子域是非常重要的，以確保所有子域都配置正確以與Adobe Campaign協作。

在選擇 **[!UICONTROL Subdomains & Certificates]** 卡。

的 **[!UICONTROL Last verification]** 列指示上次驗證子域的時間。 您可以通過按一下 **...** / **[!UICONTROL Verify subdomain]** 按鈕

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建議使用沒有證書日期的子域，因為這可能意味著這些子域可能存在某些可傳遞性問題。

啟動驗證時，會執行若干操作以檢查子域是否配置正確(實例租戶檢查、電子郵件發送test等)

如果子域的驗證失敗，請與Adobe客戶服務部聯繫以進一步調查。

**相關主題：**

* [續約子網域的 SSL 憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子網域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
