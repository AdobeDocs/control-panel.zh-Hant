---
title: 登入您的SFTP伺服器
description: 瞭解如何登入您的SFTP伺服器
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# 登入您的SFTP伺服器 {#logging-into-sft-server}

以下步驟詳細說明如何透過SFTP用戶端應用程式連接SFTP伺服器。

在登入伺服器之前，請確定：

* 您的SFTP伺服器 **由Adobe代管**。
* 已為伺服器設定您的&#x200B;**使用者名稱**。You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* 您有一 **對私用和公用密鑰** ，可登入SFTP伺服器。 有關如 [何添加SSH密鑰](../../sftp/using/key-management.md) ，請參閱本節。
* 您 **的公用IP位址已列入** SFTP伺服器的白名單。 如果沒有，請參 [閱本節](../../sftp/using/ip-range-whitelisting.md) ，以取得如何將IP範圍列入白名單的詳細資訊。
* 您可以存取 **SFTP用戶端軟體**。 您可以洽詢IT部門，以取得建議使用的SFTP用戶端應用程式，或在您的公司政策允許的情況下，在網際網路上搜尋。

若要連線至您的SFTP伺服器，請依照下列步驟進行：

1. Launch the Control Panel, then select the **[!UICONTROL Key Management]** tab from the **[!UICONTROL SFTP]** card.

   ![](assets/fingerprintNEW2.png)

1. 啟動您的SFTP用戶端應用程式，然後從「控制面板」複製並貼上伺服器位址，接著是「campaign.adobe.com」，然後填入您的使用者名稱。

   ![](assets/connect1.png)

1. 在欄位 **[!UICONTROL SSH Private Key]** 中，選擇儲存在電腦中的私鑰檔案。 它對應的文字檔案與您的公開金鑰同名，沒有副檔名"。pub"（例如"enable"）。

   ![](assets/connect2.png)

   欄位 **[!UICONTROL Password]** 會自動填入檔案的私密金鑰。

   ![](assets/connect3.png)

   您可以比較私密金鑰或公開金鑰的指紋和SFTP卡的「金鑰管理」標籤中顯示的金鑰指紋，以檢查您嘗試使用的金鑰是否已儲存在「控制面板」中。

   ![](assets/fingerprint3.png)

   >[!NOTE]
   >
   >如果您使用Mac電腦，則可以執行下列命令，來檢視儲存在電腦中的私密金鑰指紋：
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. 所有資訊填入後，按一 **[!UICONTROL Connect]** 下以登入您的SFTP伺服器。

   ![](assets/sftpconnected.png)
