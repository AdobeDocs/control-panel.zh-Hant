---
product: campaign
solution: Campaign
title: 輸送量和延時監視
description: 瞭解如何在控制面板中監視 Campaign 執行個體的輸送量和延時。
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: 84fe0aeb10bc5e535a7ab54a3316a51a1a32b3ca
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 73%

---

# 輸送量和延時監視 {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="關於輸送量和延時監視 "
>abstract="在此標籤中，您可以監視執行個體的傳遞輸送量和延時在一段時間內的趨勢。"

控制面板允許您監視每個實例的交付吞吐量和延遲。

>[!IMPORTANT]
>
>此功能適用於所有Campaign Standard和v8客戶，以及版本號為9032、9330、9346或9349的營銷活動V7客戶 [獨立](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html) 部署（沒有任何中型實例）。

監視一段時間內傳遞輸送量和延時趨勢如何是瞭解執行個體使用情況並確保其正常運作的關鍵。

此資訊可在「控制面板」中為每個&#x200B;**[!UICONTROL Performance Monitoring]**&#x200B;卡片&#x200B;**[!UICONTROL Throughputs & Latency]**&#x200B;標籤中的 Campaign 執行個體提供 (請注意，「控制面板」可能需要最多 1 小時才能顯示這些圖)。

* **[!UICONTROL Throughput]** 區針對您有權存取的所有通訊頻道，提供每小時從選定 Campaign 執行個體傳送的訊息數目。

   >[!NOTE]
   >
   >對於Campaig v7/v8，顯示的吞吐量編號是從MID（中間採購）實例獲得的吞吐量。 對於獨立營銷(MKT)部署（沒有任何MID實例），將顯示MKT實例的吞吐量。

* **[!UICONTROL Latency]** 區針對在傳送即時異動通訊時選定執行個體遇到的延時提供有關資訊。 以 95 和 99 百分位擷取並視覺化延時情況，這代表 95% 和 99% 的請求應比前述延時快。

![](assets/throughput-latencies-overview.png)

>[!NOTE]
>
>本區顯示的所有數字皆為近似值，僅供參考。

在預設情況下，顯示當天的資料。 您可以使用 **[!UICONTROL 6 months]**、**[!UICONTROL 30 days]** 和 **[!UICONTROL 7 days]** 按鈕變更顯示的時間段。

您還可使用排序 (而非圖形) 以表格格式顯示此資訊。 若要執行此操作，請按一下 **[!UICONTROL Visualization settings]** 按鈕，然後選取 **[!UICONTROL Table]**。

![](assets/throughput-latencies-table.png)
