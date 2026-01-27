---
product: campaign
solution: Campaign
title: IP 範圍允許清單
description: 瞭解如何將 IP 範圍新增至允許清單，以便存取 SFTP 伺服器
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 45a3bfcd-500c-4139-b610-d39989260ab7
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '1057'
ht-degree: 100%

---

# IP 範圍允許清單 {#ip-range-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_ip_whitelist"
>title="關於 IP 允許清單"
>abstract="在此索引標籤中，您可以將 IP 範圍新增至允許清單，以建立與 SFTP 伺服器的連線。此處僅顯示您可存取的 SFTP 伺服器。請聯絡您的管理員以要求存取其他 SFTP 伺服器。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=98" text="觀看示範影片"

SFTP 伺服器會受到保護。為了能夠存取這些檔案進行檢視或撰寫新檔案，您需要將存取該伺服器的系統或用戶端之公開 IP 位址新增至允許清單。

![](assets/do-not-localize/how-to-video.png)在利用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=zh-Hant#sftp-management) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/adding-ip-range-to-allow-list.html?lang=zh-Hant#sftp-management) 的影片中瞭解此功能

## 關於 CIDR 格式 {#about-cidr-format}

CIDR (無類別域間路由) 是使用「控制面板」介面新增 IP 範圍時支援的格式。

