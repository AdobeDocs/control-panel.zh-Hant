---
title: 活動配置檔案監控
description: 瞭解如何取得每個促銷活動例項的最新和歷史「作用中描述檔」使用和演變的即時資訊。
translation-type: tm+mt
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 14%

---


# 活動配置檔案監控 {#active-profiles-monitoring}

>[!IMPORTANT]
>
>Beta版提供「控制面板」中的作用中描述檔監控功能，並會經常更新和修改，恕不另行通知。
>
>此功能適用於AWS上代管的客戶，這些客戶來自Campaign Standard 10368構建版和Campaign Classic 8931構建版。 如果您使用舊版軟體，則需要升級才能使用此功能。

## 關於作用中的描述檔 {#about-active-profiles}

根據您的合約，您的每個促銷活動例項都會布建特定數量的作用中描述檔，並計為計費用用途。 請參閱您的最新合約，以取得有關已購買之有效設定檔數目的參考。

Profile 是指一筆代表終端客戶或潛在客戶之資訊的紀錄 (例如：nmsRecipient 表格或外部表格中的記錄，包含 cookie 識別碼、客戶識別碼、行動識別碼或特定通路相關的其他資訊)。

如果設定檔在過去12個月中透過任何通道被鎖定或通訊，則會視為作用中。

>[!NOTE]
>
>Facebook 和 Twitter 通路不包含在內。

有關「作用中」描述檔的詳細資訊，請參 [閱Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) 和 [Campaign Classic檔案](https://docs.adobe.com/content/help/en/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) 。

## 監視活動配置檔案 {#monitoring-active-profiles}

「控制面板」可讓您監控每個促銷活動例項的作用中描述檔使用情形。

若要這麼做，請依照下列步驟進行：

1. 開啟「**[!UICONTROL Performance Monitoring]**」卡片，然後選取「**[!UICONTROL Active Profiles]**」標籤。

1. 從中選擇所需的實例 **[!UICONTROL Instance List]**。

1. 此時會顯示例項使用的作用中描述檔數目，以及上次在例項上執行帳單工作流程的時間。

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>活動的個人檔案會根據每天在您執行個體上執行的專屬技術工作流程計數：
>
>* Campaign Standard的 [「帳單」](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html) 工作流程、
>* Campaign [Classic的「作用中帳單設定檔數](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) 」工作流程。


下方區域提供過去30天中作用中描述檔使用情形的圖形表示。 您可以使用右上角的可用篩選器，將顯示的時段變更為1年。

將滑鼠指標暫留在其中一個圖形列上，可讓您取得所選時段上使用的「作用中」描述檔的確切數目。
