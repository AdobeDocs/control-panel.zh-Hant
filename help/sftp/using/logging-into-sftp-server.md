---
product: campaign
solution: Campaign
title: 登入您的 SFTP 伺服器
description: 了解如何登入您的SFTP伺服器
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

以下步驟詳細說明如何透過您的SFTP用戶端應用程式連線您的SFTP伺服器。

![](assets/do-not-localize/how-to-video.png)[ 在影片中探索此功能](https://video.tv.adobe.com/v/27263?quality=12)

登入伺服器之前，請確定：

* 您的SFTP伺服器為 **由Adobe托管**.
* 已為伺服器設定您的&#x200B;**使用者名稱**。您可以直接在「控制面板」中檢查此資訊，位於 **金鑰管理** 標籤。
* 您有 **私密金鑰對** 登入SFTP伺服器。 請參閱 [本節](../../sftp/using/key-management.md) 以取得如何新增SSH金鑰的詳細資訊。
* 您的 **公用IP位址已新增至允許清單** 在SFTP伺服器上。 否則，請參閱 [本節](../../sftp/using/ip-range-allow-listing.md) 以取得如何將IP範圍新增至允許清單的詳細資訊。
* 您可以存取 **SFTP用戶端軟體**. 您可以向IT部門洽詢他們建議使用的SFTP用戶端應用程式，或在您的公司原則允許的情況下，在網際網路上搜尋。

若要連線至您的SFTP伺服器，請執行下列步驟：

1. 啟動「控制面板」，然後選取 **[!UICONTROL Key Management]** 標籤 **[!UICONTROL SFTP]** 卡片。

   ![](assets/sftp_card.png)

1. 啟動您的SFTP用戶端應用程式，然後從「控制面板」複製並貼上伺服器位址，接著加上「campaign.adobe.com」，然後填入您的使用者名稱。

   ![](assets/do-not-localize/connect1.png)

1. 在 **[!UICONTROL SSH Private Key]** 欄位中，選取儲存在電腦中的私密金鑰檔案。 它對應的文字檔與您的公開金鑰相同，但沒有副檔名「.pub」（例如「enable」）。

   ![](assets/do-not-localize/connect2.png)

   此 **[!UICONTROL Password]** 欄位會自動填入檔案中的私密金鑰。

   ![](assets/do-not-localize/connect3.png)

   您可以比較私密或公開金鑰的指紋與SFTP卡的「金鑰管理」標籤中顯示金鑰的指紋，以檢查您嘗試使用的金鑰是否已儲存在「控制面板」中。

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >如果您使用的是Mac電腦，則可以運行以下命令查看儲存在電腦中的私鑰的指紋：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 填入所有資訊後，按一下 **[!UICONTROL Connect]** 登入您的SFTP伺服器。

   ![](assets/do-not-localize/sftpconnected.png)
