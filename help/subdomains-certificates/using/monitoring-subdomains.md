---
product: campaign
solution: Campaign
title: 監視子網域的 SSL 憑證
description: 瞭解如何監視子網域的 SSL 憑證
feature: 控制面板
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 3bd3dcc0e09d887cab7d810d43f2c72bb4251ac9
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 17%

---

# 監視子網域 {#monitoring-subdomains}

>[!AVAILABILITY]
>
>此功能不適用於Campaign v8。

您必須監控子網域，以確保所有項目皆已正確設定，可搭配Adobe Campaign使用。

選取&#x200B;**[!UICONTROL Subdomains & Certificates]**&#x200B;卡片時，可直接存取每個生產執行個體的子網域清單。

**[!UICONTROL Last verification]**&#x200B;欄會指出上次驗證子網域的時間。 您可以隨時按一下&#x200B;**啟動驗證……** / **[!UICONTROL Verify subdomain]**&#x200B;按鈕。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建議使用沒有憑證日期的子網域，因為這可能表示這些子網域可能有某些傳遞能力問題。

啟動驗證時，會執行數個操作以檢查子網域是否已正確設定（例項租用戶檢查、電子郵件傳送測試等）

如果子網域的驗證失敗，請連絡Adobe客戶服務以進行進一步調查。

**相關主題：**

* [續約子網域的 SSL 憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子網域名稱](../../subdomains-certificates/using/subdomains-branding.md)
