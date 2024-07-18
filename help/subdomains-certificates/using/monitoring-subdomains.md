---
product: campaign
solution: Campaign
title: 監視子網域
description: 監視子網域，確保全部都已正確設定為與 Adobe Campaign 搭配使用。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 100%

---


# 監視您的子網域 {#monitoring-subdomains}

務必要監視子網域，以確保全部皆已正確設定為與 Adobe Campaign 搭配使用。

選取&#x200B;**[!UICONTROL 子網域和憑證]**&#x200B;卡片時，可直接存取每個生產執行個體的子網域清單。

**[!UICONTROL 上次驗證]**&#x200B;欄指出上次驗證子網域的時間。 您可以隨時按一下 **...** / **[!UICONTROL 驗證子網域]**&#x200B;按鈕來啟動驗證。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe 不建議使用沒有憑證日期的子網域，因為這可能表示這些子網域可能有一些傳遞能力問題。

啟動驗證時，系統會執行數個作業來檢查是否已正確設定子網域 (執行個體租用戶檢查、電子郵件傳送測試等) 如果子網域的驗證失敗，請聯絡 Adobe 客戶服務以進一步調查。

**相關主題：**

* [續約子網域的 SSL 憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子網域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
