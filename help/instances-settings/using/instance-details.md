---
title: 例項詳細資訊
description: 在「控制面板」中瞭解如何監控您的例項詳細資訊
translation-type: tm+mt
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# 例項詳細資訊 {#instance-details}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_instancedetails&quot;
>title=&quot;關於例項詳細資訊&quot;
>abstract=&quot;檢視Adobe Campaign例項的詳細資訊：類型、名稱、建置資訊和可能的升級建議。」
>additional-url=&quot;https://docs.adobe.com/content/help/en/campaign-classic/using/release-notes/latest-release.html&quot; text=&quot;Campaign Classic發行說明&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/campaign-standard/using/release-notes/release-notes.html&quot; text=&quot;Campaign Standard版本注意事項&quot;

>[!IMPORTANT]
>
>此功能僅適用於Campaign Classic例項。

## 關於實例詳細資訊 {#about-instance-details}

您的Adobe Campaign Classic實例架構可包含數個伺服器，以提供行銷活動的彈性。 例如，您可以有行銷、即時（或訊息中心）和中端採購伺服器支援您的例項。

「例項詳細資訊」功能可讓您檢視例項的平面架構。 除了伺服器資訊外，它還可讓您知道您的執行個體組建版本是否為最新版本，並建議視需要升級。

>[!NOTE]
>
>我們建議您的例項每年至少升級一次，以避免效能降低，並能運用Adobe Campaign Classic提供的最新功能和修正。

**相關主題：**

* [執行構建版本升級](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [更新Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## 檢索有關實例的資訊 {#retrieving-information-about-instances}

要獲取有關連接到實例的伺服器的資訊，請執行以下步驟：

1. 開啟資 **[!UICONTROL Instances Settings]** 訊卡以存取索 **[!UICONTROL Instance Details]** 引標籤。

   >[!NOTE]
   >
   >如果「控制面板」的首頁上未顯示「例項設定」卡片，表示您的IMS組織ID與任何Adobe Campaign Classic例項不相關聯

1. 在左窗格中，選擇所要的Campaign Classic例項。

   >[!NOTE]
   >
   >您的所有促銷活動例項都會顯示在左側窗格清單中。 由於「例項詳細資料」功能僅專用於「促銷活動傳統型」例項，因此如果您選取「促銷活動標準」例項，會顯示「不適用例項」訊息。

1. 顯示連接到實例的伺服器。

   ![](assets/instance_details.png)

可用資訊包括：

* **[!UICONTROL Type]**:伺服器的類型。 可能的值包括MKT（行銷）、MID（中端採購）和RT（訊息中心／即時訊息）。
* **[!UICONTROL Name]**:伺服器的名稱。
* **[!UICONTROL Build:]** 安裝在伺服器上的組建版本。
* **[!UICONTROL Upgrade info]**:此欄會通知您是否需要伺服器更新。
   * 綠色：您的伺服器是最新的，不需要升級。
   * 黃色：您應考慮升級。 您遺漏了最新的功能和修正。
   * 紅色：盡快升級。 您缺少新功能，伺服器效能可能不是最佳。

如果您的其中一台伺服器需要升級，請參 [閱本文檔](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) ，瞭解有關如何繼續的詳細資訊。

## 常見問題 {#common-questions}

**我在實例體系結構上沒有看到MID伺服器，這是否表示我的實例無法正常工作？ 我是否需要RT例項才能做到今天無法做到的事？**

您自己的實例看起來可能非常不同，它可能並不是所有類型的伺服器，也可能有多個相同的伺服器。 沒有一種或另一種類型的伺服器並不意味著您不能發送即時消息或執行其他類型的活動。 您可以要求額外的伺服器容量，但需支付額外費用。

如果您認為「例項詳細資訊」頁面中未顯示某些伺服器，請連絡客戶服務。 請務必在訊息中記下特定例項URL。
