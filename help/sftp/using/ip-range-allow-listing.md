---
product: campaign
solution: Campaign
title: IP 範圍允許清單
description: 瞭解如何將 IP 範圍新增至允許清單，以便存取 SFTP 伺服器
feature: Control Panel
role: Architect
level: Experienced
exl-id: 45a3bfcd-500c-4139-b610-d39989260ab7
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 36%

---

# IP 範圍允許清單 {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="關於 IP 允許清單"
>abstract="在此索引標籤中，您可以將 IP 範圍新增至允許清單，以建立與 SFTP 伺服器的連線。此處僅顯示您可存取的 SFTP 伺服器。請聯絡您的管理員以要求存取其他 SFTP 伺服器。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="觀看示範影片"

SFTP 伺服器會受到保護。為了能夠訪問它們以查看檔案或編寫新檔案，您需要將訪問伺服器的系統或客戶端的公共IP地址添加到允許清單。

![](assets/do-not-localize/how-to-video.png) 使用 [市場活動v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html#sftp-management)

## 關於 CIDR 格式 {#about-cidr-format}

CIDR (無類別域間路由) 是使用「控制面板」介面新增 IP 範圍時支援的格式。

語法由 IP 位址、後面加上「/」字元和十進位數字組成。格式及其語法在 [這篇文章](https://whatismyipaddress.com/cidr){target=&quot;_blank&quot;}。

您可以在Internet上搜索免費的聯機工具，這些工具將幫助您將手頭的IP範圍轉換為CIDR格式。

## 最佳實務 {#best-practices}

在「控制面板」上，將 IP 位址新增至允許清單，請務必遵循下列建議和限制。

* **將 IP 範圍新增至允許清單**，而不是使用單一 IP 位址。若要將單一 IP 位址新增至允許清單，請在 IP 位址附加「/32」以指出該範圍僅包含單一 IP。
* **請勿將非常寬的範圍新增至允許清單**，例如，包括 > 265 個 IP 位址。「控制面板」將會拒絕任何介於 /0 和 /23 之間的 CIDR 格式範圍。
* 只能將&#x200B;**公用 IP 位址**&#x200B;新增至允許清單。
* 確保 **定期刪除IP地址** 不需要再從允許清單中了。

## 將 IP 位址新增至允許清單 {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="IP範圍配置"
>abstract="定義您要新增至允許清單的 IP 範圍，以便連線至您的 SFTP 伺服器。"

若要將 IP 範圍新增至允許清單，請執行下列步驟：

1. 開啟 **[!UICONTROL SFTP]** 卡片，然後選取 **[!UICONTROL IP Allow Listing]** 索引標籤。
1. 每個執行個體會顯示允許清單上的 IP 位址清單。從左側清單中選取所需的執行個體，然後按一下 **[!UICONTROL Add new IP range]**&#x200B;按鈕。

   ![](assets/control_panel_add_range.png)

1. 定義要添加到允許清單的IP範圍。 此欄位僅接受CIDR格式的IP範圍，如 *192.150.5.0/24*。

   ![](assets/control_panel_add_range4.png)

   >[!IMPORTANT]
   >
   >IP 範圍不能與允許清單上的現有範圍重疊。在該情況下，請先刪除包含重疊 IP 的範圍。

1. 可以將一個範圍添加到多個實例的允許清單中。 若要這麼做，請按下向下鍵或輸入所需執行個體的第一個字母，然後從建議清單中選取。

   ![](assets/control_panel_add_range3.png)

1. 定義清單中將顯示的此IP範圍的標籤。

   ![](assets/control_panel_add_range2.png)

   >[!NOTE]
   >
   >在中允許以下特殊字元 **[!UICONTROL Label]** 欄位：
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

1. 為了更好地管理IP允許清單，可以設定每個IP範圍的可用時間。 為此，請在 **[!UICONTROL Type]** 下拉清單，並在相應欄位中定義持續時間。 有關IP範圍到期的詳細資訊，請參見 [此部分](#expiry)。

   ![](assets/control_panel_add_range5.png)

   >[!NOTE]
   >
   >預設情況下， **[!UICONTROL Type]** 欄位設定為 **[!UICONTROL Unlimited]**&#x200B;這意味著IP範圍永遠不會過期。

1. 在 **[!UICONTROL Comment]** 欄位中，您可以指明允許此IP範圍的原因（原因、對象等）。

1. 按一下 **[!UICONTROL Save]** 按鈕。允許清單的IP範圍添加將顯示為 **[!UICONTROL Pending]** 直到完全處理請求，這隻需幾秒鐘。

   ![](assets/control_panel_add_range6.png)

>[!IMPORTANT]
>
>如果您試圖將SFTP伺服器連接到新系統，從而將新的IP範圍添加到允許清單中，則可能需要輸入新的公鑰來完成連接。 如需詳細資訊，請參閱[本節](key-management.md)。

## 管理IP範圍 {#managing-ip-ranges}

建立的IP範圍顯示在 **[!UICONTROL IP Allow Listing]** 頁籤。

您可以根據建立日期或版本日期、建立或編輯項目的用戶以及IP範圍到期日對項目進行排序。

您還可以通過開始鍵入標籤、範圍、名稱或注釋來搜索IP範圍。

![](assets/control_panel_allow_list_sort.png)

要編輯一個或多個IP範圍，請參見 [此部分](#editing-ip-ranges)。

要從允許清單中刪除一個或多個IP範圍，請選擇它們，然後按一下 **[!UICONTROL Delete IP range]** 按鈕

![](assets/control_panel_delete_range.png)

### 到期 {#expiry}

的 **[!UICONTROL Expires]** 列顯示在IP範圍到期之前的剩餘天數。

如果您訂閱 [電子郵件警報](../../performance-monitoring/using/email-alerting.md)，您將在IP範圍到期前10天5天通過電子郵件接收通知，並在IP範圍到期之日收到通知。 收到警報後，您可以 [編輯IP範圍](#editing-ip-ranges) 如有需要，可延長有效期。

7天後將自動刪除過期的IP範圍。 顯示為 **[!UICONTROL Expired]** 的 **[!UICONTROL Expires]** 的雙曲餘切值。 在此7天期間內：

* 不能再使用過期的IP範圍來訪問SFTP伺服器。

* 不能建立與過期範圍重疊的其他IP範圍。 在建立新IP範圍之前，需要先刪除過期的IP範圍。

* 你可以 [編輯](#editing-ip-ranges) 過期的IP範圍並更新其持續時間以使其再次可用。

* 可以從允許清單中刪除它。

## 編輯IP範圍 {#editing-ip-ranges}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_update"
>title="更新IP範圍"
>abstract="更新允許連接到SFTP伺服器的選定IP範圍。"

要編輯IP範圍，請執行以下步驟。

>[!NOTE]
>
>您只能編輯自「控制面板」 2021年10月發行以來建立的IP範圍。

<!--Edition is not available for IP ranges that have been created before the Control Panel October 2021 release.-->

1. 從 **[!UICONTROL IP Allow Listing]** 清單框。

1. 按一下 **[!UICONTROL Update IP range]** 按鈕。

   ![](assets/control_panel_edit_range.png)

1. 您只能編輯IP範圍到期和/或添加新注釋。

   >[!NOTE]
   >
   >要修改CIDR格式、其標籤或編輯相關實例，必須先刪除IP範圍，然後根據需要建立一個新範圍。

   ![](assets/control_panel_edit_range2.png)

1. 儲存您的變更。

## 監視變更 {#monitoring-changes}

的 **[!UICONTROL Job Logs]** 在「控制面板」首頁中，您可以跟蹤和監視對允許清單上的IP地址所做的所有更改。

如需「控制面板」介面的詳細資訊，請參閱[本章節](../../discover/using/discovering-the-interface.md)。

![](assets/control_panel_ip_log.png)
