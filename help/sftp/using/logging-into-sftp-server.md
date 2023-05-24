---
product: campaign
solution: Campaign
title: 登入您的 SFTP 伺服器
description: 瞭解如何登錄到SFTP伺服器
feature: Control Panel
role: Architect
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---

# 登入您的 SFTP 伺服器 {#logging-into-sft-server}

以下步驟詳細說明如何通過SFTP客戶端應用程式連接SFTP伺服器。

![](assets/do-not-localize/how-to-video.png)[ 在影片中探索此功能](https://video.tv.adobe.com/v/27263?quality=12)

登錄到伺服器之前，請確保：

* 您的SFTP伺服器 **由Adobe托管**。
* 已為伺服器設定您的&#x200B;**使用者名稱**。您可以直接在「控制面板」中檢查此資訊， **密鑰管理** 頁籤。
* 您有 **私有和公共密鑰對** 登錄到SFTP伺服器。 請參閱 [此部分](../../sftp/using/key-management.md) 的子菜單。
* 您 **公共IP地址已添加到允許清單** 在SFTP伺服器上。 否則，請參閱 [此部分](../../sftp/using/ip-range-allow-listing.md) 的子菜單。
* 您可以訪問 **SFTP客戶端軟體**。 您可以咨詢IT部門，瞭解他們建議使用的SFTP客戶端應用程式，或在Internet上搜索一個（如果公司策略允許）。

要連接到SFTP伺服器，請執行以下步驟：

1. 啟動「控制面板」，然後選擇 **[!UICONTROL Key Management]** 的 **[!UICONTROL SFTP]** 卡。

   ![](assets/sftp_card.png)

1. 啟動SFTP客戶端應用程式，然後從「控制面板」中複製並貼上伺服器地址，然後按「campaign.adobe.com」，然後填寫用戶名。

   ![](assets/do-not-localize/connect1.png)

1. 在 **[!UICONTROL SSH Private Key]** 欄位中，選擇儲存在電腦中的私鑰檔案。 它對應於與公鑰具有相同名稱且沒有&quot;。pub&quot;副檔名（如&quot;enable&quot;）的文本檔案。

   ![](assets/do-not-localize/connect2.png)

   的 **[!UICONTROL Password]** 欄位將自動填充檔案中的私鑰。

   ![](assets/do-not-localize/connect3.png)

   通過將私鑰或公鑰的指紋與SFTP卡的「密鑰管理」頁籤中顯示的密鑰的指紋進行比較，可以檢查您嘗試使用的密鑰是否保存在控制面板中。

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >如果您使用的是Mac電腦，則可以通過運行以下命令查看儲存在電腦中的私鑰的指紋：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 填寫完所有資訊後，按一下 **[!UICONTROL Connect]** 登錄到SFTP伺服器。

   ![](assets/do-not-localize/sftpconnected.png)
