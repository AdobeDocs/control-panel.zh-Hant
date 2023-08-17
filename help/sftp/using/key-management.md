---
product: campaign
solution: Campaign
title: 金鑰管理
description: 瞭解如何管理連線至 SFTP 伺服器的金鑰
feature: Control Panel
role: Architect
level: Experienced
exl-id: 03815e01-6371-4e1c-b4b8-7abe25957cee
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 41%

---

# 金鑰管理 {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="關於公開金鑰管理"
>abstract="在此索引標籤中，建立、管理和編輯您的公開金鑰。"
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="觀看示範影片"

Adobe 建議所有客戶使用&#x200B;**公開和私密金鑰組**&#x200B;建立與其 SFTP 伺服器的連線。

以下說明了產生公開 SSH 金鑰以及新增金鑰以存取 SFTP 伺服器的步驟，還有身份驗證相關的建議。

設定了伺服器的存取權限後，請記得&#x200B;**將存取伺服器所需的 IP 位址新增至允許清單**，如此您才能連線至伺服器。如需詳細資訊，請參閱[本章節](../../instances-settings/using/ip-allow-listing-instance-access.md)。

![](assets/do-not-localize/how-to-video.png)利用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/generate-ssh-key.html#sftp-management) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/generate-ssh-key.html#sftp-management) 在影片中瞭解此功能

## 最佳實務 {#best-practices}

**關於公開 SSH 金鑰**

請確定您一律使用相同的驗證來連線至伺服器，並且使用支援的金鑰格式。

**API 與使用者名稱和密碼的整合**

在極少數的情況下，某些SFTP伺服器會啟用密碼式驗證。 Adobe建議您使用金鑰式驗證，因為此方法更有效且更安全。 您可以聯絡客戶服務，以要求切換至金鑰式驗證。

>[!IMPORTANT]
>
>如果您的密碼過期，即使系統上已安裝金鑰，您也無法登入 SFTP 帳戶。

## 安裝 SSH 金鑰 {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="公開金鑰新增"
>abstract="產生執行個體的公開 SSH 金鑰並將其新增到控制面板以存取 SFTP 伺服器。"

>[!IMPORTANT]
>
>關於SSH金鑰，您必須一律遵循組織方針。 以下步驟只是如何建立SSH金鑰的範例，可做為向團隊或內部網路群組溝通需求的有用參考點。

1. 導覽至 **[!UICONTROL Key Management]** 索引標籤，然後按一下 **[!UICONTROL Add new public key]** 按鈕。

   ![](assets/key0.png)

1. 在開啟的對話方塊中，選取想要建立公開金鑰的使用者名稱，以及您想要啟用金鑰的伺服器。

   ![](assets/key1.png)

   >[!NOTE]
   >
   >「控制面板」會檢查指定的使用者名稱是否在指定的執行個體上有效，並可讓您在一或多個執行個體上啟用金鑰。
   >
   >您可以為每位使用者新增一或多個公開 SSH 金鑰。

