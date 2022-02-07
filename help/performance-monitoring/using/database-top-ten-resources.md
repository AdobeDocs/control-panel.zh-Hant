---
product: campaign
solution: Campaign
title: 前 10 大臨時資源
description: 瞭解如何在控制面板中監視市場活動資料庫上由工作流和交貨生成的10個最大臨時資源。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 92%

---

# 前 10 項臨時資源 {#top-10}

**[!UICONTROL Top 10 temporary resources]** 區域列出了工作流程及傳遞內容所消耗的 10 大臨時資源。

監視資料庫的關鍵步驟，就是針對建立大型臨時資源的工作流程和傳遞進行監視。若有任何臨時資源消耗過多資料庫空間，請確定有必要保留此工作流程或傳遞，最終再導向您的執行個體以停止。

>[!IMPORTANT]
>
>一般建議避免在非開箱即用資源中使用&#x200B;**超過 40 個欄位**。

![](assets/database-top10.png)

>[!NOTE]
>
>若發現工作流程有大量表格數或龐大的資料庫規模，建議您檢視工作流程，以調查工作流程中為何會產生如此大量的資料。
>
>此頁面的最後亦提供 Campaign Standard 及 Classic 資源，協助您防止資料庫超載。

**[!UICONTROL View all]** 按鈕讓您能存取這些臨時資源的詳細資訊。

![](assets/database-top10-view.png)

**[!UICONTROL Keep interim results]** 欄中的值表示選項在 Campaign 中為啟用 (&quot;1&quot;) 或停用 (&quot;0&quot;)。 此選項可讓您在工作流程的各種活動之間儲存轉換結果 (請參閱 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=zh-Hant) 和 [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/introduction/workflow-best-practices.html?lang=zh-Hant#logs) 文件)。

>[!IMPORTANT]
>
>在生產工作流程中，請勿勾選此選項。 將此用於分析結果，且僅供用於測試目的，因此只能在開發或中繼環境中使用。
>
>如果「控制面板」中的值顯示您的某個工作流程已啟用此選項，我們強烈建議您在 Campaign 中關閉它。
