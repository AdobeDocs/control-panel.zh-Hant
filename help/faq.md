---
title: 控制面板常見問答集
description: 與控制面板相關的常見問題
translation-type: tm+mt
source-git-commit: 7bde86a86fbd128f4eb7bf029e58b0f95964390b
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 5%

---


# 常見問答集 {#faq}

## IMS組織ID {#ims-org-id}

**什麼是IMS組織ID?**

這是您第一次登入Adobe Experience Cloud時，提供給您實例的唯一ID。 它的格式應為： xxx@AdobeOrg。

如需詳細資訊，請參閱 [Adobe Experience Cloud檔案](https://marketing.adobe.com/resources/help/zh_TW/mcloud/organizations.html)。

**我可以在哪裡找到我的IMS組織ID?**

One way is to navigate to [Adobe Experience Cloud Home](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. You will find your IMS Org ID at the bottom of Administration **[!UICONTROL Quick Access]** section. 您可在 [Adobe Experience Cloud 文件](https://marketing.adobe.com/resources/help/zh_TW/mcloud/organizations.html)中找到更多詳細資訊。

另一種方式是啟動 **Admin Console**。 您的IMS組織ID將會顯示在您的URL中，其外觀應該類似： https://adminconsole.adobe.com/xxx@AdobeOrg/overview。

**我為何需要知道我的IMS組織ID?**

為了讓您管理實例的設定，我們希望確保您針對正確的實例獲得正確的資訊，以備您公司使用多個實例時使用。

**如果我有多個IMS組織ID該怎麼辦？**

如果您擁有多個Adobe解決方案的存取權，可能會有多個IMS組織ID。 在此情況下，您應使用的正確IMS組織ID是您在Adobe Campaign例項下看到的IMS組織ID。

>[!NOTE]
>
>如果您有相同的Adobe Campaign和Adobe Analytics IMS組織ID，這就太好了。 如果您打算整合解決方案，以利用購物車放棄（針對AA + AC）等複雜的使用案例，則需要在Analytics和Campaign之間擁有一個IMS組織ID是必要條件。
>
>如果您有不同的Adobe Campaign和Adobe Analytics IMS組織ID，請聯絡客戶服務以協調它們。

**我要如何得知我的Adobe Campaign實例是否在AWS上托管？**

要檢查您的實例是否托管在AWS上，請執行以下步驟：

1. 擷取您的登入URL。 它是您用來登入Campaign例項的URL，最終結束為&quot;。campaign.adobe.com&quot;或&quot;。neolane.net&quot;。
1. 開啟終端，然後對您的登 **[!DNL nslookup]** 入URL執行操作。

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. 回應會傳回您實例的資訊。

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

1. 對返回 **的IP地址** ，執行nslookup操作。

   `doe-macOS% nslookup 12.34.567.89`

1. 在傳回的結果中檢查「名稱」值。 如果包含「amazonaws.com」，表示您的實例是在AWS上托管的。

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>如果您希望遷移到AWS，請聯繫您的Customer Success Manager以啟動該過程。

## 控制面板 {#control-panel}

**什麼是控制面板？**

「控制面板」可讓產品管理員直接管理各種設定，並監控連接至Adobe Campaign的SFTP伺服器的容量。

**控制面板當前有哪些功能？**

「控制面板」允許您根據自己的需求和其他操作，自行跟蹤SFTP伺服器的儲存、白名單IP並管理SSH密鑰。

有關詳細資訊，請參閱「控制面板」支援的操作文檔。

**「控制面板」是否只適用於Adobe Campaign?**

是的，您只能在「控制面板」中管理Adobe Campaign的設定。

**我可以使用控制面板嗎？**

控制面板僅開放給在AWS上代管Adobe Campaign的現有客戶的產品管理員。 請注意，目前尚未支援混合環境。

如果您不是管理員，但想要存取權，請連絡您的產品管理員，協助您新增為管理員。

**如何存取控制面板？**

請按照訪問控制面板文檔中的詳細說明操作。

**使用控制面板是否需要額外付費？**

否。如果您目前是Adobe Campaign的客戶，則不需額外付費。
