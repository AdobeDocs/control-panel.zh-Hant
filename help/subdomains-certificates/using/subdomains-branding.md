---
title: 子網域名稱
description: 進一步瞭解子網域名稱
translation-type: tm+mt
source-git-commit: 198c974d269289a6a9e5a87314662dba0bc85aff
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 91%

---


# 子網域名稱{#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="關於子網域和 SSL 憑證"
>abstract="監視您的子網域和相關聯的 SSL 憑證。"
>additional-url="https://docs.adobe.com/content/help/zh-Hant/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="如何監視子網域的 SSL 憑證"

>[!IMPORTANT]
>
>從「控制面板」委派子網域的功能會在測試版提供，且可能會不時更新和修改，恕不另行通知。

## 為什麼要設定子網域？{#why-setting-up-subdomains}

子網域是您網域的分區，可用來隔離您的名稱或各類流量 (交易訊息、行銷資訊等等)。

讓我們以「mybrand.com」網域為例，這是個用來傳送交易和行銷通訊的網域。在此情況下，您可以決定設定兩個子網域：

* 「Info.mybrand.com」子網域用來進行交易通訊 (購買確認函、密碼重設等等)；
* 「marketing.mybrand.com」子網域則用來傳送電子郵件給潛在客戶。

您可以藉此維護網域和其他子網域的信譽。例如，如果「marketing.mybrand.com」子網域因傳送能力不佳而被網際網路服務供應商新增至區塊清單中，則會阻止將整個「mybrand.com」網域和「info.mybrand.com」子網域新增至區塊清單。

## 子網域委派方法{#subdomain-delegation-methods}

子網域委派可讓您委派網域的子區域 (技術上稱為「DNS區域」)，以便與 Adobe Campaign 搭配使用。可用的設定方法有：

* **將子網域完全委派給 Adobe Campaign** (建議)：子網域已完全委派給 Adobe。Adobe 可以控制並維護傳遞、演算及追蹤電子郵件促銷活動所需的 DNS 的各個層面，以受管理的方式提供 Campaign。

* **使用 CNAME** (不建議使用，也不支援透過「控制面板」使用)：建立子網域並使用 CNAME 指向 Adobe 特定記錄。若使用此設定，Adobe 和客戶都有責任維護 DNS。

下表提供這些方法的運作方式摘要，以及所需投入的精力：

| 委派方法 | 運作方式 | 所需投入的精力 |
|---|---|---|
| **完全委派** | 建立子網域和命名空間記錄。Adobe 便會設定 Adobe Campaign 所需的所有 DNS 記錄。<br/><br/>在此設定中，Adobe 會完全負責管理子網域和所有 DNS 記錄。 | 低 |
| **CNAME，自訂方法** | 建立子網域和命名空間記錄。Adobe 便會提供要放置在 DNS 伺服器中的記錄，並在 Adobe Campaign DNS 伺服器中設定對應的值。<br/><br/>在此設定中，您和 Adobe 都有責任維護 DNS。 | 高 |

如需網域委派的其他資訊，請參閱[本文件](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。

如果您對子網域委派方法有任何疑問，請聯絡 Adobe Deliverability 團隊，或最終聯絡客戶服務以要求獲得傳遞能力的諮詢。

**相關主題：**

* [設定新子網域](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [委派子網域 (教學課程影片)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [監視子網域](../../subdomains-certificates/using/monitoring-subdomains.md)
