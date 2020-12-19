---
product: campaign
solution: Campaign
title: 子網域名稱
description: 進一步瞭解子網域名稱
translation-type: tm+mt
source-git-commit: 2d84a5ebe8dbf42264c94f882a51180aae2a58a6
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# 子網域名稱{#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="關於子網域和 SSL 憑證"
>abstract="監視您的子網域和相關聯的 SSL 憑證。"
>additional-url="https://docs.adobe.com/content/help/zh-Hant/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="如何監視子網域的 SSL 憑證"

## 為什麼要設定子網域？{#why-setting-up-subdomains}

>[!IMPORTANT]
>
>「控制面板」的子網域設定提供測試版，而且必須經常更新和修改，恕不另行通知。

子網域是您網域的分區，可用來隔離您的名稱或各類流量（交易訊息、行銷資訊等等）。

讓我們以「mybrand.com」網域為例，這是個用來傳送交易和行銷通訊的網域。在此情況下，您可以決定設定兩個子網域：

* 「Info.mybrand.com」子網域用來進行交易通訊（購買確認函、密碼重設等等）；
* 「marketing.mybrand.com」子網域則用來傳送電子郵件給潛在客戶。

您可以藉此維護網域和其他子網域的信譽。舉例來說，如果「marketing.mybrand.com」子網域因傳遞能力不佳，而被網際網路服務提供者新增至封鎖清單，如此就能防止整個「mybrand.com」網域和「info.mybrand.com」子網域被新增至封鎖清單。

## 子網域配置方法{#subdomain-delegation-methods}

子網域設定可讓您設定網域的子區段（技術上為「DNS區域」），以便與Adobe Campaign搭配使用。 可用的設定方法有：

* **將子網域完全委派給 Adobe Campaign**（建議）：子網域已完全委派給 Adobe。Adobe 可以控制並維護傳遞、演算及追蹤電子郵件行銷活動所需的 DNS 的各個層面，以受管理的方式提供 Campaign。

* **CNAME的使用**:建立子網域並使用CNAME指向Adobe特定記錄。若使用此設定，Adobe 和客戶都有責任維護 DNS。

下表提供這些方法的運作方式摘要，以及所需投入的精力：

| 配置方法 | 運作方式 | 所需投入的精力 |
|---|---|---|
| **完全委派** | 建立子網域和命名空間記錄。Adobe 便會設定 Adobe Campaign 所需的所有 DNS 記錄。<br/><br/>在此設定中，Adobe 會完全負責管理子網域和所有 DNS 記錄。 | 低 |
| **CNAME，自訂方法** | 建立子網域和命名空間記錄。Adobe 便會提供要放置在 DNS 伺服器中的記錄，並在 Adobe Campaign DNS 伺服器中設定對應的值。<br/><br/>在此設定中，您和 Adobe 都有責任維護 DNS。 | 高 |

有關域配置的其他資訊，請參見本文檔](https://helpx.adobe.com/tw/campaign/kb/domain-name-delegation.html)。[

如果您對子網域配置方法有任何疑問，請聯絡Adobe Deliverability團隊，或最終聯絡客戶服務以要求提供性諮詢。

## 子網域的使用案例(Campaign Classic){#subdomains-use-cases}

為Campaign Classic實例設定子域時，需要選擇將使用子域的使用案例（請參閱[設定新子域](../../subdomains-certificates/using/setting-up-new-subdomain.md)）。

可能的使用案例包括：

* **行銷通訊**：用於商業目的的通訊。範例：銷售電子行銷活動。

* **交易與營運通訊**：交易通訊包含的資訊旨在完成收件者與您開展的流程。範例：購買確認函、密碼重設電子郵件。組織通訊與組織內外的資訊、構思和意見交換有關，並無任何商業目的。

**根據使用案例劃分子網域是傳遞能力的最佳實務**。如此一來，就能分隔和保護每個子網域的信譽。舉例來說，如果行銷通訊的子網域最後被網際網路服務提供者新增至封鎖清單，您的交易通訊子網域將不會受到影響，而且會繼續傳送通訊。

**您可以為行銷和交易使用案例設定子網域**:

* 若是行銷使用案例，子網域將會設定在 **MID** (Mid sourcing) 執行個體上。
* 若是交易使用案例，子網域將會設定在 ALL **RT** (Message Center/即時傳送訊息) 執行個體上，以確保連線能力。因此，子網域將會搭配您所有 RT 執行個體一起運作。

>[!NOTE]
>
>如果您使用 Campaign Classic，「控制面板」可讓您查看哪些 RT/MID 執行個體已連線至您正在使用的行執行個體。有關詳情，請參閱[執行個體詳細資訊](../../instances-settings/using/instance-details.md)區段。

**相關主題：**

* [設定新子網域](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [監視子網域](../../subdomains-certificates/using/monitoring-subdomains.md)
