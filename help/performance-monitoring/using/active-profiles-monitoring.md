---
product: campaign
solution: Campaign
title: 活躍輪廓監視
description: 瞭解如何取得每個 Campaign 執行個體之最新和歷史「活躍輪廓」使用量和演化的即時資訊。
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: 73cf3102c0926728595e975ee4c85bf110f2a23d
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# 監視活躍輪廓 {#active-profiles-monitoring}

## 關於活躍輪廓 {#about-active-profiles}

>[!IMPORTANT]
>
>從「控制面板」進行活躍輪廓監視的功能會在測試版提供，且可能會不時更新和修改，恕不另行通知。其可從 Campaign Standard 版本編號 10368 中使用。

根據您的合約，您的每個 Campaign 執行個體都已佈建特定數量的活躍輪廓，而且會計算這些輪廓數量以結算費用。請參閱您的最新合約，以參考已購買活躍輪廓數目。

「輪廓」是指一筆代表終端客戶或潛在客戶之資訊的記錄 (例如：nmsRecipient 表格或外部表格中的記錄，包含 cookie 識別碼、客戶識別碼、行動識別碼或特定通路相關的其他資訊)。

如果輪廓在過去 12 個月期間，曾經透過任何通道而被設為目標或進行通訊，請將此類輪廓視為「作用中」。

>[!NOTE]
>
>Facebook 和 X (原稱為 Twitter) 管道不予考慮。

如需活躍輪廓的詳細資訊，請參閱 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=zh-Hant) 和 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=zh-Hant#active-profiles) 文件。

## 監視活躍輪廓的使用情況 {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="關於活躍輪廓監視"
>abstract="在此標籤中，您可以取得每個 Campaign 執行個體與您組織最新和歷史活躍輪廓使用情況和演變的即時資訊。"

若要在「控制面板」中監視活躍輪廓的使用情況，請導覽至&#x200B;**[!UICONTROL 效能監視]**&#x200B;卡片 > **[!UICONTROL 活躍輪廓]**&#x200B;標籤，然後從&#x200B;**[!UICONTROL 執行個體清單]**&#x200B;中選取所需的執行個體。

活躍輪廓使用情況的相關資訊隨即顯示。

![](assets/active-profiles-graph.png)

上半區段顯示下列資訊：

* 所選執行個體目前使用的活躍輪廓計數，以及執行個體最近執行計費工作流程的時間戳記。

* 組織內所有執行個體中使用的活躍輪廓總數。

  >[!NOTE]
  >
  >只有當您有多個與組織相關聯的執行個體時，才會看到此區段。

* 分配給組織的活躍輪廓總數。

下半區段會以視覺化方式呈現過去 30 天的活躍輪廓使用情況。您可以使用位於右上角的篩選器，將此時間範圍變更為 1 年。將滑鼠游標暫留在圖形上，這可讓您取得所選時段使用之活躍輪廓的確切數目。

與活動輪廓使用相關的資訊會根據您在執行個體上執行的專屬[!DNL Campaign]「帳單」技術工作流程在「控制面板」更新。

| Campaign 版本 | 技術工作流程 | 執行 |
|  ---  |  ---  |  ---  |
| Campaign Standard | [帳單](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=zh-Hant) | 每日 |
| 促銷活動 v7/v8 | [帳單](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=zh-Hant) | 每月 |

