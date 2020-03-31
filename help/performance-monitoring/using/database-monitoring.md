---
title: 資料庫監控
description: 瞭解如何在「控制面板」中監控您的Campaign資料庫
translation-type: tm+mt
source-git-commit: f995e0dc51fd95d00fdcaa2eb347b2aedfdef60d

---


# 資料庫監控 {#database-monitoring}

## 關於實例資料庫 {#about-instances-databases}

根據您的合約，您的每個促銷活動例項都會布建特定數量的資料庫空間。

資料庫包 **括** Adobe Campaign **中儲存的所** 有資產、工作 **流程** 和資料。

隨著時間的推移，資料庫可以達到其最大容量，特別是如果儲存的資源從未從實例中刪除，或者如果有許多工作流處於暫停狀態。

溢出實例資料庫可能會導致幾個問題（無法登錄、無法發送電子郵件等）。 因此，監控實例的資料庫是確保最佳效能的關鍵。

>[!NOTE]
>
>請注意，當前資料庫空間容量與合同中指定的不同時間段的容量之間可能存在一些差異，以確保效能更高。

## 監控資料庫使用情況 {#monitoring-instances-database}

1. 開啟資 **[!UICONTROL Health Monitoring]** 訊卡，然後選取標 **[!UICONTROL Databases]** 簽。

1. 從中選擇所需的實例 **[!UICONTROL Instance List]**。

   上部區域提供實例資料庫容量和使用空間的資訊。

   ![](assets/databases_dashboard.png)

   下方區域提供過去7天中資料庫利用率的圖形表示。 您可以使用右上角的可用篩選器來變更顯示的時段。

   將滑鼠指標暫留在圖形上，可讓您取得所選時段的詳細資訊。

   ![](assets/databases_dashboard_detail.png)

## 防止資料庫過載 {#preventing-database-overload}

Campaign Standard和Classic提供多種方法來防止資料庫磁碟空間過度耗用。

下節提供Campaign檔案的有用資源，以協助您最佳化資料庫的使用：

**工作流程監控**

* [工作流程最佳實務](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) (Campaign Standard)
* [監控工作流程執行](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) (Campaign Classic)

**資料庫維護**

* 資料庫清除技術工[作流程(Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflowshtml#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [資料庫維護指南](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) (Campaign Classic)
* [資料庫效能疑難排解](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) (Campaign Classic)
* [資料庫相關選項](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campaign Classic)
