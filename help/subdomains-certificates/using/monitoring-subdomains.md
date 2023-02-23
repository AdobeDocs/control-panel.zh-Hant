---
product: campaign
solution: Campaign
title: 監視子網域
description: 監視您的子網域，以確保所有項目皆已正確設定，可搭配Adobe Campaign使用。
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: f0c3df4727e89e3f6127fe4563908b955ccb820c
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 7%

---

# 監視子網域 {#monitoring-subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="移除子網域委派"
>abstract="此畫面可讓您移除要Adobe的子網域委派。 請記住，提交後，此程式無法還原或停止。<br><br>如果您嘗試移除所選執行個體之主要網域的委派，系統會要求您選擇要取代它的網域。"

您必須監控子網域，以確保所有項目皆已正確設定，可搭配Adobe Campaign使用。

選取 **[!UICONTROL Subdomains & Certificates]** 卡片。

此 **[!UICONTROL Last verification]** 欄會指出上次驗證子網域的時間。 您可以隨時按一下 **...** / **[!UICONTROL Verify subdomain]** 按鈕。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe不建議使用沒有憑證日期的子網域，因為這可能表示這些子網域可能有某些傳遞能力問題。

啟動驗證時，會執行數個操作以檢查子網域是否已正確設定（例項租用戶檢查、電子郵件傳送測試等）

如果子網域的驗證失敗，請連絡Adobe客戶服務以進行進一步調查。

**相關主題：**

* [續約子網域的 SSL 憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子網域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
