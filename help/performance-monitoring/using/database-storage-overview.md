---
product: campaign
solution: Campaign
title: 儲存空間概覽
description: 了解如何在「控制面板」中監視佔用執行個體資料庫空間的不同Campaign資源。
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: c52094b8145bdd84aa9e71430a811b8a7b32354d
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 59%

---

# 儲存空間概覽 {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="關於儲存概述"
>abstract="在此索引標籤中，您可以取得佔用資料庫空間的不同 Campaign 資源的詳細資訊。"

**[!UICONTROL Storage overview]** 區域以圖形呈現以下項目佔用的空間：

* **[!UICONTROL System resources]**

   請注意，如果系統資源耗用大部分的資料庫空間，我們建議您聯絡客戶服務。

* 您的 Campaign 執行個體預設提供的 **[!UICONTROL Out-of-the-box tables]**、
* 由工作流程和傳遞內容建立的 **[!UICONTROL Temporary tables]**、
* 在建立自訂資源後產生的 **[!UICONTROL Non-out of the box tables]**。

![](assets/database-storage-overview.png)

按一下 **[!UICONTROL View details]** 按鈕，以針對消耗資料庫空間的不同資產獲取更多詳細資訊。

您可以使用下拉式清單來調整搜尋範圍，並只顯示特定資產類型（工作流程、傳送、收件者）的表格。

![](assets/database-storage-details.png)

請注意，此畫面也可讓您監視可能需要特別注意的工作流程參數，以避免例項上出現任何問題。 在[本頁](workflow-monitoring.md)中瞭解更多。
