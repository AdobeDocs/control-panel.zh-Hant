---
product: campaign
solution: Campaign
title: 儲存空間概覽
description: 瞭解如何在「控制面板」中監視在執行個體上佔用資料庫空間的不同Campaign資源。
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 30%

---

# 儲存空間概覽 {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="關於儲存概述"
>abstract="在此索引標籤中，您可以取得佔用資料庫空間的不同 Campaign 資源的詳細資訊。"

此 **[!UICONTROL 儲存空間概覽]** 區域以圖形呈現以下專案佔用的空間：

* **[!UICONTROL 系統資源]**

  請注意，如果系統資源耗用大部分的資料庫空間，我們建議您聯絡客戶服務。

* **[!UICONTROL 現成可用的表格]** 您的Campaign執行個體預設提供的、
* **[!UICONTROL 臨時表格]** 由工作流程和傳遞內容建立的、
* **[!UICONTROL 非現成可用的表格]** 在建立自訂資源後產生。

![](assets/database-storage-overview.png)

按一下 **[!UICONTROL 檢視詳細資料]** 按鈕，以針對消耗資料庫空間的不同資產取得更多詳細資訊。

您可以使用下拉式清單來縮小搜尋範圍並顯示特定資產型別（工作流程、傳送、收件者）的表格。

![](assets/database-storage-details.png)

請注意，此畫面也可讓您監視可能需要特別關注的工作流程引數，以避免執行個體上出現任何問題。 在[本頁](workflow-monitoring.md)中瞭解更多。
