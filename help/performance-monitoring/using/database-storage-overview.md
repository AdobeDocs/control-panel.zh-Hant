---
product: campaign
solution: Campaign
title: 儲存空間概觀
description: 了解如何在「控制面板」中監視佔用執行個體上資料庫空間的不同 Campaign 資源。
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
TQID: 'https://experienceleague.adobe.com/3zcScy61C5LHsWM86WWWuy0uic-pdNQGKc0qY7ewwOQ'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e519a22f-a06a-42fc-9d09-d78a3ab2c434
    internal-label: Monitoring guidelines
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 100%
---
# 儲存空間概觀 {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="關於儲存概觀"
>abstract="在此索引標籤中，您可以取得佔用資料庫空間的不同 Campaign 資源的詳細資訊。"

**[!UICONTROL 儲存空間概觀]**&#x200B;區域以圖形呈現以下項目佔用的空間：

* **[!UICONTROL 系統資源]**

  請注意，如果系統資源耗用大部分的資料庫空間，我們建議您聯絡客戶服務。

* 預設會隨 Campaign 執行個體提供的&#x200B;**[!UICONTROL 現成表格]**，
* 透過工作流程和傳遞建立的&#x200B;**[!UICONTROL 臨時表格]**，
* 建立自訂資源後產生的&#x200B;**[!UICONTROL 非現成表格]**。

![](assets/database-storage-overview.png)

按一下&#x200B;**[!UICONTROL 檢視詳細資料]**&#x200B;按鈕，以針對佔用資料庫空間的不同資產取得更多詳細資訊。

您可以使用下拉式清單，來縮小搜尋範圍並僅顯示特定資產類型 (工作流程、傳遞、收件者) 的表格。

![](assets/database-storage-details.png)

請注意，此畫面也可讓您監視可能需要特別注意的工作流程參數，以避免執行個體上出現任何問題。 在[本頁](workflow-monitoring.md)中瞭解更多。
