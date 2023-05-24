---
product: campaign
solution: Campaign
title: 關於資料庫監視
description: 瞭解如何在控制面板監視 Campaign 資料庫
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2bd7d2dd-97be-49bb-9f8e-7161d0742bc1
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 78%

---

# 關於資料庫監視 {#database-monitoring}

## 關於執行個體資料庫 {#about-instances-databases}

根據您的合約，您的每個 Campaign 執行個體都會以特定數量的資料庫空間佈建。資料庫包含所有儲存在 Adobe Campaign 的&#x200B;**資產**、**工作流程**&#x200B;及&#x200B;**資料**。

隨著時間過去，資料庫可能會達到最大容量限制，特別是永遠不從執行個體中刪除儲存資源，或是有許多工作流程處於暫停狀態。

執行個體資料庫溢出可能會導致幾個問題 (無法登入、傳送電子郵件等)。因此，監視執行個體的資料庫是確保最佳效能的關鍵。

如果您訂閱 [電子郵件警報](../../performance-monitoring/using/email-alerting.md)，當實例的某個資料庫容量達到其容量的80%或更多時，您將通過電子郵件接收通知。

## 監視資料庫使用情況{#monitoring-database-usage}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="關於資料庫監視"
>abstract="在此索引標籤中，您可以取得每個 Campaign 執行個體最新和歷史資料庫使用和演變的即時資訊。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=zh-Hant" text="關於效能監視"

控制面板允許您監視每個 Campaign 執行個體的資料庫使用情況。若要這麼做，請開啟 **[!UICONTROL Performance Monitoring]** 卡片，然後選取 **[!UICONTROL Databases]** 標籤。

從 **[!UICONTROL Instance List]** 中選擇所需的執行個體，以顯示有關執行個體的資料庫容量和已用空間的資訊。

>[!NOTE]
>
>如果控制面板中顯示的可用資料庫空間量未反應合約中所指明的量，請聯絡客戶服務。

![](assets/databases_dashboard.png)

此儀表板中的資料將根據 **[!UICONTROL Database cleanup technical workflow]** 運行在您的市場活動實例上(請參閱 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=zh-Hant#list-of-technical-workflows) 和 [市場活動v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=zh-Hant) 文檔)。 您可以檢查工作流上次在以下運行的時間 **[!UICONTROL Used Space]** 和 **[!UICONTROL Provided Space]** 度量。 請注意，如果工作流程在 3 天後仍未執行，我們建議您與 Adobe 客戶服務聯絡，以便他們調查工作流程未執行的原因。

此儀表板中提供了其他度量，以幫助您分析實例資料庫的使用情況。 以下各節詳細介紹了這些內容：

* [資料庫使用率](../../performance-monitoring/using/database-utilization.md)
* [儲存空間概覽](../../performance-monitoring/using/database-storage-overview.md)
* [前 10 大臨時資源](../../performance-monitoring/using/database-top-ten-resources.md)
* [活動查詢](../../performance-monitoring/using/database-active-queries.md)

![](assets/do-not-localize/how-to-video.png)利用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=zh-Hant#performance-monitoring) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=zh-Hant#performance-monitoring) 在影片中瞭解此功能
