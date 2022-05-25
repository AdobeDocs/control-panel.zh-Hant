---
product: campaign
solution: Campaign
title: 添加MID/RT實例（混合型）
description: 瞭解如何將MID/RT實例添加到具有混合主機模型的控制面板。
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 2458263ef5981a16d983912b498e320501df7889
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 3%

---


# 添加MID/RT實例（混合型）

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="外部帳戶"
>abstract="在此螢幕中，具有混合托管模型的客戶可以提供在「控制面板」的營銷實例中配置的MID/RT實例URL，以便利用「控制面板」功能。"

控制面板允許使用混合托管模型的客戶利用特定的控制面板功能。 為此，他們需要提供在「控制面板」中的營銷實例中配置的MID/RT實例URL。

有關托管模型的詳細資訊，請參閱 [Campaign Classic文檔](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html)。

## 添加MID/RT實例 {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="實例的URL，可在「管理」>「平台」>「外部帳戶」菜單的「市場活動客戶端控制台」中找到。"

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="運算元"
>abstract="Adobe管理員在初始設定後提供的操作員ID。"

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="密碼"
>abstract="Adobe管理員在初始設定後提供的操作員密碼。"

混合型客戶應通過Experience Cloud連接到控制面板。 首次訪問控制面板時，首頁上只顯示兩張卡。

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>如果您遇到訪問「控制面板」的任何問題，則您的營銷實例很可能尚未與您的組織ID映射。 請與客戶服務部聯繫以完成此設定以繼續。 成功連接後，您將看到「控制面板」首頁。

要能夠訪問「控制面板」功能，您需要在 **[!UICONTROL Instances Settings]** 卡。 請依照下列步驟以執行此操作。

1. 在 **[!UICONTROL Instances Settings]** 卡，選擇 **[!UICONTROL External Accounts]** 頁籤。

1. 從下拉清單中選擇所需的市場營銷實例，然後按一下 **[!UICONTROL Add new URL]**。

   ![](assets/external-account-addbutton.png)

1. 提供有關要添加的MID/RT實例的資訊。

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**:實例的URL，可在「市場活動客戶端控制台」中 **[!UICONTROL Administration]** > **[!UICONTROL Platform]** > **[!UICONTROL External Accounts]** 的子菜單。

      ![](assets/external-account-url.png)

   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**:Adobe管理員在初始設定後提供的操作員的憑據。

      >[!NOTE]
      >
      >如果這些詳細資訊不可用，請與客戶服務部聯繫。

1. 按一下 **[!UICONTROL Save]** 確認。

在添加MID/RT URL時，觸發非同步進程以驗證URL的正確性。 此過程可能需要幾分鐘。 在驗證MID/RT實例URL之前，作業將處於掛起狀態。 只有驗證完成後，您才能訪問「控制面板」主功能。

![](assets/external-account-pending.png)

通過從清單中選擇MID/RT實例URL，可以隨時刪除或停用它。

![](assets/external-account-edit.png)

請注意，您可以監視在 **[!UICONTROL External Accounts]** 頁籤 **[!UICONTROL Job Logs]**:

![](assets/external-account-logs.png)

## 為混合型客戶提供的功能 {#capabilities}

在將MID/RT實例添加到「控制面板」後，您可以利用下面列出的功能：

* [監視主要聯絡人和事件](../../service-events/service-events.md)
* [查看實例詳細資訊](../../instances-settings/using/instance-details.md)。
* [將IP地址添加到允許清單](../../instances-settings/using/ip-allow-listing-instance-access.md) （對於RT實例）,
* [查看有關委派子域的資訊](../../subdomains-certificates/using/monitoring-subdomains.md)。
* [查看有關SSL證書的資訊](../../subdomains-certificates/using/monitoring-ssl-certificates.md)。