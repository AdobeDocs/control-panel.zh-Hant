---
product: campaign
solution: Campaign
title: 前 10 大臨時資源
description: 了解如何在「控制面板」中監控Campaign資料庫中工作流程和傳遞所產生的10個最大臨時資源。
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: b17abddf6bad7e58cb7bd825cd97322427a0b21f
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 69%

---

# 前 10 項臨時資源 {#top-10}

**[!UICONTROL Top 10 temporary resources]** 區域列出了工作流程及傳遞內容所消耗的 10 大臨時資源。

監視資料庫的關鍵步驟，就是針對建立大型臨時資源的工作流程和傳遞進行監視。若有任何臨時資源消耗過多資料庫空間，請確定有必要保留此工作流程或傳遞，最終再導向您的執行個體以停止。

>[!IMPORTANT]
>
>一般建議避免在非開箱即用資源中使用&#x200B;**超過 40 個欄位**。若發現工作流程有大量表格數或龐大的資料庫規模，建議您檢視工作流程，以調查工作流程中為何會產生如此大量的資料。
>
>Campaign Standard和傳統准則也位於 [本頁](database-preventing-overload.md) 來防止資料庫過載。

![](assets/database-top10.png)

此 **[!UICONTROL View all]** 按鈕可讓您存取 **[!UICONTROL Storage overview]** 詳細資訊，以取得這些臨時資源的詳細資訊。 如需詳細資訊，請參閱[此頁面](database-storage-overview.md)。
