---
product: campaign
solution: Campaign
title: 執行個體詳細資訊
description: 瞭解如何監視「控制面板」的執行個體詳細資訊
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 02819bfc-9886-43fc-8014-9bfe64c42048
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '536'
ht-degree: 100%

---

# 執行個體詳細資訊 {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="關於執行個體詳細資訊"
>abstract="檢視 Adobe Campaign 執行個體的詳細資訊：類型、名稱、版本編號資訊以及可能的升級推薦項目。"

## 關於執行個體詳細資訊 {#about-instance-details}

>[!IMPORTANT]
>
>此功能僅適用於 Campaign v7/v8 執行個體。

您的 Adobe Campaign 執行個體架構可以包含數個伺服器，以便提供行銷活動的彈性。例如，您可以有行銷、即時 (或 Message Center) 和 Mid Sourcing 伺服器以支援您的執行個體。

「執行個體詳細資訊」功能可讓您檢視執行個體的平面架構。除了伺服器資訊外，它還讓您知道執行個體版本編號是否為最新版本，並會視需要建議升級。

>[!NOTE]
>
>我們建議您至少每年升級一次您的執行個體，以免效能下降，並能利用 Adobe Campaign v7/v8 提供的最新功能和修正。

**相關主題：**

* [執行版本編號升級](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=zh-Hant)
* [更新 Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/introduction.html?lang=zh-Hant)

## 擷取關於執行個體的資訊 {#retrieving-information-about-instances}

若要獲得與您執行個體連結之伺服器的資訊，請執行以下步驟：

1. 開啟&#x200B;**[!UICONTROL 「執行個體設定」]**&#x200B;卡片以存取&#x200B;**[!UICONTROL 「執行個體詳細資料」]**&#x200B;標籤。

   >[!NOTE]
   >
   >如果「控制面板」首頁上並未顯示「執行個體設定」卡片，表示您的組織 ID 未與任何 Adobe Campaign v7/v8 執行個體建立關聯

1. 在左窗格中，選取所需的 Campaign 執行個體。

   >[!NOTE]
   >
   >所有 Campaign 執行個體都會顯示在左側窗格清單中。由於「執行個體詳細資訊」功能專屬於 Campaign v7/v8 執行個體，如果您選取 Campaign Standard 執行個體，則會顯示「不適用執行個體」訊息。

1. 隨即顯示伺服器連結的執行個體。

   ![](assets/instance_details.png)

可用資訊包括：

* **[!UICONTROL 類型]**：伺服器的類型。可能的值包括 MKT (行銷)、MID (中間來源) 和 RT (訊息中心 / 即時傳送訊息)。
* **[!UICONTROL 名稱]**：伺服器的名稱。
* **[!UICONTROL 組建：]**&#x200B;安裝在伺服器上的組建版本。
* **[!UICONTROL 更新資訊]**：此欄會通知您伺服器是否需要更新。
   * 綠色：您的伺服器為最新狀態，不需要升級。
   * 黃色：您應考慮升級。您缺少了最新的功能和修正項目。
   * 紅色：盡快升級。您缺少了新功能，伺服器可能無法提供最佳效能。

如果您的其中一台伺服器需要升級，請參閱[本文件](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/updating-adobe-campaign/build-upgrade.html?lang=zh-Hant)以瞭解如何處理的詳細資訊。

## 常見問題 {#common-questions}

**我在執行個體架構上沒有看到 MID 伺服器，是否代表我的執行個體無法正常運作？我是否需要 RT 執行個體才能做到今天無法做到的事？**

您自己的執行個體看起來可能非常不同，它可能並沒有所有類型的伺服器，或者可能有多個相同的伺服器。沒有任何一種或另一種類型的伺服器，並不代表您不能傳送即時訊息或執行其他類型的活動。您可以要求額外的伺服器容量，但需支付額外費用。

如果您認為「執行個體詳細資訊」頁面中並未顯示某些伺服器，請聯烙客戶服務。請務必在您的訊息中註明特定的執行個體 URL。
