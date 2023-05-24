---
product: campaign
solution: Campaign
title: GPG 金鑰管理
description: 瞭解如何管理GPG密鑰以加密和解密Adobe Campaign內的資料。
feature: Control Panel
role: Architect
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: 5d2f0d08b7f9ae78fecfaa169190d6248ec4505b
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 12%

---

# GPG 金鑰管理 {#gpg-keys-management}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_gpg_management"
>title="關於 GPG 金鑰"
>abstract="在此索引標籤中，您可在行銷執行個體上安裝和/或產生 GPG 金鑰，以將傳送自 Campaign 的資料加密並將傳入的資料解密。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=zh-Hant" text="關於效能監視"

## 關於GPG加密 {#about-gpg-encryption}

GPG加密允許您使用遵循以下命令的公鑰和私鑰對系統保護資料 [OpenPGP](https://www.openpgp.org/about/standard/) 規範。

一旦實施，您就可以在傳輸發生之前對傳入資料進行解密和加密，以確保沒有有效匹配密鑰對的任何人不會訪問這些資料。

若要使用 Campaign實作 GPG加密，管理員使用者必須直接從控制面板在行銷執行實例安裝及/或產生 GPG 金鑰。

之後，您將能夠：

* **加密發送的資料**:Adobe Campaign在用安裝的公鑰加密後發送資料。

* **解密傳入資料**:Adobe Campaign使用從控制面板下載的公鑰從外部系統接收加密的資料。 Adobe Campaign使用從控制面板生成的私鑰解密資料。

## 加密資料 {#encrypting-data}

「控制面板」可以讓您加密從 Adobe Campaign 執行個體傳出的資料。

為此，您需要從PGP加密工具生成GPG密鑰對，然後將公鑰安裝到「控制面板」中。 然後，在從實例發送資料之前，您將能夠加密資料。 請依照下列步驟以執行此操作。

>[!NOTE]
>
>在「控制面板」中最多可安裝60個GPG密鑰。

![](assets/do-not-localize/how-to-video.png)[ 在影片中探索此功能](#video)

1. 使用PGP加密工具在 [OpenPGP規範](https://www.openpgp.org/about/standard/)。 為此，請安裝GPG實用程式或GNuGP軟體。

   >[!NOTE]
   >
   >可使用開源免費軟體生成密鑰。 但是，請確保您遵循組織的准則，並使用IT/安全組織推薦的GPG實用程式。

1. 安裝該應用工具後，在Mac終端或Windows命令中運行以下命令。

   `gpg --full-generate-key`

1. 出現提示時，指定所需的鍵參數。 所需參數為：

   * **鍵類型**:RSA
   * **密鑰長度**:3072 - 4096比特
   * **實名** 和 **電子郵件地址**:允許跟蹤建立密鑰對的人。 輸入連結到您的組織或部門的名稱和電子郵件地址。
   * **注釋**:向注釋欄位添加標籤將幫助您輕鬆確定用於加密資料的密鑰。
   * **到期**:無到期日的日期或「0」。
   * **密碼**

   ![](assets/do-not-localize/gpg_command.png)

1. 確認後，指令碼將生成一個具有其關聯指紋的密鑰，您可以將其導出到檔案中，或直接貼上到控制面板中。 要導出檔案，請運行此命令，然後運行生成的密鑰的指紋。

   `gpg -a --export <fingerprint>`

1. 要將公鑰安裝到「控制面板」中，請開啟 **[!UICONTROL Instance settings]** 卡，然後選擇 **[!UICONTROL GPG keys]** 頁籤和所需實例。

1. 按一下 **[!UICONTROL Install Key]** 按鈕。

   ![](assets/gpg_install_button.png)

1. 貼上從PGP加密工具生成的公鑰。 您還可以直接拖放導出的公鑰檔案。

   >[!NOTE]
   >
   >公鑰應採用OpenPGP格式。

   ![](assets/gpg_install_paste.png)

1. 按一下 **[!UICONTROL Install Key]** 按鈕。

安裝公鑰後，它將顯示在清單中。 您可以使用 **...** 按鈕下載或複製指紋。

![](assets/gpg_install_download.png)

然後，該密鑰可用於Adobe Campaign工作流。 在使用資料提取活動時，可以使用它來加密資料。

![](assets/do-not-localize/how-to-video.png)[ 在影片中探索此功能](#video)

有關本主題的詳細資訊，請參閱Adobe Campaign文檔：

**市場活動v7/v8 :**

* [壓縮或加密檔案](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html)
* [用例：使用控制面板上安裝的密鑰加密和導出資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [管理已加密的資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [用例：使用控制面板上安裝的密鑰加密和導出資料](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html#use-case-gpg-encrypt)

## 解密資料 {#decrypting-data}

控制面板允許您解密進入您的Adobe Campaign實例的外部資料。

為此，需要直接從「控制面板」生成GPG密鑰對。

* 的 **公鑰** 將與外部系統共用，外部系統將使用它加密要發送到市場活動的資料。
* 的 **私鑰** 將被市場活動用於解密傳入的加密資料。

![](assets/do-not-localize/how-to-video.png)[ 在影片中探索此功能](#video)

要在「控制面板」中生成密鑰對，請執行以下步驟：

1. 開啟 **[!UICONTROL Instance settings]** 卡，然後選擇 **[!UICONTROL GPG keys]** 頁籤和所需的Adobe Campaign實例。

1. 按一下 **[!UICONTROL Generate Key]** 按鈕。

   ![](assets/gpg_generate.png)

1. 指定鍵的名稱，然後按一下 **[!UICONTROL Generate Key]**。 此名稱將幫助您確定在市場活動工作流中用於解密的密鑰

   ![](assets/gpg_generate_name.png)

生成密鑰對後，公鑰將顯示在清單中。 請注意，解密密鑰對生成時沒有過期日期。

您可以使用 **...** 按鈕下載公鑰或複製其指紋。

![](assets/gpg_generate_list.png)

公共密鑰隨後可用於與任何外部系統共用。 Adobe Campaign將能夠在資料載入活動中使用私鑰來解密用公鑰加密的資料。

有關詳情，請參閱Adobe Campaign文檔：

**市場活動v7和v8 :**

* [在處理前解壓縮或解密檔案](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html)
* [用例：導入使用控制面板生成的密鑰加密的資料](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [管理已加密的資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [用例：導入使用控制面板生成的密鑰加密的資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## 監視GPG密鑰

要訪問為實例安裝和生成的GPG密鑰，請開啟 **[!UICONTROL Instance settings]** 卡，然後選擇 **[!UICONTROL GPG keys]** 頁籤。

![](assets/gpg_list.png)

該清單顯示已為實例安裝和生成的所有加密和解密GPG密鑰，其中包含每個密鑰的詳細資訊：

* **[!UICONTROL Name]**:安裝或生成密鑰時已定義的名稱。
* **[!UICONTROL Use case]**:此列指定鍵的使用情形：

   ![](assets/gpg_icon_encrypt.png):已安裝用於資料加密的密鑰。

   ![](assets/gpg_icon_decrypt.png):已生成密鑰以允許資料解密。

* **[!UICONTROL Fingerprint]**:鑰匙的指紋。
* **[!UICONTROL Expires]**:密鑰的到期日期。 請注意，當主要設備到期日臨近時，控制面板將提供直觀指示：

   * 30天前顯示緊急（紅色）。
   * 警告（黃色）在60天前顯示。
   * 一旦密鑰過期，將顯示一個「已過期」紅色橫幅。

   >[!NOTE]
   >
   >請注意，控制面板不會發送任何電子郵件通知。

作為最佳做法，我們建議您刪除不再需要的任何密鑰。 要執行此操作，請按一下 **...** 按鈕 **[!UICONTROL Delete Key]。**。

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>在刪除密鑰之前，請確保未在任何Adobe Campaign工作流中使用該密鑰以防止其失敗。

## 教程視頻 {#video}

以下視頻顯示了如何生成和安裝用於資料加密的GPG密鑰。

有關GPG密鑰管理的其他操作視頻，請參見  [市場活動v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html#instance-settings) 和 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html#instance-settings) 教程頁面。

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
