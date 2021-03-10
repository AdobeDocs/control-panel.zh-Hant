---
product: campaign
solution: Campaign
title: GPG 金鑰管理
description: 瞭解如何管理GPG金鑰，以在Adobe Campaign加密和解密資料。
feature: 控制面板
role: 架構師
level: 經驗豐富
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 8%

---


# GPG 金鑰管理 {#gpg-keys-management}

## 關於GPG加密{#about-gpg-encryption}

GPG加密允許您使用遵循[OpenPGP](https://www.openpgp.org/about/standard/)規範的公私密密鑰對系統來保護資料。

在實施後，您可以在傳輸之前解密傳入的資料並加密傳出的資料，以確保沒有有效匹配密鑰對的任何人不會訪問這些資料。

若要使用 Campaign實作 GPG加密，管理員使用者必須直接從控制面板在行銷執行實例安裝及/或產生 GPG 金鑰。

然後，您將能夠：

* **加密發送的資料**:Adobe Campaign在使用安裝的公鑰加密資料後，會將資料發出。

* **解密傳入資料**:Adobe Campaign接收使用從控制面板下載的公開金鑰從外部系統加密的資料。Adobe Campaign使用從控制面板產生的私密金鑰解密資料。

## 加密資料{#encrypting-data}

「控制面板」可以讓您加密從 Adobe Campaign 執行個體傳出的資料。

為此，您需要從PGP加密工具生成GPG密鑰對，然後將公共密鑰安裝到「控制面板」中。 然後，您就可以在從實例發送資料之前加密資料。 請依照下列步驟以執行此操作。

![](assets/do-not-localize/how-to-video.png)[ 在影片中探索此功能](#video)

1. 使用遵循[OpenPGP規範](https://www.openpgp.org/about/standard/)的PGP加密工具生成公用／私用密鑰對。 為此，請安裝GPG實用程式或GNuGP軟體。

   >[!NOTE]
   >
   >提供可產生金鑰的開放原始碼免費軟體。 不過，請務必遵循貴機構的准則，並使用IT/安全性機構建議的GPG公用程式。

1. 安裝該實用程式後，在Mac終端機或Windows命令中運行以下命令。

   `gpg --full-generate-key`

1. 出現提示時，請指定您的索引鍵所需的參數。 所需參數為：

   * **鍵類型**:RSA
   * **鍵長**:1024 - 4096比特
   * **真實** 姓名 **和電子郵件地址**:允許跟蹤建立密鑰對的人。輸入連結至您的組織或部門的名稱和電子郵件地址。
   * **注釋**:在注釋欄位中新增標籤，可協助您輕鬆識別用來加密資料的金鑰。
   * **有效期**:日期或「0」，表示無到期日。
   * **密碼短語**

   ![](assets/do-not-localize/gpg_command.png)

1. 確認後，指令碼將生成一個帶有其相關指紋的密鑰，您可以將其導出到檔案中，或直接貼上到「控制面板」中。 要導出檔案，請運行此命令，然後運行生成的密鑰的指紋。

   `gpg -a --export <fingerprint>`

1. 若要將公開金鑰安裝至「控制面板」，請開啟&#x200B;**[!UICONTROL Instance settings]**&#x200B;卡，然後選取&#x200B;**[!UICONTROL GPG keys]**&#x200B;標籤和所要的例項。

1. 按一下 **[!UICONTROL Install Key]** 按鈕。

   ![](assets/gpg_install_button.png)

1. 貼上已從PGP加密工具產生的公開金鑰。 您也可以直接拖放您匯出的公開金鑰檔案。

   >[!NOTE]
   >
   >公開金鑰應採用OpenPGP格式。

   ![](assets/gpg_install_paste.png)

1. 按一下 **[!UICONTROL Install Key]** 按鈕。

在安裝公開金鑰後，它會顯示在清單中。 您可以使用&#x200B;**...**&#x200B;按鈕，以下載或複製其指紋。

![](assets/gpg_install_download.png)

此金鑰可在Adobe Campaign工作流程中使用。 使用資料擷取活動時，您可使用它來加密資料。

![](assets/do-not-localize/how-to-video.png)[ 在影片中探索此功能](#video)

有關此主題的更多資訊，請參閱Adobe Campaign文檔：

**Campaign Classic:**

* [壓縮或加密檔案](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#zipping-or-encrypting-a-file)
* [使用案例：使用控制面板上安裝的密鑰加密和導出資料](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [管理已加密的資料](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [使用案例：使用控制面板上安裝的密鑰加密和導出資料](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

## 解密資料 {#decrypting-data}

「控制面板」可讓您解密傳入Adobe Campaign實例的外部資料。

若要這麼做，您必須直接從「控制面板」產生GPG金鑰對。

* **公開金鑰**&#x200B;將與外部系統共用，外部系統將使用它來加密要傳送至Campaign的資料。
* 促銷活動將使用&#x200B;**私密金鑰**&#x200B;解密傳入的加密資料。

![](assets/do-not-localize/how-to-video.png)[ 在影片中探索此功能](#video)

要在「Control Panel（控制面板）」中生成鍵對，請執行以下步驟：

1. 開啟&#x200B;**[!UICONTROL Instance settings]**&#x200B;卡片，然後選取&#x200B;**[!UICONTROL GPG keys]**&#x200B;標籤和所要的Adobe Campaign例項。

1. 按一下 **[!UICONTROL Generate Key]** 按鈕。

   ![](assets/gpg_generate.png)

1. 指定鍵的名稱，然後按一下&#x200B;**[!UICONTROL Generate Key]**。 此名稱可協助您識別促銷活動工作流程中用於解密的金鑰

   ![](assets/gpg_generate_name.png)

一旦產生金鑰對，公開金鑰就會顯示在清單中。 請注意，解密密鑰對是在沒有到期日的情況下生成的。

您可以使用&#x200B;**...**&#x200B;按鈕，以下載公開金鑰或複製其指紋。

![](assets/gpg_generate_list.png)

公共密鑰隨後可用於與任何外部系統共用。 Adobe Campaign將能夠在資料載入活動中使用私鑰解密已用公鑰加密的資料。

有關詳情，請參閱Adobe Campaign檔案：

**Campaign Classic:**

* [在處理前解壓縮或解密檔案](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#unzipping-or-decrypting-a-file-before-processing)
* [使用案例：匯入使用控制面板產生的金鑰加密的資料](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [管理已加密的資料](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [使用案例：匯入使用控制面板產生的金鑰加密的資料](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## 監控GPG密鑰

要訪問為實例安裝和配置的GPG密鑰，請開啟&#x200B;**[!UICONTROL Instance settings]**&#x200B;卡，然後選擇&#x200B;**[!UICONTROL GPG keys]**&#x200B;頁籤。

![](assets/gpg_list.png)

該清單顯示為實例安裝和生成的所有加密和解密GPG密鑰，其中包含每個密鑰的詳細資訊：

* **[!UICONTROL Name]**:安裝或生成密鑰時已定義的名稱。
* **[!UICONTROL Use case]**:此列指定鍵的使用案例：

   ![](assets/gpg_icon_encrypt.png):已安裝該密鑰以進行資料加密。

   ![](assets/gpg_icon_decrypt.png):已生成密鑰以允許資料解密。

* **[!UICONTROL Fingerprint]**:鑰匙的指紋。
* **[!UICONTROL Expires]**:密鑰的到期日。請注意，當主要指示即將到期時，控制面板將提供視覺指示：

   * 30天前會顯示緊急（紅色）。
   * 警告（黃色）顯示於60天前。
   * 當金鑰過期時，會顯示「已過期」的紅色橫幅。

   >[!NOTE]
   >
   >請注意，控制面板不會傳送任何電子郵件通知。

建議您移除不再需要的任何金鑰，這是最佳實務。 要執行此操作，請按一下&#x200B;**...**&#x200B;按鈕，然後選擇&#x200B;**[!UICONTROL Delete Key]。**。

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>在移除金鑰之前，請確定未在任何Adobe Campaign工作流程中使用金鑰，以防止金鑰失敗。

## 教學課程影片{#video}

以下視訊說明如何產生和安裝GPG金鑰以進行資料加密。

[Campaign Classic](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings)和[Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings)教學課程頁面提供與GPG密鑰管理相關的其他操作視頻。

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)

