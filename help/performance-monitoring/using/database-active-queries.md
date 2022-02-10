---
product: campaign
solution: Campaign
title: 監視使用中查詢
description: 瞭解如何在「控制面板」中的 Campaign 執行個體上監視使用中查詢。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: ht
source-wordcount: '118'
ht-degree: 100%

---

# 監視使用中查詢 {#long-running-queries}

 標籤的&#x200B;**[!UICONTROL Databases]**&#x200B;區域&#x200B;**[!UICONTROL Active queries]**&#x200B;列出在選定執行個體上執行時間最長的五個查詢。

![](assets/active-queries.png)

**[!UICONTROL Duration]** 欄指定在執行個體上執行查詢的時間。 持續時間以此格式顯示：`hh:mm:ss.ms`。

>[!IMPORTANT]
>
>如果其中一個查詢已啟動超過 24 小時，您將會收到電子郵件通知，前提是您訂閱了[電子郵件提醒](email-alerting.md)。
>
>在這種情況下，請聯絡「客戶服務」，以便他們確定問題並加以解決。 您需要提供 **[!UICONTROL PID]** 欄值，這是查詢的唯一識別碼。
