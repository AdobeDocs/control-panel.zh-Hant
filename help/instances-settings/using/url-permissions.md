---
title: URL權限
description: 瞭解如何在「控制面板」中管理URL權限
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# URL權限 {#url-permissions}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_urlpermissions&quot;
>title=&quot;關於URL權限&quot;
>abstract=&quot;管理Adobe Campaign例項可連線至的URL。&quot;
>additional-url=&quot;https://images-tv.adobe.com/mpcv3/91206a19-d9af-4b6a-8197-0d2810a78941_1563488165.1920x1080at3000_h264.mp4&quot; text=&quot;Watch demo video&quot;

>[!CAUTION]
>
>此功能僅適用於Campaign Classic例項。

## 關於URL權限 {#about-url-permissions}

可由JavaScript代碼（工作流程等）呼叫的預設URL清單的Campaign Classic例項有限。 這些URL可讓您的例項正常運作。

依預設，例項不允許連線至外部URL。 「控制面板」可讓您將一些外部URL新增至授權URL清單，讓您的例項可以連線至這些URL。 這可讓您將促銷活動例項連接至外部系統，例如SFTP伺服器或網站，以啟用檔案和／或資料傳輸。

新增URL後，該URL會在例項的設定檔案(serverConf.xml)中參考。

**相關主題：**

* [設定促銷活動伺服器](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html)
* [外發連接保護](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Outgoing_connection_protection)
* [新增URL權限（教學課程影片）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/adding-url-permissions.html)

## 最佳實務 {#best-practices}

* 請勿將您的促銷活動例項連線至您不想連線至的網站／伺服器。
* 刪除您不再使用的URL。 不過，請注意，如果您公司的其他區段仍連線至您刪除的URL，則沒有人會再使用它。
* 「控制面板」支 **援http**、 **https**&#x200B;和 **sftp** 通訊協定。 輸入無效的URL或通訊協定將會導致錯誤。

## 管理URL權限 {#managing-url-permissions}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesettings_url_add&quot;
>title=&quot;Add new URL&quot;
>abstract=&quot;新增URL以允許連線至您的促銷活動例項。&quot;

若要新增您的例項可連線至的URL，請依照下列步驟進行：

1. 開啟資 **[!UICONTROL Instances Settings]** 訊卡以存取索 **[!UICONTROL URL Permissions]** 引標籤。

   >[!NOTE]
   >
   >如果「控制面板」的首頁上未顯示「例項設定」卡片，表示您的IMS組織ID與任何Adobe Campaign Classic例項不相關聯
   >
   >「 <b><span class="uicontrol">URL權限</span></b> 」標籤會列出您的例項可連接的所有外部URL。 此清單不包含促銷活動運作所需的URL（例如，基礎架構件之間的連線）。

1. 在左窗格中選取所要的例項，然後按一下 **[!UICONTROL Add new URL]** 按鈕。

   ![](assets/add_url1.png)

   >[!NOTE]
   >
   >您的所有促銷活動例項都會顯示在左側窗格清單中。
   >
   >由於「URL權限」管理僅專用於「促銷活動傳統型」例項，因此如果您選取「促銷活動標準」例項，會顯示「不適用例項」訊息。

1. 輸入要授權的URL及其相關通訊協定（http、https或sftp）。

   >[!NOTE]
   >
   >可授權多個例項以連線至URL。 若要這麼做，請直接從「例項」欄位輸入其第一個字母來新增。

   ![](assets/add_url2.png)

1. URL會新增至清單，您現在可以連線至清單。

   >[!NOTE]
   >
   >&quot;/.*」字元會自動新增至您在驗證後所輸入之URL的尾端，以涵蓋所輸入頁面的所有子頁面。

   ![](assets/add_url_listnew.png)

您隨時可以選取URL並按一下按鈕，以刪除該URL **[!UICONTROL Delete URL]** 。

請記住，如果您刪除URL，您的例項將無法再呼叫它。

## 常見問題 {#common-questions}

**我新增了新的URL，但我的例項仍無法連線至該URL。 為什麼？**

在某些情況下，您嘗試連線的URL需要加入白名單、輸入密碼或其他驗證形式。 控制面板不管理其他驗證。
