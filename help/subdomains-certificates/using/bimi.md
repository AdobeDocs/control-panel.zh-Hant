---
product: campaign
solution: Campaign
title: 新增 BIMI 記錄
description: 瞭解如何為子網域新增 BIMI 記錄。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: eb7863fb-6e6d-4821-a156-03fee03cdd0e
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 84%

---

# 新增 BIMI 記錄 {#dmarc}

## 關於 BIMI 記錄 {#about}

郵件識別品牌指標 (BIMI) 是一種產業標準，允許在郵箱提供者的收件匣中寄件者的電子郵件旁邊顯示核准的標誌，以增強品牌認知度和信任。 它透過 DMARC 驗證寄件者的身分，有助於防止電子郵件詐騙和網路釣魚，讓惡意行動者更難以在電子郵件中模擬合法品牌。

有關 BIMI 實作的詳細資訊，請參閱 [Adobe 傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html?lang=zh-Hant)

![](assets/bimi-example.png){width="70%" align="center"}

## 限制和先決條件 {#limitations}

* SPF、DKIM 和 DMARC 記錄是建立 BIMI 記錄的必要條件
* 只能使用完整子網域委派為子網域新增 BIMI 記錄。 [進一步瞭解子網域設定方法](subdomains-branding.md#subdomain-delegation-methods)
* DMARC 記錄的先決條件：

   * 子網域的記錄原則類型必須設為「隔離」或「拒絕」。 DMARC 原則類型設為「無」時，無法建立 BIMI 記錄。
   * 套用 DMARC 原則的電子郵件百分比必須為 100%。 BIMI 不支援將此百分比設定為小於 100% 的 DMARC 原則。

[瞭解如何設定 DMARC 記錄](dmarc.md)

## 為子網域新增 BIMI 記錄 {#add}

若要新增子網域的 BIMI 記錄，請遵循下列步驟：

1. 從子網域清單中，按一下所需子網域旁的省略符號按鈕，然後選取 **[!UICONTROL 子網域詳細資料]**.

1. 按一下 **[!UICONTROL 新增TXT記錄]** 按鈕，然後選擇 **[!UICONTROL BIMI]** 從 **[!UICONTROL 記錄型別]** 下拉式清單。

   ![](assets/bimi-add.png)

1. 在 **[!UICONTROL 公司標誌URL]**，指定包含您標誌之SVG檔案的URL。

1. 不過 **[!UICONTROL 憑證URL]** 這是選用專案，因此某些信箱供應商(例如Gmail和Apple)需要此專案，這些供應商涵蓋信箱市場的80%。 因此，建議您取得經過認證的標籤憑證 (VMC)，以確實善用 BIMI。

   +++如何取得 VMC？

   取得 VMC 的主要步驟如下：

   1. 在 VMC 發行者認可的智慧財產辦公室註冊您的品牌標誌為商標。 如果您有法務團隊，建議您與其合作以取得商標標誌，或確認商標已註冊。 

   1. 確認標誌已註冊為商標後，請連絡 DigiCert 或 Entrust 憑證授權單位 (CA) 請求 VMC。

   1. 您的 VMC 獲得核准後，您將會收到實體憑證 Privacy Enhanced Mail (PEM) 檔案。 將您從 CA 取得的任何其他中繼憑證附加至此 PEM 檔案。 上傳 PEM 檔案 (連同附加的檔案) 至您的公開 Web 伺服器，並記下 PEM 檔案 URL。 您會在 BIMI TXT 記錄中使用該 URL。

   1. 一旦特定子網域的子網域詳細資訊頁面中顯示 BIMI 記錄，您就可以使用[此處](https://bimigroup.org/bimi-generator/)提供的 BIMI 檢測器來檢查 BIMI 記錄是否正常運作。

   有關 BIMI 實作的詳細資訊，請參閱 [BIMI 標準文件](https://bimigroup.org/implementation-guide/)
+++

1. 按一下 **[!UICONTROL 新增]** 以確認BIMI記錄建立。

建立 BIMI 記錄之後 (大約 5 分鐘)，它就會顯示在子網域的詳細資訊畫面中。 [瞭解如何監視子網域的 TXT 記錄](gs-txt-records.md#monitor)
