---
product: campaign
solution: Campaign
title: 子網域名稱
description: 進一步瞭解子網域名稱
feature: Control Panel
role: Architect
level: Intermediate
exl-id: a489d051-fb95-45cf-bb6d-33aef10b7795
source-git-commit: f1f6388bd32927cb13359f8975748ca4a158e660
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 75%

---

# 子網域品牌化 {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="關於子網域和 SSL 憑證"
>abstract="監視您的子網域和相關聯的 SSL 憑證。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=zh-Hant" text="監視 SSL 憑證"

## 為什麼要設定子網域？ {#why-setting-up-subdomains}

子網域是您網域的分區，可用來隔離您的名稱或各類流量（交易訊息、行銷資訊等等）。

讓我們以「mybrand.com」網域為例，這是個用來傳送交易和行銷通訊的網域。在此情況下，您可以決定設定兩個子網域：

* 「Info.mybrand.com」子網域用來進行交易通訊（購買確認函、密碼重設等等）；
* 「marketing.mybrand.com」子網域則用來傳送電子郵件給潛在客戶。

您可以藉此維護網域和其他子網域的信譽。舉例來說，如果「marketing.mybrand.com」子網域因傳遞能力不佳，而被網際網路服務提供者新增至封鎖清單，如此就能防止整個「mybrand.com」網域和「info.mybrand.com」子網域被新增至封鎖清單。

## 子域配置方法 {#subdomain-delegation-methods}

子域配置允許您配置域的子部分（技術上是「DNS區域」），以便與Adobe Campaign配合使用。 可用的設定方法有：

* **將子網域完全委派給 Adobe Campaign**（建議）：子網域已完全委派給 Adobe。Adobe 可以控制並維護傳遞、演算及追蹤電子郵件行銷活動所需的 DNS 的各個層面，以受管理的方式提供 Campaign。

* **CNAME的使用**:建立子域並使用CNAME指向特定於Adobe的記錄。 若使用此設定，Adobe 和客戶都有責任維護 DNS。

下表提供這些方法的運作方式摘要，以及所需投入的精力：

| 配置方法 | 運作方式 | 所需投入的精力 |
|---|---|---|
| **完全委派** | 建立子網域和命名空間記錄。Adobe 便會設定 Adobe Campaign 所需的所有 DNS 記錄。<br/><br/>在此設定中，Adobe 會完全負責管理子網域和所有 DNS 記錄。 | 低 |
| **CNAME，自訂方法** | 建立子網域和命名空間記錄。Adobe 便會提供要放置在 DNS 伺服器中的記錄，並在 Adobe Campaign DNS 伺服器中設定對應的值。<br/><br/>在此設定中，您和 Adobe 都有責任維護 DNS。 | 高 |

有關域配置的其他資訊，請參見 [本文檔](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html)。

如果您對子域配置方法有任何疑問，請聯繫Adobe交付能力團隊，或最終聯繫客戶服務部門以請求交付能力咨詢。

## 子域的使用案例（市場活動v7/v8）{#subdomains-use-cases}

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_usecase_selection"
>title="選擇子域的使用案例"
>abstract="通過使用案例拆分子域是提供能力的最佳做法。 如此一來，就能分隔和保護每個子網域的信譽。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=zh-Hant" text="設定新的子網域"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=zh-Hant" text="子網域品牌化"

為市場活動v7/v8實例設定子域時，需要選擇子域將用於的使用案例(請參閱 [設定新子域](../../subdomains-certificates/using/setting-up-new-subdomain.md))。

可能的使用案例包括：

* **行銷通訊**：用於商業目的的通訊。範例：銷售電子行銷活動。

* **交易與營運通訊**：交易通訊包含的資訊旨在完成收件者與您開展的流程。範例：購買確認函、密碼重設電子郵件。組織通訊與組織內外的資訊、構思和意見交換有關，並無任何商業目的。

**根據使用案例劃分子網域是傳遞能力的最佳實務**。如此一來，就能分隔和保護每個子網域的信譽。舉例來說，如果行銷通訊的子網域最後被網際網路服務提供者新增至封鎖清單，您的交易通訊子網域將不會受到影響，而且會繼續傳送通訊。

**您可以為市場營銷和事務性使用案例配置子域**:

* 若是行銷使用案例，子網域將會設定在 **MID** (Mid sourcing) 執行個體上。
* 若是交易使用案例，子網域將會設定在 ALL **RT** (Message Center/即時傳送訊息) 執行個體上，以確保連線能力。因此，子網域將會搭配您所有 RT 執行個體一起運作。

>[!NOTE]
>
>如果您正在使用「市場活動v7/v8」，則「控制面板」允許您查看哪些RT/MID實例連接到您正在使用的「市場營銷」實例。 有關詳情，請參閱[執行個體詳細資訊](../../instances-settings/using/instance-details.md)區段。

**相關主題：**

* [設定新的子網域](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [監視子網域](../../subdomains-certificates/using/monitoring-subdomains.md)
