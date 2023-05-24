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

在極少數情況下，某些SFTP伺服器上啟用了基於密碼的身份驗證。 Adobe建議您使用基於密鑰的身份驗證，因為此方法更高效和安全。 您可以通過聯繫「客戶服務」請求切換到基於密鑰的身份驗證。

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
>您必須始終遵循有關SSH密鑰的組織准則。 以下步驟僅是如何建立SSH密鑰的一個示例，它們可作為向團隊或內部網路組傳達要求的有用參考點。

1. 導覽至 **[!UICONTROL Key Management]** 索引標籤，然後按一下 **[!UICONTROL Add new public key]** 按鈕。

   ![](assets/key0.png)

1. 在開啟的對話方塊中，選取想要建立公開金鑰的使用者名稱，以及您想要啟用金鑰的伺服器。

   ![](assets/key1.png)

   >[!NOTE]
   >
   >控制面板將檢查給定實例上的給定用戶名是否處於活動狀態，並使您能夠在一個或多個實例上激活密鑰。
   >
   >您可以為每位使用者新增一或多個公開 SSH 金鑰。

1. 為了更好地管理公共密鑰，您可以設定每個密鑰的可用時間。 為此，請在 **[!UICONTROL Type]** 下拉清單，並在相應欄位中定義持續時間。 有關公鑰到期的詳細資訊，請參見 [此部分](#expiry)。

   ![](assets/key_expiry.png)

   >[!NOTE]
   >
   >預設情況下， **[!UICONTROL Type]** 欄位設定為 **[!UICONTROL Unlimited]**&#x200B;這意味著公鑰永不過期。

1. 在 **[!UICONTROL Comment]** 欄位中，您可以指明添加此公鑰的原因（原因、對象等）。

1. 能夠填入 **[!UICONTROL Public Key]** 欄位中，需要生成公共SSH密鑰。 根據您的作業系統，請執行以下步驟。

   **Linux 和 Mac：**

   使用「終端機」產生公開和私密金鑰組：
   1. 輸入以下命令：`ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`。
   1. 在提示出現時提供您金鑰的名稱。如果 .ssh 目錄不存在，系統將會為您建立一個目錄。
   1. 在提示出現時輸入複雜密碼，然後再輸入一次。您也可保留空白。
   1. 系統會建立「name」和「name.pub」金鑰組。搜尋「name.pub」檔案並開啟，其中應包含英數字串，結尾應為您指定的電子郵件地址。

   **Windows：**

   您可能需要安裝第三方工具，該工具將幫助您以相同格式「name.pub」生成私鑰/公鑰對。

1. 開啟 .pub 檔案，然後複製以「ssh...」開頭的整個字串並貼到「控制面板」中。

   ![](assets/publickey.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL Public Key]** 欄位只接受OpenSSH格式。 公開 SSH 金鑰的大小應為 **2048 位元**。

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;按鈕以建立金鑰。控制面板保存使用SHA256格式加密的公鑰及其相關指紋。

>[!IMPORTANT]
>
>如果建立的密鑰用於與以前從未連接到選定SFTP伺服器的系統建立連接，則在能夠將此系統與SFTP伺服器一起使用之前，需要將該系統的公用IP添加到允許清單中。 請參閱[本節](ip-range-allow-listing.md)。

您可以使用指紋將保存在電腦上的私鑰與保存在「控制面板」中的相應公鑰進行匹配。

![](assets/fingerprint_compare.png)

「**...**」按鈕可讓您刪除現有的金鑰，或將其相關聯的指紋複製到剪貼簿中。

![](assets/key_options.png)

## 管理公鑰 {#managing-public-keys}

您建立的公鑰在 **[!UICONTROL Key Management]** 頁籤。

您可以根據建立日期或版本日期、建立或編輯項目的用戶以及IP範圍到期日對項目進行排序。

您還可以通過開始鍵入名稱或注釋來搜索公鑰。

![](assets/control_panel_key_management_sort.png)

要編輯一個或多個IP範圍，請參見 [此部分](#editing-public-keys)。

要從清單中刪除一個或多個公鑰，請選擇它們，然後按一下 **[!UICONTROL Delete public key]** 按鈕

![](assets/control_panel_delete_key.png)

### 到期 {#expiry}

的 **[!UICONTROL Expires]** 列顯示在公鑰到期之前的剩餘天數。

如果您訂閱 [電子郵件警報](../../performance-monitoring/using/email-alerting.md)，您將在公鑰到期前10天5天通過電子郵件接收通知，並在公鑰到期後10天5天收到通知。 收到警報後，您可以 [編輯公鑰](#editing-public-keys) 如有需要，可延長有效期。

7天後將自動刪除過期的公鑰。 顯示為 **[!UICONTROL Expired]** 的 **[!UICONTROL Expires]** 的雙曲餘切值。 在此7天期間內：

* 已過期的公鑰不能再用於連接到SFTP伺服器。

* 你可以 [編輯](#editing-public-keys) 過期的公鑰，並更新其持續時間以使其再次可用。

* 可以從清單中刪除它。

## 編輯公鑰 {#editing-public-keys}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_update"
>title="編輯公開金鑰"
>abstract="更新選取的公開金鑰以存取您的 SFTP 伺服器。"

要編輯公鑰，請執行以下步驟。

>[!NOTE]
>
>您只能編輯自「控制面板」 2021年10月發行以來建立的公鑰。

1. 從 **[!UICONTROL Key Management]** 清單框。
1. 按一下 **[!UICONTROL Update public key]** 按鈕。

   ![](assets/control_panel_edit_key.png)

1. 您只能編輯公鑰到期和/或添加新注釋。

   >[!NOTE]
   >
   >要以OpenSSH格式修改用戶名、實例和公鑰，請刪除公鑰，然後根據您的需要建立一個新的公鑰。

1. 儲存您的變更。
