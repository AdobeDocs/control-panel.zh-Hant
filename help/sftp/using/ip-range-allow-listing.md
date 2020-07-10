---
title: IP範圍允許清單
description: 瞭解如何將IP範圍新增至允許SFTP伺服器存取的清單
translation-type: tm+mt
source-git-commit: d96c044e83d37f020b5fd6ea55199c1223b9fa39
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# IP範圍允許清單 {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="關於IP允許清單"
>abstract="在此標籤中，您可以將IP範圍新增至允許清單，以建立與SFTP伺服器的連線。 此處僅顯示您可存取的 SFTP 伺服器。請聯絡您的管理員以要求存取其他 SFTP 伺服器。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="觀看示範影片"

SFTP 伺服器會受到保護。為了能夠訪問這些檔案或編寫新檔案，您需要將訪問伺服器的系統或客戶端的公共IP地址添加到允許清單。

## 關於 CIDR 格式{#about-cidr-format}

CIDR (無類別域間路由) 是使用「控制面板」介面新增 IP 範圍時支援的格式。

語法由 IP 位址、後面加上「/」字元和十進位數字組成。[本文](https://whatismyipaddress.com/cidr)會詳細說明格式及其語法。

您可以在網際網路上搜尋免費線上工具，協助您將現有的 IP 範圍轉換為 CIDR 格式。

## 最佳實務{#best-practices}

將IP位址新增至「控制面板」的「允許」清單時，請務必遵循下列建議和限制。

* **將IP範圍新增至允許清單** ，而非單一IP位址。 若要新增單一IP位址至允許清單，請在清單中附加&#39;/32&#39;，以指出範圍僅包含單一IP。
* **請勿將非常寬的範圍新增至允許清單**，例如，包括> 265個IP位址。 「控制面板」將會拒絕任何介於 /0 和 /23 之間的 CIDR 格式範圍。
* 只 **能將公用IP位址** 新增至允許清單。
* 請務必 **定期從允許清單中刪除** ，您不再需要的IP位址。

## 將IP位址新增至允許清單 {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="新增 IP 範圍"
>abstract="定義要新增至允許清單的IP範圍，以便連線至您的SFTP伺服器。"

要將IP範圍添加到允許清單，請執行以下步驟：

1. 開啟「**[!UICONTROL SFTP]**」卡片，然後選取「**[!UICONTROL IP Allow Listing]**」標籤。
1. 每個例項會顯示允許清單上的IP位址清單。 從左側清單中選取所需的執行個體，然後按一下 **[!UICONTROL Add new IP range]**&#x200B;按鈕。

   ![](assets/control_panel_add_range.png)

1. 以CIDR格式定義要添加到允許清單的IP範圍，然後定義將在清單中顯示的標籤。

   >[!NOTE]
   >
   >「標籤」欄位允許使用下列特殊字元：
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!IMPORTANT]
   >
   >IP範圍不能與允許清單上的現有範圍重疊。 在該情況下，請先刪除包含重疊 IP 的範圍。
   >
   >可以在允許清單中為多個實例添加一個範圍。 若要這麼做，請按下向下鍵或輸入所需執行個體的第一個字母，然後從建議清單中選取。

   ![](assets/control_panel_add_range3.png)

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;按鈕。在完全處理請求之前，允許清單的IP新增項目會顯示為「待定」。 此流程只需要數秒鐘的時間。

若要從允許清單刪除IP範圍，請選取範圍，然後按一下 **[!UICONTROL Delete IP range]** 按鈕。

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>目前無法編輯允許清單上的範圍。 若要修改 IP 範圍，請先予以刪除，然後建立符合您需求的範圍。

## 監視變更{#monitoring-changes}

The **[!UICONTROL Job Logs]** in the Control Panel home page let you monitor all changes that have been made to IP addresses on the allow list.

如需「控制面板」介面的詳細資訊，請參閱[本節](../../discover/using/discovering-the-interface.md)。

![](assets/control_panel_ip_log.png)
