---
product: campaign
solution: Campaign
title: 監視子網域
description: 監視您的子網域，確保所有子網域都已正確設定為搭配Adobe Campaign使用。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---


# 監視您的子網域 {#monitoring-subdomains}

監視子網域十分重要，以確保所有子網域皆已正確設定為可與Adobe Campaign搭配使用。

選取「 」時，可直接存取每個生產執行個體的子網域清單 **[!UICONTROL Subdomains & Certificates]** 卡片。

此 **[!UICONTROL Last verification]** 欄指出上次驗證子網域的時間。 您可以隨時按一下 **...** / **[!UICONTROL Verify subdomain]** 按鈕。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建議使用沒有憑證日期的子網域，因為這可能表示這些子網域可能有一些傳遞問題。

啟動驗證時，會執行數個操作來檢查子網域是否已正確設定（例項租使用者檢查、電子郵件傳送測試等） 如果子網域驗證失敗，請聯絡Adobe客戶服務以進一步調查。

**相關主題：**

* [續約子網域的 SSL 憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子網域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
