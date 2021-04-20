---
product: campaign
solution: Campaign
title: 監視子網域的 SSL 憑證
description: 瞭解如何監視子網域的 SSL 憑證
feature: Control Panel
role: Architect
level: Experienced
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 17%

---


# 監視子網域 {#monitoring-subdomains}

必須監控子網域，以確保所有子網域都已正確設定，以便與Adobe Campaign搭配運作。

選取&#x200B;**[!UICONTROL Subdomains & Certificates]**&#x200B;卡片時，可直接存取每個生產例項的子網域清單。

**[!UICONTROL Last verification]**&#x200B;欄會指出上次驗證子網域的時間。 您可以隨時按一下&#x200B;**啟動驗證……** / **[!UICONTROL Verify subdomain]**&#x200B;按鈕。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建議使用沒有憑證日期的子網域，因為這可能表示這些子網域可能有某些傳送性問題。

啟動驗證時，會執行數個操作以檢查子網域的設定是否正確（例項租用戶檢查、電子郵件傳送測試等）

如果子網域的驗證失敗，請聯絡Adobe客戶服務以進一步調查。

**相關主題：**

* [續約子網域的 SSL 憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子網域名稱](../../subdomains-certificates/using/subdomains-branding.md)