1. 為了更好地管理您的公開金鑰，您可以設定每個金鑰的可用期間。 若要這麼做，請選取 **[!UICONTROL Type]** 下拉式清單，並在對應欄位中定義持續時間。 如需公開金鑰到期的詳細資訊，請參閱 [本節](#expiry).

   ![](assets/key_expiry.png)

   >[!NOTE]
   >
   >根據預設， **[!UICONTROL Type]** 欄位已設為 **[!UICONTROL Unlimited]**，這表示公開金鑰永不過期。

1. 在 **[!UICONTROL Comment]** 欄位，您可以指出新增此公開金鑰的原因（原因、對象等）。

1. 若要能夠填寫 **[!UICONTROL Public Key]** 欄位中，您必須產生公開SSH金鑰。 根據您的作業系統，請遵循下列步驟。

   **Linux 和 Mac：**

   使用「終端機」產生公開和私密金鑰組：
   1. 輸入以下命令：`ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`。
   1. 在提示出現時提供您金鑰的名稱。如果 .ssh 目錄不存在，系統將會為您建立一個目錄。
   1. 在提示出現時輸入複雜密碼，然後再輸入一次。您也可保留空白。
   1. 系統會建立「name」和「name.pub」金鑰組。搜尋「name.pub」檔案並開啟，其中應包含英數字串，結尾應為您指定的電子郵件地址。

   **Windows：**

   您可能需要安裝協力廠商工具，協助您以相同格式「name.pub」產生私密/公開金鑰組。

1. 開啟 .pub 檔案，然後複製以「ssh...」開頭的整個字串並貼到「控制面板」中。

   ![](assets/publickey.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL Public Key]** 欄位僅接受OpenSSH格式。 公開 SSH 金鑰的大小應為 **2048 位元**。

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;按鈕以建立金鑰。「控制面板」會儲存公開金鑰及其相關聯的指紋，並使用SHA256格式加密。

>[!IMPORTANT]
>
>如果您建立的金鑰是用來與之前從未連線至所選SFTP伺服器的系統建立連線，您必須先將該系統的公用IP新增至允許清單，才能將此系統與SFTP伺服器搭配使用。 請參閱[本節](ip-range-allow-listing.md)。

您可以使用指紋來比對儲存在電腦上的私密金鑰與儲存在「控制面板」中的對應公開金鑰。

![](assets/fingerprint_compare.png)

「**...**」按鈕可讓您刪除現有的金鑰，或將其相關聯的指紋複製到剪貼簿中。

![](assets/key_options.png)

## 管理公開金鑰 {#managing-public-keys}

您建立的公開金鑰會顯示在 **[!UICONTROL Key Management]** 標籤。

您可以根據建立日期或編輯日期、建立或編輯的使用者以及IP範圍到期日來排序專案。

您也可以開始輸入名稱或註解，以搜尋公開金鑰。

![](assets/control_panel_key_management_sort.png)

若要編輯一或多個IP範圍，請參閱 [本節](#editing-public-keys).

若要從清單中刪除一或多個公開金鑰，請選取這些金鑰，然後按一下 **[!UICONTROL Delete public key]** 按鈕。

![](assets/control_panel_delete_key.png)

### 到期 {#expiry}

此 **[!UICONTROL Expires]** 欄會顯示公開金鑰到期前的剩餘天數。

如果您訂閱 [電子郵件警示](../../performance-monitoring/using/email-alerting.md)，您將會在公開金鑰到期的10天及5天前，以及到期的當天，收到電子郵件通知。 收到警示後，您可以 [編輯公開金鑰](#editing-public-keys) 以視需要延長其有效期間。

過期的公開金鑰將在7天後自動刪除。 它顯示為 **[!UICONTROL Expired]** 在 **[!UICONTROL Expires]** 欄。 在此7天期間：

* 過期的公開金鑰無法再用來連線至SFTP伺服器。

* 您可以 [編輯](#editing-public-keys) 過期的公開金鑰並更新其持續時間，以使其再次可用。

* 您可以從清單中刪除它。

## 編輯公開金鑰 {#editing-public-keys}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_update"
>title="編輯公開金鑰"
>abstract="更新選取的公開金鑰以存取您的 SFTP 伺服器。"

若要編輯公開金鑰，請遵循下列步驟。

>[!NOTE]
>
>您只能編輯自控制面板2021年10月版本以來建立的公開金鑰。

1. 從中選擇一或多個專案 **[!UICONTROL Key Management]** 清單。
1. 按一下 **[!UICONTROL Update public key]** 按鈕。

   ![](assets/control_panel_edit_key.png)

1. 您只能編輯公開金鑰到期和/或新增註解。

   >[!NOTE]
   >
   >若要以OpenSSH格式修改使用者名稱、執行個體和公開金鑰，請刪除公開金鑰，並根據您的需求建立新的公開金鑰。

1. 儲存您的變更。
