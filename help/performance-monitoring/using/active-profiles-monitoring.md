---
product: campaign
solution: Campaign
title: 作用中設定檔監控
description: 瞭解如何取得每個 Campaign 執行個體之最新和歷史「作用中設定檔」使用量和演化的即時資訊。
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: 9d0686cd3bb0a037ae66b1a090c3f77d215ff61c
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 85%

---

# 監視作用中設定檔 {#active-profiles-monitoring}

## 關於作用中設定檔 {#about-active-profiles}

>[!IMPORTANT]
>
>從「控制面板」進行作用中設定檔監視的功能會在測試版提供，且可能會不時更新和修改，恕不另行通知。其可從 Campaign Standard 版本編號 10368 中使用。

根據您的合約，您的每個 Campaign 執行個體都已佈建特定數量的作用中設定檔，而且會計算這些設定檔數量以結算費用。請參閱您的最新合約，以參考已購買作用中設定檔數目。

「設定檔」是指一筆代表終端客戶或潛在客戶之資訊的記錄 (例如：nmsRecipient 表格或外部表格中的記錄，包含 cookie 識別碼、客戶識別碼、行動識別碼或特定通路相關的其他資訊)。

如果設定檔在過去 12 個月期間，曾經透過任何通道而被設為目標或進行通訊，請將此類設定檔視為「作用中」。

>[!NOTE]
>
>Facebook 和 Twitter 通路不包含在內。

如需作用中設定檔的詳細資訊，請參閱 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=zh-Hant) 和 [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=zh-Hant#active-profiles) 文件。

## 監視作用中設定檔的使用情況 {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="關於作用中設定檔監視"
>abstract="在此標籤中，您可以取得每個 Campaign 執行個體與您組織最新和歷史作用中設定檔使用情況和演變的即時資訊。"

若要在「控制面板」中監視您作用中設定檔的使用情況，請導覽至 **[!UICONTROL 效能監視]** 卡片> **[!UICONTROL 使用中的設定檔]** 標籤，然後從中選擇所需的執行個體 **[!UICONTROL 執行個體清單]**.

作用中設定檔使用情況的相關資訊隨即顯示。

![](assets/active-profiles-graph.png)

上半區段顯示下列資訊：

* 所選執行個體目前使用的作用中設定檔計數，以及執行個體最近執行計費工作流程的時間戳記。

* 組織內所有執行個體中使用的作用中設定檔總數。

  >[!NOTE]
  >
  >只有當您有多個與組織相關聯的執行個體時，才會看到此區段。

* 分配給組織的作用中設定檔總數。

下半區段會以視覺化方式呈現過去 30 天的作用中設定檔使用情況。您可以使用位於右上角的篩選器，將此時間範圍變更為 1 年。將滑鼠游標暫留在圖形上，這可讓您取得所選時段使用之作用中設定檔的確切數目。

與作用中設定檔使用相關的資訊會根據專用在「控制面板」中更新 [!DNL Campaign] 定期在執行個體上執行的「計費」技術工作流程。

| Campaign 版本 | 技術工作流程 | 執行 |
|  ---  |  ---  |  ---  |
| Campaign Standard | [帳單](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=zh-Hant) | 每日 |
| Campaign v7/v8 | [帳單](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflowsadvanced-management/about-technical-workflows.html) | 每月 |
