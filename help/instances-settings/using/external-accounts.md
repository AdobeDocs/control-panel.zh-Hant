---
product: campaign
solution: Campaign
title: 連接MID/RT實例
description: 瞭解如何將MID/RT實例連接到「控制面板」。
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 1b712300bd7a1ef8dc784fa977f938bacc4c5e5b
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---


# 連接MID/RT實例

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="子網域詳細資訊"
>abstract="在此螢幕中，具有混合托管模型的客戶可以提供其營銷實例中存在的MID/RT實例，以便在「控制面板」中執行特定操作。"

「控制面板」允許使用混合托管模型的客戶通過提供其營銷實例中的MID/RT實例，在「控制面板」中執行特定操作。 有關托管模型的詳細資訊，請參閱 [Campaign Classic文檔](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html)。

## 連接MID/RT實例 {#connect}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="子網域詳細資訊"
>abstract="客戶端控制台中用於在市場營銷實例中添加MID/RT實例的操作員的ID。"

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="子網域詳細資訊"
>abstract="在客戶端控制台中用於在市場營銷實例中添加MID/RT實例的操作員的密碼。"

要在控制面板中提供MID/RT實例，請執行以下步驟：

1. 在 **[!UICONTROL Instances Settings]** 卡，選擇 **[!UICONTROL External Accounts]** 頁籤。

1. 從下拉清單中選擇市場營銷實例，然後按一下 **[!UICONTROL Add new URL]**。

   ![](assets/external-account-addbutton.png)

1. 提供有關要連接的MID/RT實例的資訊：
   * **[!UICONTROL URL]**:實例的URL,
   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**:客戶端控制台中用於在市場營銷實例中添加MID/RT實例的操作員的憑據。

   ![](assets/external-account-add.png)

1. 按一下 **[!UICONTROL Save]** 確認。

您的實例現在已連接到「Control Panel（控制面板）」。 通過從清單中選擇連接，可以隨時刪除或停用連接。

![](assets/external-account-edit.png)

## 可用於MID/RT實例的功能 {#capabilities}

一旦MID/RT實例連接到控制面板，您就可以利用下面列出的功能對其進行監視：

* [查看實例詳細資訊](../../instances-settings/using/instance-details.md)。
* [將IP地址添加到允許清單以訪問實例](../../instances-settings/using/ip-allow-listing-instance-access.md)。
* [查看有關委派子域的資訊](../../subdomains-certificates/using/setting-up-new-subdomain.md)。
* [查看有關SSL證書的資訊](../../subdomains-certificates/using/monitoring-ssl-certificates.md)。
