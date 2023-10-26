---
product: campaign
solution: Campaign
title: 作用中設定檔監控
description: 瞭解如何取得每個 Campaign 執行個體之最新和歷史「作用中設定檔」使用量和演化的即時資訊。
feature: Control Panel
role: Architect
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: ebebff05669160b97de7e0d58d898ba0e3a30df1
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 41%

---

# 監視作用中設定檔 {#active-profiles-monitoring}

## 關於作用中設定檔 {#about-active-profiles}

>[!IMPORTANT]
>
>從「控制面板」進行作用中設定檔監視的功能會在測試版提供，且可能會不時更新和修改，恕不另行通知。它可從Campaign Standard10368建置中使用。

根據您的合約，您的每個 Campaign 執行個體都已佈建特定數量的作用中設定檔，而且會計算這些設定檔數量以結算費用。請參閱您的最新合約，以參考已購買作用中設定檔數目。

「設定檔」是指一筆代表終端客戶或潛在客戶之資訊的記錄 (例如：nmsRecipient 表格或外部表格中的記錄，包含 cookie 識別碼、客戶識別碼、行動識別碼或特定通路相關的其他資訊)。

如果設定檔在過去 12 個月期間，曾經透過任何通道而被設為目標或進行通訊，請將此類設定檔視為「作用中」。

>[!NOTE]
>
>Facebook 和 Twitter 通路不包含在內。

有關作用中設定檔的詳細資訊，請參閱 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) 和 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) 檔案。

## 監視您使用中的設定檔使用情況 {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="關於作用中設定檔監視"
>abstract="在此索引標籤中，您可以取得您的Campaign執行個體和組織中每個活動設定檔的最新和歷史使用情況和演變的即時資訊。"

與作用中設定檔使用相關的資訊會根據專用在「控制面板」中更新 [!DNL Campaign] 每天在執行個體上執行的技術工作流程：
* Campaign Standard的[「計費」](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=zh-Hant)工作流程、
* 此 [「作用中計費設定檔數目」](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=zh-Hant) Campaign v7/v8的工作流程。


若要在「控制面板」中監視您作用中設定檔的使用情況，請導覽至 **[!UICONTROL Performance Monitoring]** 卡片> **[!UICONTROL Active Profiles]** 標籤，然後從中選擇所需的執行個體 **[!UICONTROL Instance List]**.

有關使用中設定檔的資訊隨即顯示。

![](assets/active-profiles-graph.png)

上方區段會顯示下列資訊：

* 所選執行個體中目前使用的作用中設定檔計數，以及執行個體最近計費工作流程執行的時間戳記。

* 所有執行個體中，整個組織使用的作用中設定檔總數。 只有當您有多個與組織相關聯的執行個體時，此區段才會顯示。

* 配置給貴組織的作用中設定檔總數。

下方區段以視覺化方式呈現過去30天的使用中設定檔使用量。 您可以使用右上角的篩選器將此時間範圍變更為1年。 將游標暫留在圖形上可讓您取得所選期間使用的作用中設定檔的確切數目。
