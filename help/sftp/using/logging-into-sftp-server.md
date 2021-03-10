---
product: campaign
solution: Campaign
title: 登入您的 SFTP 伺服器
description: 瞭解如何登入您的SFTP伺服器
feature: 控制面板
role: 架構師
level: 經驗豐富
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 7%

---


# 登入您的 SFTP 伺服器 {#logging-into-sft-server}

以下步驟詳細說明如何透過SFTP用戶端應用程式連接SFTP伺服器。

![](assets/do-not-localize/how-to-video.png)[ 在影片中探索此功能](https://video.tv.adobe.com/v/27263?quality=12)

在登入伺服器之前，請確定：

* 您的SFTP伺服器由Adobe **托管。**
* 已為伺服器設定您的&#x200B;**使用者名稱**。您可以直接在「控制面板」中，從SFTP卡的&#x200B;**鍵管理**&#x200B;標籤中檢查此資訊。
* 您有&#x200B;**專用和公用密鑰對**&#x200B;可登錄到SFTP伺服器。 有關如何添加SSH密鑰的詳細資訊，請參閱[本節](../../sftp/using/key-management.md)。
* 您的&#x200B;**公用IP位址已新增至SFTP伺服器上的allow list**。 如果沒有，請參閱[本節](../../sftp/using/ip-range-allow-listing.md)以取得如何將IP範圍新增至允許清單的詳細資訊。
* 您可以訪問&#x200B;**SFTP客戶端軟體**。 您可以洽詢IT部門，以取得建議使用的SFTP用戶端應用程式，或在您的公司政策允許的情況下，在網際網路上搜尋。

若要連線至您的SFTP伺服器，請依照下列步驟進行：

1. 啟動「Control Panel（控制面板）」，然後從&#x200B;**[!UICONTROL SFTP]**&#x200B;卡中選擇&#x200B;**[!UICONTROL Key Management]**&#x200B;標籤。

   ![](assets/sftp_card.png)

1. 啟動您的SFTP用戶端應用程式，然後從「控制面板」複製並貼上伺服器位址，接著是「campaign.adobe.com」，然後填入您的使用者名稱。

   ![](assets/do-not-localize/connect1.png)

1. 在&#x200B;**[!UICONTROL SSH Private Key]**&#x200B;欄位中，選取儲存在您電腦中的私密金鑰檔案。 它對應的文字檔案與您的公開金鑰同名，沒有副檔名&quot;。pub&quot;（例如&quot;enable&quot;）。

   ![](assets/do-not-localize/connect2.png)

   **[!UICONTROL Password]**&#x200B;欄位會自動填入檔案的私密金鑰。

   ![](assets/do-not-localize/connect3.png)

   您可以比較私密金鑰或公開金鑰的指紋和SFTP卡的「金鑰管理」標籤中顯示的金鑰指紋，以檢查您嘗試使用的金鑰是否已儲存在「控制面板」中。

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >如果您使用Mac電腦，則可以執行下列命令，來檢視儲存在電腦中的私密金鑰指紋：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 填入所有資訊後，按一下&#x200B;**[!UICONTROL Connect]**&#x200B;以登入您的SFTP伺服器。

   ![](assets/do-not-localize/sftpconnected.png)
