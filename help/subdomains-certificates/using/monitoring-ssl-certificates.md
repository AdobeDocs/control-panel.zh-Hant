---
title: 監視子域的SSL證書
description: 瞭解如何監控子網域的SSL憑證
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# 監視子域的SSL證書 {#monitoring-ssl-certificates}

## 關於SSL憑證 {#about-ssl-certificates}

Adobe Campaign建議您保護裝載著陸頁面的子網域，尤其是收集客戶敏感資訊的子網域。

**SSL(安全通訊端層** )加密可確保您委派給Adobe的子網域安全無虞。 當您的客戶填寫網頁表格或造訪Adobe Campaign代管的登陸頁面時，依預設會透過非安全通訊協定(HTTP)傳送資訊。 為確保額外的安全性，請使用HTTPS通訊協定來保護傳送的資訊。 例如，您的「http://info.mywebsite.com/」子網域位址現在會是「https://info.mywebsite.com/」。

**委派的子網域本身不會安裝SSL憑證**。 它們會安裝在相關的子網域上，主要是裝載著陸頁面、資源頁面等的子網域。

**SSL憑證會提供特定時段** （1年、60天等）。 一旦憑證過期，您在存取登陸頁面或使用子網域的資源時可能會遇到問題。 為避免此問題，「控制面板」可讓您監控子網域的SSL憑證，並啟動其續約程式。

![](assets/no_certificate.png)

## 監控SSL憑證 {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id=&quot;cp_subdomain_details&quot;
>title=&quot;子網域詳細資料&quot;
>abstract=&quot;擷取子網域的資訊。&quot;

在選擇子網域時，您的子網域SSL憑證狀態可直接從子網域清單中取 **[!UICONTROL Subdomains & Certificates]** 得。

子網域依SSL憑證的最近到期日排列，並提供過期的視覺化資訊（以天為單位）:

* **綠色**:子網域未在未來60天內到期的憑證。
* **橙色**:一或多個子網域有一個憑證，將在未來60天內到期。
* **紅色**:一或多個子網域有一個憑證，將在未來30天內到期。
* **灰色**:未為子域安裝任何證書。

![](assets/subdomains_list.png)

若要取得子網域的詳細資訊，請按一下 **[!UICONTROL Subdomain Details]** 按鈕。
會顯示所有相關子網域的清單。 它通常包含著陸頁面、資源頁面等的子網域。

該選 **[!UICONTROL Sender info]** 項卡提供有關已配置收件箱的資訊（發件人、回覆、錯誤電子郵件）。

![](assets/subdomain_details.png)

如果您的子網域的其中一個SSL憑證即將過期，您可以直接從「控制面板」續約。 如需更多相關資訊，請參閱本節：續 [約子網域的SSL憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)。

>[!IMPORTANT]
>
>Control Panel的憑證續約功能提供測試版，而且必須經常更新和修改，恕不另行通知。

**相關主題：**

* [新增SSL憑證（教學課程影片）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [續約子網域的SSL憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子網域品牌](../../subdomains-certificates/using/subdomains-branding.md)
