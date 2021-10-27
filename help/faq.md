---
product: campaign
solution: Campaign
title: 「控制面板」常見問答集
description: 與「控制面板」相關的常見問題
feature: Control Panel
role: Architect
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: 47a57b38e9af8b03d277bf9ee6922b19f0298944
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 常見問題集 {#faq}

## 控制面板 {#control-panel}

### 什麼是「控制面板」？

「控制面板」可讓產品管理員直接管理各種設定，並監視連線至 Adobe Campaign 的 SFTP 伺服器容量。

### 「控制面板」目前有哪些功能？

「控制面板」可讓您追蹤儲存情形、將 IP 新增至允許清單，以及根據您的需求自行管理 SFTP 的 SSH 金鑰並執行其他動作。

有關詳細資訊，請參閱「控制面板」支援的動作文件。

### 是否有些功能尚未在Campaign v8上支援，但在Campaign Classicv7上可用{#v8-restrictions}

否. 現在，Campaign Classicv7上可用的所有功能也可透過Campaign v8的「控制面板」來支援，包括子網域和憑證管理相關功能。

### 「控制面板」是否只適用於 Adobe Campaign？

是的，您只能在「控制面板」中管理 Adobe Campaign 的設定。

### 我可以使用「控制面板」嗎？

「控制面板」僅開放給將 Adobe Campaign 託管在 AWS 上之現有客戶的產品管理員。請注意，我們目前並不支援混合環境。

如果您不是管理員，但想要取得存取權限，請聯絡您的產品管理員，並協助將您新增為管理員。

### 身為 Campaign Classic v7 使用者，存取「控制面板」的條件為何？ {#v7-restrictions}

控制面板僅限管理員使用者存取。[深入瞭解](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=zh-Hant#discover-control-panel)。

請注意，就 Campaign Classic v7 而言，您的執行個體必須託管至 Amazon Web Services (AWS)，並升級至最新的 [Campaign GA](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=zh-Hant#rn-statuses) 版本。於[本節](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=zh-Hant#getting-your-campaign-version)中瞭解如何確認您的 Campaign Classic 版本。若要檢查您的 Campaign Classic 執行個體是否託管至 AWS，請依照 [本節](#hosted-aws)詳述步驟操作。

### 如何存取「控制面板」？

請依照「存取控制面板」文件中的詳細指示操作。

### 使用「控制面板」是否需要額外付費？

否。如果您是 Adobe Campaign 的現有客戶，則無須額外付費。

## IMS 組織 ID {#ims-org-id}

### 什麼是 IMS 組織 ID？

這是您第一次登入 Adobe Experience Cloud 時，針對您的執行個體提供的唯一 ID，其格式應為：xxx@AdobeOrg。

如需詳細資訊，請參閱 [Adobe Experience Cloud 文件](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=zh-Hant)。

### 我可以在哪裡找到我的 IMS 組織 ID？

一種方式是導覽至[「Adobe Experience Cloud 首頁](https://experiencecloud.adobe.com/) >**[!UICONTROL Administration]**」。您會在「管理人員&#x200B;**[!UICONTROL Quick Access]**」區段的底部找到您的 IMS 組織 ID。您可在 [Adobe Experience Cloud 文件](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html)中找到更多詳細資訊。

另一種方式是啟動 **Admin Console**。您的 IMS 組織 ID 將會顯示在您的 URL 中，看起來會像這樣：https://adminconsole.adobe.com/xxx@AdobeOrg/overview。

### 為什麼我需要知道我的 IMS 組織 ID?

為了方便您管理執行個體的設定，我們希望確保您為您的公司使用多個執行個體時，能針對正確的執行個體獲得正確資訊。

### 如果我有多個 IMS 組織 ID，該怎麼辦？

如果您擁有多個 Adobe 解決方案的存取權限，您可能會有超過一個 IMS 組織 ID。在此情況下，您在 Adobe Campaign 執行個體下看到的 IMS 組織 ID 就是您應使用的正確 ID。

>[!NOTE]
>
>如果您的 Adobe Campaign 和 Adobe Analytics 擁有相同的 IMS 組織 ID，這是最理想的情況。如果您打算整合解決方案，以善用購物車放棄（針對 AA + AC）等複雜的使用案例，Analytics 和 Campaign 之間便需要共用同一個 IMS 組織 ID。
>
>如果您的 Adobe Campaign 和 Adobe Analytics 擁有不同的 IMS 組織 ID，請聯絡客戶服務進行整合。

### 我如何得知我的 Adobe Campaign 執行個體是否託管在 AWS 上？{#hosted-aws}

要檢查您的執行個體是否托管在 AWS 上，請執行下列步驟：

1. 擷取您的登入 URL。這是您用來登入 Campaign 執行個體的 URL，通常會以「.campaign.adobe.com」或「.neolane.net」為結尾。
1. 開啟終端機，然後對您的登入 URL 執行 **[!DNL nslookup]**&#x200B;操作。

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. 回應會傳回您執行個體的資訊。

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. 對傳回 IP 位址執行 **nslookup** 操作。

   `doe-macOS% nslookup 12.34.567.89`

1. 在傳回的結果中檢查「name」值。如果結果包含「amazonaws.com」，表示您的執行個體託管在 AWS 上。

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>如果您想要移轉到 AWS，請聯絡您的客戶成功經理以展開程序。
