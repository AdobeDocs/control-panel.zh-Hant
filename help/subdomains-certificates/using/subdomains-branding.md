---
title: 子網域品牌
description: 進一步瞭解子網域品牌
translation-type: tm+mt
source-git-commit: 762c445713e6e728fc1a45d5fcf8c9c1cb0dcdf6

---


# 子網域品牌 {#subdomains-branding}

>[!IMPORTANT]
>
>在1月底之前，控制面板的子網域委派將提供測試版，並在不另行通知的情況下，經常進行更新和修改。

## 為什麼要設定子網域？ {#why-setting-up-subdomains}

子網域是您網域的劃分，可用來隔離您的品牌或各種類型的流量（交易訊息、行銷資訊等）。

讓我們以&quot;mybrand.com&quot;網域為例，該網域用於傳送交易和行銷通訊。 在這種情況下，您可以決定設定兩個子網域：

* 「info.mybrand.com」子網域供您進行交易通訊（購買確認、密碼重設等）、
* 「marketing.mybrand.com」子網域，供您發掘潛在客戶的電子郵件。

如此，您將有助於維護網域和其他子網域的信譽。 例如，如果「marketing.mybrand.com」子網域因傳送能力不佳而被網際網路服務供應商列入黑名單，將會阻止整個「mybrand.com」網域和「info.mybrand.com」子網域被列入黑名單。

## 子網域委派方法 {#subdomain-delegation-methods}

子網域委派可讓您委派網域的子區域（技術上為「DNS區域」），以便與Adobe Campaign搭配使用。 可用的設定方法有：

* **完整的子網域委派給Adobe Campaign** （建議）:子網域已完全委派給Adobe。 Adobe能夠控制並維護傳送、轉譯及追蹤電子郵件宣傳所需的DNS的所有方面，以受管理的方式提供宣傳。

* **使用CNAME** （不建議使用，也不支援透過「控制面板」使用）:建立子網域並使用CNAME指向Adobe特定記錄。 使用此設定，Adobe和客戶都有維護DNS的責任。

下表提供這些方法的運作方式摘要，以及隱含的努力程度：

| 委派方法 | 運作方式 | 努力程度 |
|---|---|---|
| **完全委派** | 建立子域和命名空間記錄。 然後Adobe將設定Adobe Campaign所需的所有DNS記錄。<br/><br/>在此設定中，Adobe完全負責管理子網域和所有DNS記錄。 | 低 |
| **CNAME，自訂方法** | 建立子域和命名空間記錄。 然後Adobe會提供要放在DNS伺服器中的記錄，並在Adobe Campaign DNS伺服器中設定對應的值。<br/><br/>在此設定中，您和Adobe都有維護DNS的責任。 | 高 |

有關域委派的其他資訊，請參見 [本文檔](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。

如果您對子網域委派方法有任何疑問，請洽詢Adobe Deliverability團隊，或最終聯絡客戶服務以要求Deliverability諮詢。

**相關主題：**

* [設定新子網域](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [委派子網域（教學課程影片）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [監控子網域](../../subdomains-certificates/using/monitoring-subdomains.md)
