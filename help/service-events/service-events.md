---
product: campaign
solution: Campaign
title: 監視主要聯絡人和事件
description: 瞭解如何識別在執行個體上發生的事件和 Adobe 的主要聯絡人。
feature: Control Panel
role: Architect
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: ht
source-wordcount: '497'
ht-degree: 100%

---

# 監視主要聯絡人和事件 {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="服務行事曆"
>abstract="「主要聯絡人」區段列出了 Adobe 的聯絡窗口，您可藉此提出任何問題或有關執行個體的請求。在「服務事件行事曆」部分，您可識別選定執行個體的版本以及服務審查，並為即將發生的事件設定提醒。"

>[!IMPORTANT]
>
>服務行事曆現有提供測試版，且可能會不時更新和修改，恕不另行通知。

確定在執行個體上規劃的事件對於監控 Campaign 執行個體至關重要。

有了「控制面板」，您可以監視執行個體上的發行版本和服務審查，並為某項請求或問題存取 Adobe 的主要聯絡人清單。

這些資訊可在控制面板首頁上的&#x200B;**[!UICONTROL Service Calendar]**&#x200B;卡片取得。

## 主要聯絡人 {#key-contacts}

**[!UICONTROL Key contacts]**&#x200B;區段列出了 Adobe 的聯絡窗口，以便您提出任何有關執行個體上的請求或問題。

>[!NOTE]
>
>此區段只會顯示托管服務帳戶的資訊。

![](assets/service-events-contacts.png)

主要聯絡人包括以下角色：

* **[!UICONTROL TAM]**：技術客戶經理，
* **[!UICONTROL CSM]**：客戶成功經理，
* **[!UICONTROL Deliverability]**：傳遞作業的聯絡點，
* **[!UICONTROL Transition Manager]**：Managed Services 轉變經理 (僅限 Managed Services 客戶)，
* **[!UICONTROL On-boarding Specialist]**：指派給客戶的專家，可幫助您上手 Campaign Classic (僅限 Managed Services 客戶)。

## 事件 {#events}

### 監視事件 {#monitor-events}

**[!UICONTROL Service Event Calendar]** 區段顯示選定執行個體所有過去和即將發佈的版本以及服務審查。

![](assets/service-events-calendar.png)

**[!UICONTROL Note]**&#x200B;欄提供了有關每個版本的狀態資訊：

* **[!UICONTROL General availability]**：最新可用的穩定版本。
* **[!UICONTROL Limited availability]**：僅限隨選部署。
* **[!UICONTROL Release candidate]**：工程驗證。 等待生產校訂。 
* **[!UICONTROL Pre release]**：針對特定客戶需求的更早可用性。
* **[!UICONTROL No longer available]**：此版本雖無重大問題，仍有附加錯誤修復的新版可用。需要更新。
* **[!UICONTROL Deprecated]**：建立嵌入已知的迴歸。
不再支援此版本。須更新。

您可為一個或多個即將發生的事件指派旗標，以追蹤這些事件。 若要執行此動作，請按一下事件名稱旁邊的橢圓按鈕。

![](assets/service-events-flag.png)

### 設定提醒 {#reminders}

您可以使用服務行事曆設定提醒，以便在事件發生之前透過電子郵件通知您。

>[!NOTE]
>
>為了獲得有關即將發生的事件的通知，請確保您已在「控制面板」中訂閱了電子郵件警示。 [了解更多](../performance-monitoring/using/email-alerting.md)

設定事件警示，請執行以下步驟：

1. 按一下要提醒的事件旁邊的橢圓按鈕，然後選取 **[!UICONTROL Set Reminder]**。

1. 為提醒事項提供標題，然後選取要在事件發生之前通知的日期。

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >如果您尚未訂閱「控制面板」警示，會顯示一則訊息，允許您註冊接收電子郵件通知。

1. 現在已為所選的事件設定提醒。 您可以隨時將滑鼠游標停留在上面以顯示標題。

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >您可以為同一事件設定 2 個提醒。

1. 在指定的提醒日期當天將傳送一封電子郵件，通知您即將發生的事件，並且該提醒會自動從 **[!UICONTROL Reminders]** 服務日曆選單的項目個數中移除。
