---
product: campaign
solution: Campaign
title: 監視子網域的 SSL 憑證
description: 瞭解如何監視子網域的 SSL 憑證
feature: Control Panel
role: Architect
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: 46a4e13e8017c5406dcd65f21c9839374dd44aa7
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 91%

---

# 監視子網域的 SSL 憑證 {#monitoring-ssl-certificates}

## 關於 SSL 憑證 {#about-ssl-certificates}

Adobe Campaign 建議您保護託管登陸頁面之子網域的安全，尤其是收集客戶敏感資訊的子網域。

**SSL（安全套接字層）加密** 確保您設定為搭配Adobe運作的子網域安全無虞。 當您的客戶填寫網頁表格或造訪 Adobe Campaign 託管的登陸頁面時，系統會依預設透過非安全通訊協定 (HTTP) 傳送資訊。為確保多一層安全性，請使用 HTTPS 通訊協定來保護傳送的資訊。舉例來說，您的「http://info.mywebsite.com/」子網域位址現在會成為「https://info.mywebsite.com/」。

**已設定的子網域本身並未安裝SSL憑證**. 它們會安裝在相關聯的子網域上，主要是託管登陸頁面、資源頁面等子網域。

**在特定時間內提供 SSL 憑證** (1年、60 天等等)。憑證過期後，您在存取登陸頁面或使用子網域的資源時，就可能會遇到問題。為避免出現此問題，「控制面板」可讓您監視子網域的 SSL 憑證，並啟動其續約流程。

![](assets/no_certificate.png)

## 監視 SSL 憑證 {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="子網域詳細資訊"
>abstract="擷取子網域SSL憑證的相關資訊。"

選取「**[!UICONTROL Subdomains & Certificates]**」卡片時，您可以直接從子網域清單中取得子網域 SSL 憑證的狀態。

子網域會依 SSL 憑證的最近到期日排序，並提供過期的視覺化資訊 (以天為單位)：

* **綠色**：子網域在未來 60 天內沒有到期的憑證。
* **橙色**：一或多個子網域有一個會在未來 60 天內到期的憑證。
* **紅色**：一或多個子網域有一個會在未來 30 天內到期的憑證
* **灰色**：未為子網域安裝任何憑證。

![](assets/subdomains_list.png)

若要取得子網域的詳細資訊，請按一下&#x200B;**[!UICONTROL Subdomain Details]**按鈕。
隨即顯示所有相關子網域的清單。這通常會包括登陸頁面、資源頁面等等的子網域。

「**[!UICONTROL Sender info]**」標籤提供有關已設定收件匣的資訊 (寄件人、回覆、錯誤電子郵件)。

![](assets/subdomain_details.png)

如果子網域的其中一個 SSL 憑證即將到期，您可以直接從「控制面板」續約。如需更多資訊，請參閱本節：[續約子網域的 SSL 憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)。

>[!IMPORTANT]
>
>從「控制面板」續約憑證的功能會在測試版提供，且可能會不時更新和修改，恕不另行通知。

**相關主題：**

* [續約子網域的 SSL 憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [子網域名稱](../../subdomains-certificates/using/subdomains-branding.md)
