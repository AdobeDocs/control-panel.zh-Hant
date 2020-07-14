---
title: 「控制面板」常見問答集
description: 與「控制面板」相關的常見問題
translation-type: tm+mt
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 71%

---


# 常見問答集{#faq}

## IMS組織ID {#ims-org-id}

**什麼是IMS組織ID?**

這是您第一次登入 Adobe Experience Cloud 時，針對您的執行個體提供的唯一 ID，其格式應為：xxx@AdobeOrg。

如需詳細資訊，請參閱 [Adobe Experience Cloud 文件](https://marketing.adobe.com/resources/help/zh_TW/mcloud/organizations.html)。

**我可以在哪裡找到我的IMS組織ID?**

一種方式是導覽至[「Adobe Experience Cloud 首頁](https://experiencecloud.adobe.com/) >**[!UICONTROL Administration]**」。You will find your IMS Organization ID at the bottom of Administration **[!UICONTROL Quick Access]** section. 您可在 [Adobe Experience Cloud 文件](https://marketing.adobe.com/resources/help/zh_TW/mcloud/organizations.html)中找到更多詳細資訊。

另一種方式是啟動 **Admin Console**。您的IMS組織ID會顯示在您的URL中，其外觀應類似： https://adminconsole.adobe.com/xxx@AdobeOrg/overview。

**我為何需要知道我的IMS組織ID?**

為了方便您管理執行個體的設定，我們希望確保您對公司使用多個執行個體時，能針對正確的執行個體獲得正確的資訊。

**如果我有多個IMS組織ID該怎麼辦？**

如果您擁有多個Adobe解決方案的存取權，可能會有多個IMS組織ID。 在此情況下，您應使用的正確IMS組織ID是您在Adobe Campaign例項下看到的IMS組織ID。

>[!NOTE]
>
>如果您有相同的Adobe Campaign和Adobe Analytics IMS組織ID，這就太好了。 如果您打算整合解決方案，以利用購物車放棄（針對AA + AC）等複雜的使用案例，則需要在Analytics和Campaign之間擁有一個IMS組織ID是必要條件。
>
>如果您有不同的Adobe Campaign和Adobe Analytics IMS組織ID，請聯絡客戶服務以協調它們。

**我如何得知我的 Adobe Campaign 執行個體是否託管在 AWS 上？**

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

## 控制面板{#control-panel}

**什麼是「控制面板」？**

「控制面板」可讓產品管理員直接管理各種設定，並監視連線至 Adobe Campaign 的 SFTP 伺服器容量。

**「控制面板」目前有哪些功能？**

「控制面板」可讓您追蹤儲存情形、將 IP 新增至允許清單，以及根據您的需求自行管理 SFTP 的 SSH 金鑰並執行其他動作。

有關詳細資訊，請參閱「控制面板」支援的動作文件。

**「控制面板」是否只適用於 Adobe Campaign？**

是的，您只能在「控制面板」中管理 Adobe Campaign 的設定。

**我可以使用「控制面板」嗎？**

「控制面板」僅開放給將 Adobe Campaign 託管在 AWS 上之現有客戶的產品管理員。請注意，我們目前並不支援混合環境。

如果您不是管理員，但想要取得存取權限，請聯絡您的產品管理員，並協助將您新增為管理員。

**如何存取「控制面板」？**

如需存取「控制面板」文件，請依照下列詳細指示操作。

**使用「控制面板」是否需要額外付費？**

否。如果您是 Adobe Campaign 的現有客戶，則無須額外付費。
