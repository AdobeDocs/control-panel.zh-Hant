---
title: 密鑰管理
description: 瞭解如何管理連線至SFTP伺服器的金鑰
translation-type: tm+mt
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451

---


# 密鑰管理 {#key-management}

>[!CONTEXTUALHELP]
>id=&quot;cp_key_management&quot;
>title=&quot;關於金鑰管理&quot;
>abstract=&quot;在此標籤中，您可以管理公開金鑰。&quot;
>additional-url=&quot;https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166&quot; text=&quot;Watch demo video&quot;

Adobe 建議所有客戶使用&#x200B;**公開和私密金鑰組**&#x200B;建立與其 SFTP 伺服器的連線。

下面介紹了生成公共SSH密鑰並將其添加到訪問SFTP伺服器的步驟，以及有關身份驗證的建議。

一旦設定了對伺服器的存取權，請記 **住將需要存取伺服器的IP位址列入白名單** ，以便您連線至伺服器。 如需詳細資訊，請參閱[本小節](../../instances-settings/using/ip-whitelisting-instance-access.md)。

>[!NOTE]
>
>目前無法刪除SSH公鑰。

## 最佳實務 {#best-practices}

**關於公共SSH密鑰**

請確定您始終使用相同的驗證來連接伺服器，並且使用支援的密鑰格式。

**API與使用者名稱和密碼整合**

在極少數情況下，某些SFTP伺服器會啟用密碼驗證。 Adobe建議您使用基於金鑰的驗證，因為此方法更有效率且更安全。 您可以聯絡客戶服務，要求切換至基於金鑰的驗證。

>[!CAUTION]
>
>如果您的密碼過期，即使系統上已安裝密鑰，您也無法登入SFTP帳戶。

![](assets/control_panel_passwordexpires.png)

## 安裝SSH密鑰 {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id=&quot;cp_sftp_publickey_add&quot;
>title=&quot;Add New Public Key&quot;
>abstract=&quot;為實例添加新的公鑰。&quot;

>[!CAUTION]
>
>以下步驟僅是SSH密鑰建立的示例，請遵循有關SSH密鑰的組織指導方針。 以下範例只是如何進行此作業的一個範例，可做為您向您的團隊或內部網路群組傳達需求時的參考點。

1. 導覽至標 **[!UICONTROL Key Management]** 簽，然後按一下 **[!UICONTROL Add new public key]** 按鈕。

   ![](assets/key0.png)

1. 在開啟的對話框中，選擇要為其建立公鑰的用戶名，以及要為其激活密鑰的伺服器。

   >[!NOTE]
   >
   >介面會檢查指定的使用者名稱是否在指定的執行個體上作用中，並提供您在一或多個執行個體上啟動金鑰的選項。
   >
   >可為每個用戶添加一個或多個公共SSH密鑰。

   ![](assets/key1.png)

1. 複製並貼上公共SSH密鑰。 若要產生公開金鑰，請依照下列與您的作業系統對應的步驟進行：

   >[!NOTE]
   >
   >公共SSH密鑰大小應 **為2048位**。

   **Linux和Mac:**

   使用「終端機」產生公用和私密金鑰對：
   1. 輸入以下命令： `ssh-keygen -t rsa -C <your_email@example.com>`。
   1. 在出現提示時，為您的金鑰提供名稱。 如果。ssh目錄不存在，系統將為您建立一個目錄。
   1. 在出現提示時輸入密碼短語，然後重新輸入。 也可保留為空白。
   1. 系統會建立「name」和「name.pub」金鑰對。 搜尋&quot;name.pub&quot;檔案，然後開啟它。 它應有英數字串，結尾應為您指定的電子郵件地址。
   **Windows:**

   您可能需要安裝協力廠商工具，協助您以相同格式「name.pub」產生私人／公用金鑰對。

1. 開啟。pub檔案，然後複製並貼上以&quot;ssh...&quot;開頭的整個字串 到控制面板。

   ![](assets/publickey.png)

1. 按一下 **[!UICONTROL Save]** 按鈕以建立金鑰。 控制面板會儲存公開金鑰及其相關指紋，並使用SHA256格式加密。

您可以使用指紋來比對儲存在電腦上的私密金鑰與儲存在「控制面板」中的對應公開金鑰。

![](assets/fingerprint_compare.png)

&quot;**..**&quot; 按鈕可讓您刪除現有的金鑰，或將其相關指紋複製到剪貼簿中。

![](assets/key_options.png)