語法由 IP 位址、後面加上「/」字元和十進位數字組成。[本文](https://whatismyipaddress.com/cidr){target="_blank"}會詳細說明格式及其語法。

您可以在網際網路上搜尋免費線上工具，協助您將現有的 IP 範圍轉換為 CIDR 格式。

## 最佳實務 {#best-practices}

在「控制面板」上，將 IP 位址新增至允許清單，請務必遵循下列建議和限制。

* **將 IP 範圍新增至允許清單**，而不是使用單一 IP 位址。若要將單一 IP 位址新增至允許清單，請在 IP 位址附加「/32」以指出該範圍僅包含單一 IP。
* **請勿將非常寬的範圍新增至允許清單**，例如，包括 > 265 個 IP 位址。「控制面板」將會拒絕任何介於 /0 和 /23 之間的 CIDR 格式範圍。
* 只能將&#x200B;**公用 IP 位址**&#x200B;新增至允許清單。
* 請務必從允許清單中&#x200B;**定期刪除不再需要的 IP 位址**。

## 將 IP 位址新增至允許清單 {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_add"
>title="IP 範圍設定"
>abstract="定義您要新增至允許清單的 IP 範圍，以便連線至您的 SFTP 伺服器。"

若要將 IP 範圍新增至允許清單，請執行下列步驟：

1. 開啟 **[!UICONTROL SFTP]** 卡片，然後選取 **[!UICONTROL IP 允許名單]**&#x200B;標籤。
1. 每個執行個體會顯示允許清單上的 IP 位址清單。從左側清單中選取所需的執行個體，然後按一下&#x200B;**[!UICONTROL 新增 IP 範圍]**&#x200B;按鈕。

   ![](assets/control_panel_add_range.png)

1. 定義您要新增至允許清單的 IP 範圍。 此欄位只接受 CIDR 格式的 IP 範圍，例如 *192.150.5.0/24*。

   ![](assets/control_panel_add_range4.png)

   >[!IMPORTANT]
   >
   >IP 範圍不能與允許清單上的現有範圍重疊。在該情況下，請先刪除包含重疊 IP 的範圍。

1. 您可以在允許清單中，為多個執行個體新增一個範圍。若要這麼做，請按下向下鍵或輸入所需執行個體的第一個字母，然後從建議清單中選取。

   ![](assets/control_panel_add_range3.png)

1. 為清單中的此 IP 範圍定義顯示的標籤。

   ![](assets/control_panel_add_range2.png)

   >[!NOTE]
   >
   >**[!UICONTROL 標籤]**欄位允許使用下列特殊字元：
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

1. 若要以更佳的方式管理 IP 允許清單，您可以設定每個 IP 範圍可用的期間。若要這樣做，請選取&#x200B;**[!UICONTROL 類型]**&#x200B;下拉式清單，然後在對應欄位中定義期間 如需 IP 範圍到期日的詳細資訊，請參閱[本章節](#expiry)。

   ![](assets/control_panel_add_range5.png)

   >[!NOTE]
   >
   >預設情況下，**[!UICONTROL 類型]**&#x200B;欄位已設為&#x200B;**[!UICONTROL 無限制]**，其表示 IP 範圍永不到期。

1. 在&#x200B;**[!UICONTROL 註解]**&#x200B;欄位中，您可以指出允許此 IP 範圍的原因 (理由、對象等)。

1. 按一下&#x200B;**[!UICONTROL 儲存]**&#x200B;按鈕。在請求完全處理完畢之前，加入允許清單的 IP 範圍都將顯示為&#x200B;**[!UICONTROL 待處理]**，這應該只需要幾秒鐘的時間。

   ![](assets/control_panel_add_range6.png)

>[!IMPORTANT]
>
>如果您嘗試將 SFTP 伺服器連線至新系統，因而將新 IP 範圍新增至允許清單，您可能需要輸入新的公開金鑰才能完成連線。如需詳細資訊，請參閱[本節](key-management.md)。

## 管理 IP 範圍 {#managing-ip-ranges}

您建立的 IP 範圍會顯示在 **[!UICONTROL IP 允許清單]**&#x200B;標籤。

您可以根據建立日期或編輯日期、建立或編輯的使用者，以及 IP 範圍到期日來排序項目。

您也可以開始輸入標籤、範圍、名稱或註解來搜尋 IP 範圍。

![](assets/control_panel_allow_list_sort.png)

若要編輯一或多個 IP 範圍，請參閱[本節](#editing-ip-ranges)。

若要從允許清單中刪除一個或多個 IP 範圍，請選取範圍，然後按一下&#x200B;**[!UICONTROL 刪除 IP 範圍]**&#x200B;按鈕。

![](assets/control_panel_delete_range.png)

### 到期日 {#expiry}

此&#x200B;**[!UICONTROL 到期]**&#x200B;欄顯示 IP 範圍到期前的剩餘天數。

如果您訂閱[電子郵件警示](../../performance-monitoring/using/email-alerting.md)，您會在 IP 範圍到期的 10 天及 5 天前，以及到期當日，收到電子郵件通知。 收到警示後，您可以[編輯 IP 範圍](#editing-ip-ranges)以視需要延長其有效期間。

到期的 IP 範圍將在 7 天後自動刪除。它在&#x200B;**[!UICONTROL 到期]**&#x200B;欄顯示為&#x200B;**[!UICONTROL 已到期]**。這 7 天的期間內：

* 已到期的 IP 範圍無法再用來存取 SFTP 伺服器。

* 您無法建立與到期範圍重疊的另一個 IP 範圍。您必須先刪除已到期的 IP 範圍，才能建立新的範圍。

* 您可以[編輯](#editing-ip-ranges)已到期的 IP 範圍，並更新其期間，予以再次使用。

* 您可以從允許清單中加以刪除。

## 編輯 IP 範圍 {#editing-ip-ranges}

>[!CONTEXTUALHELP]
>id="cp_sftp_iprange_update"
>title="更新 IP 範圍"
>abstract="更新允許連線至您的 SFTP 伺服器的已選取 IP 範圍。"

若要編輯 IP 範圍，請依照下列步驟進行。

>[!NOTE]
>
>您只能編輯自「控制面板」2021 年 10 月發行版本以來建立的 IP 範圍。

<!--Edition is not available for IP ranges that have been created before the Control Panel October 2021 release.-->

1. 從 **[!UICONTROL IP 允許清單]**&#x200B;中選取一或多個 IP 範圍。

1. 按一下&#x200B;**[!UICONTROL 更新 IP 範圍]**&#x200B;按鈕。

   ![](assets/control_panel_edit_range.png)

1. 您只能編輯 IP 範圍到期日和/或新增註解。

   >[!NOTE]
   >
   >若要修改 CIDR 格式、其標籤，或編輯相關執行個體，您必須先刪除 IP 範圍，並根據需求建立新的範圍。

   ![](assets/control_panel_edit_range2.png)

1. 儲存您的變更。

## 監視變更 {#monitoring-changes}

「控制面板」首頁的&#x200B;**[!UICONTROL 工作記錄]**&#x200B;可讓您追蹤和監視對允許清單中的 IP 位址所做的所有變更。

如需「控制面板」介面的詳細資訊，請參閱[本章節](../../discover/using/discovering-the-interface.md)。

![](assets/control_panel_ip_log.png)
