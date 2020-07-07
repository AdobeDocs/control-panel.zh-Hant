---
title: IP允許清單
description: 瞭解如何將IP位址新增至「控制面板」中的允許清單，以進行例項存取
translation-type: tm+mt
source-git-commit: abe22509e3389874e0b3586a99a1ad2d49681ed8
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 49%

---


# IP允許清單 {#ip-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="關於IP允許清單"
>abstract="將IP位址新增至允許清單以存取您的例項。"
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="觀看示範影片"

>[!IMPORTANT]
>
>此功能僅適用於 Campaign Classic 執行個體。

## 關於IP允許清單 {#about-ip-allow-listing}

依預設，您的 Adobe Campaign Classic 執行個體無法從各種 IP 位址進行存取。

如果您的IP位址尚未新增至允許清單，您將無法從此位址登入執行個體。 同樣地，如果IP位址未明確新增至允許清單及執行個體，您可能無法將API連線至訊息中心或行銷實例。

「控制面板」允許您通過向允許清單添加IP地址範圍來設定到實例的新連接。 請依照下列步驟以執行此操作：

一旦IP位址列在允許清單上，您就可以建立促銷活動運算子並將其連結至這些運算子，讓使用者可以存取該例項。

## 最佳實務{#best-practices}

將IP位址新增至「控制面板」的「允許」清單時，請務必遵循下列建議和限制。

* 如果您不想要將 IP 位址連線至您的 RT 伺服器或 AEM 安全區域，**請勿對所有「存取類型」啟用 IP 存取權限**。
* **如果您暫時啟用了對實例的IP地址訪問**，請務必從允許清單中刪除IP地址，一旦您不再需要連接到實例。
* **我們不建議將公共場所的IP位址新增至允許清單** （機場、酒店等）。 請一律使用您的公司 VPN 地址，確保執行個體安全無虞。

## 將IP位址新增至允許執行個體存取的清單 {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="新增 IP 範圍"
>abstract="定義要新增至允許清單以連線至您實例的IP範圍。"

要將IP地址添加到允許清單，請執行以下步驟：

1. Open the **[!UICONTROL Instances Settings card]** to access the IP allow listing tab, then click **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >如果「控制面板」首頁上並未顯示「執行個體設定」卡片，表示您的 IMS 組織 ID 未與任何 Adobe Campaign Classic 執行個體建立關聯

   ![](assets/ip_whitelist_list1.png)

1. 如下所述，填寫您要新增至允許清單的IP範圍資訊。

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**：IP 位址可連線的執行個體，可同時操作多個執行個體。例如，IP允許清單可透過相同步驟同時在生產與階段例項上執行。
   * **[!UICONTROL IP Range]**: 要添加到允許清單的IP範圍，格式為CIDR。 請注意，IP範圍不能與允許清單上的現有範圍重疊。 在該情況下，請先刪除包含重疊 IP 的範圍。
   >[!NOTE]
   >
   >CIDR (無類別域間路由) 是使用「控制面板」介面新增 IP 範圍時支援的格式。語法由 IP 位址、後面加上「/」字元和十進位數字組成。[本文](https://whatismyipaddress.com/cidr)會詳細說明格式及其語法。
   >
   >您可以在網際網路上搜尋免費線上工具，協助您將現有的 IP 範圍轉換為 CIDR 格式。

   * **[!UICONTROL Label]**: 將顯示在允許清單中的標籤。
   * **[!UICONTROL Name]**：此名稱必須是「存取類型」、「執行個體」(若是外部 API 連線) 和 IP 位址的唯一名稱。


1. 指定要授予 IP 位址的存取類型：

   * **[!UICONTROL Campaign Console Access]**：IP 位址可連線至 Campaign Classic Console。請注意，Console 僅為行銷執行個體啟用。由於不允許存取 MID 和 RT 執行個體，因此並未啟用此功能。
   * **[!UICONTROL AEM connection]**：指定的 AEM IP 位址可以連線至行銷執行個體。
   * **[!UICONTROL External API connection]**：具有指定 IP 位址的外部 API 可以連線至行銷和/或 Message Center (RT) 執行個體。請注意，系統並未啟用與 RT 執行個體控制台的連線。
   ![](assets/ip_whitelist_acesstype.png)

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;按鈕。IP範圍會新增至允許清單。

   ![](assets/ip_whitelist_added.png)

若要從允許清單刪除IP範圍，請選取範圍，然後按一下 **[!UICONTROL Delete IP range]** 按鈕。

**相關主題：**
* [IP允許清單（教學課程影片）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/ip-allow-listing.html)
* [將安全區域連結到運算子](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
