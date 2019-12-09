---
title: 監視子域的SSL證書
description: 瞭解如何監控子網域的SSL憑證
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# 監視子域的SSL證書 {#monitoring-ssl-certificates}

Adobe Campaign建議您保護裝載著陸頁面的子網域，尤其是收集客戶敏感資訊的子網域。

**SSL(安全通訊端層** )加密可確保您委派給Adobe的子網域安全無虞。 當您的客戶填寫網頁表格或造訪Adobe Campaign代管的登陸頁面時，依預設會透過非安全通訊協定(HTTP)傳送資訊。 為確保額外的安全性，請使用HTTPS通訊協定來保護傳送的資訊。 例如，您的「http://info.mywebsite.com/」子網域位址現在會是「https://info.mywebsite.com/」。

**委派的子網域本身不會安裝SSL憑證**。 它們會安裝在相關的子網域上，主要是裝載著陸頁面、資源頁面等的子網域。

**SSL憑證會提供特定時段** （1年、60天等）。 一旦憑證過期，您在存取登陸頁面或使用子網域的資源時可能會遇到問題。 為避免此問題，「控制面板」可讓您監控子網域的SSL憑證，並啟動其續約程式。

有關子域委託的詳細資訊，請 [參閱](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。

此 **[!UICONTROL Subdomains and Certificates]**卡可讓您查看您的登陸頁面和資源所在的子網域和相關子網域，以及安裝了SSL憑證的子網域。

您也可以輕鬆查看哪些子網域有過期的憑證，並視需要續約。

>[!NOTE]
>
>Adobe 建議您在相關子網域的 SSL 憑證&#x200B;**接近到期日時**&#x200B;進行更新。根據您的組織而定，憑證更新可能需要數天的時間，我們建議您為此程序分配適當的時間。
<!-- note to remove? immediate, no more delay? -->

選取資訊卡時，可直接存取每個例項的子網域清 **[!UICONTROL Subdomains & Certificates]**單。

子網域依SSL憑證的最近到期日排列，並提供過期的視覺化資訊（以天為單位）:

* **綠色**:子網域未在未來60天內到期的憑證。
* **橙色**:一或多個子網域有一個憑證，將在未來60天內到期。
* **紅色**:一或多個子網域有一個憑證，將在未來30天內到期。

![](assets/visual_alert2.png)

To get more details on a subdomain&#39;s certificates, click the **[!UICONTROL Certificate Details]**button.

![](assets/certificate_details4.png)

所有相關子網域的清單都會顯示在其憑證上。 它通常包含著陸頁面、資源頁面等的子網域。

![](assets/monitoring_subdomains_details2.png)
