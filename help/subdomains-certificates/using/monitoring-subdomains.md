---
product: campaign
solution: Campaign
title: 監視子網域
description: 監視子網域，確保全部都已正確設定為與 Adobe Campaign 搭配使用。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
TQID: https://experienceleague.adobe.com/49fMBOZ2iN7xs7PpnYRLDHpQO5eXMTvn-veAxpjeH7w
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 06babfad697fb874f2b77c5204e30580c55cd0d1
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 77%

---

# 監視您的子網域 {#monitoring-subdomains}

務必要監視子網域，以確保全部皆已正確設定為與 Adobe Campaign 搭配使用。

選取&#x200B;**[!UICONTROL 子網域和憑證]**&#x200B;卡片時，可直接存取每個生產執行個體的子網域清單。

**[!UICONTROL 上次驗證]**&#x200B;欄指出上次驗證子網域的時間。 您可以隨時按一下 **...** / **[!UICONTROL 驗證子網域]**&#x200B;按鈕來啟動驗證。

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe 不建議使用沒有憑證日期的子網域，因為這可能表示這些子網域可能有一些傳遞能力問題。

啟動驗證時，會執行數個操作來檢查子網域是否已正確設定（例項租使用者檢查、電子郵件傳送測試等） 如果子網域驗證失敗，請聯絡Adobe客戶服務以進一步調查。

**相關主題：**

* [續約子網域的 SSL 憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子網域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
