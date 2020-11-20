---
product: campaign
solution: Campaign
title: IP 範圍允許清單
description: 瞭解如何將 IP 範圍新增至允許清單，以便存取 SFTP 伺服器
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# IP 範圍允許清單 {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="關於 IP 允許清單"
>abstract="在此索引標籤中，您可以將 IP 範圍新增至允許清單，以建立與 SFTP 伺服器的連線。此處僅顯示您可存取的 SFTP 伺服器。請聯絡您的管理員以要求存取其他 SFTP 伺服器。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="觀看示範影片"

SFTP 伺服器會受到保護。為了能夠存取這些檔案進行檢視或撰寫新檔案，您需要將存取該伺服器的系統或用戶端之公用 IP 地址新增至允許清單。

## 關於 CIDR 格式{#about-cidr-format}

CIDR (無類別域間路由) 是使用「控制面板」介面新增 IP 範圍時支援的格式。

語法由 IP 位址、後面加上「/」字元和十進位數字組成。[本文](https://whatismyipaddress.com/cidr)會詳細說明格式及其語法。

您可以在網際網路上搜尋免費線上工具，協助您將現有的 IP 範圍轉換為 CIDR 格式。

## 最佳實務{#best-practices}

在「控制面板」上，將 IP 位址新增至允許清單，請務必遵循下列建議和限制。

* **將 IP 範圍新增至允許清單**，而不是使用單一 IP 位址。若要將單一 IP 位址新增至允許清單，請在 IP 位址附加「/32」以指出該範圍僅包含單一 IP。
* **請勿將非常寬的範圍新增至允許清單**，例如，包括 > 265 個 IP 位址。「控制面板」將會拒絕任何介於 /0 和 /23 之間的 CIDR 格式範圍。
* 只能將&#x200B;**公用 IP 位址**&#x200B;新增至允許清單。
* 請務必&#x200B;**從允許清單中定期刪除您不再需要的 IP 位址**。

## 將 IP 位址新增至允許清單 {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="新增 IP 範圍"
>abstract="定義您要新增至允許清單的 IP 範圍，以便連線至您的 SFTP 伺服器。"

若要將 IP 範圍新增至允許清單，請執行下列步驟：

1. 開啟 **[!UICONTROL SFTP]** 卡片，然後選取 **[!UICONTROL IP Allow Listing]** 索引標籤。
1. 每個執行個體會顯示允許清單上的 IP 位址清單。從左側清單中選取所需的執行個體，然後按一下 **[!UICONTROL Add new IP range]**&#x200B;按鈕。

   ![](assets/control_panel_add_range.png)

1. 定義您想要新增至允許清單的 IP 範圍，並以 CIDR 格式顯示，然後定義要在清單上顯示的標籤。

   >[!NOTE]
   >
   >「標籤」欄位允許使用下列特殊字元：
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >IP 範圍不能與允許清單上的現有範圍重疊。在該情況下，請先刪除包含重疊 IP 的範圍。
   >
   >可以在允許清單中，為多個執行個體新增一個範圍。若要這麼做，請按下向下鍵或輸入所需執行個體的第一個字母，然後從建議清單中選取。

   ![](assets/control_panel_add_range3.png)

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;按鈕。在完全處理請求之前，新增至允許清單的 IP 會顯示為「待處理」。此流程只需要數秒鐘的時間。

若要從允許清單刪除 IP 範圍，請選取範圍，然後按一下 **[!UICONTROL Delete IP range]** 按鈕。

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>目前無法編輯允許清單上的範圍。若要修改 IP 範圍，請先予以刪除，然後建立符合您需求的範圍。

## 監視變更{#monitoring-changes}

「控制面板」首頁的 **[!UICONTROL Job Logs]** 可讓您監控對列入允許清單之 IP 位址所進行的所有變更。

如需「控制面板」介面的詳細資訊，請參閱[本章節](../../discover/using/discovering-the-interface.md)。

![](assets/control_panel_ip_log.png)
