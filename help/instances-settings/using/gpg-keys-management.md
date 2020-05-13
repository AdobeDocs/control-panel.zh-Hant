---
title: GPG密鑰管理
description: 瞭解如何管理GPG金鑰，以在Adobe Campaign中加密和解密資料。
translation-type: tm+mt
source-git-commit: d44c0557904f0e6f6688c12687fbf84e42553d6b
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 0%

---


# GPG密鑰管理 {#gpg-keys-management}

## 關於GPG加密 {#about-gpg-encryption}

GPG加密可讓您使用遵循 [OpenPGP規格的公私密金鑰對系統來保護您的資](https://www.openpgp.org/about/standard/) 料。

在實施後，您可以在傳輸之前解密傳入的資料並加密傳出的資料，以確保沒有有效匹配密鑰對的任何人不會訪問這些資料。

若要使用Campaign實作GPG加密，管理員使用者必須直接從控制面板在行銷實例上安裝和／或產生GPG金鑰。

然後，您將能夠：

* **加密發送的資料**: Adobe Campaign使用已安裝的公開金鑰加密資料後，會將資料傳出。

* **解密傳入資料**: Adobe Campaign會使用從「控制面板」下載的公開金鑰，從外部系統接收加密的資料。 Adobe Campaign會使用從「控制面板」產生的私密金鑰解密資料。

## 監控GPG密鑰

若要存取已安裝並產生的GPG金鑰，請開啟資訊卡， **[!UICONTROL Instance settings]** 然後選取索 **[!UICONTROL GPG keys]** 引標籤。

![](assets/gpg_list.png)

該清單顯示為實例安裝和生成的所有加密和解密GPG密鑰，其中包含每個密鑰的詳細資訊：

* **[!UICONTROL Name]**: 安裝或生成密鑰時已定義的名稱。
* **[!UICONTROL Use case]**: 此列指定鍵的使用案例：

   ![](assets/gpg_icon_encrypt.png): 已安裝該密鑰以進行資料加密。

   ![](assets/gpg_icon_decrypt.png): 已生成密鑰以允許資料解密。

* **[!UICONTROL Fingerprint]**: 鑰匙的指紋。
* **[!UICONTROL Expires]**: 密鑰的到期日。 請注意，當主要指示即將到期時，控制面板將提供視覺指示：

   * 30天前會顯示緊急（紅色）。
   * 警告（黃色）在60天前顯示。
   * 當金鑰過期時，會顯示「已過期」的紅色橫幅。
   >[!NOTE]
   >
   >請注意，控制面板不會傳送任何電子郵件通知。

建議您移除不再需要的任何金鑰，這是最佳實務。 若要這麼做，請按一下 **...** 按鈕，然後選 **[!UICONTROL Delete Key]擇。**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>在移除金鑰之前，請確定未在任何Adobe Campaign工作流程中使用金鑰，以防止金鑰失敗。

## 加密資料 {#encrypting-data}

「控制面板」可讓您加密從Adobe Campaign例項傳出的資料。

為此，您需要從PGP加密工具生成GPG密鑰對，然後將公共密鑰安裝到「控制面板」中。 然後，您就可以在從實例發送資料之前加密資料。 若要這麼做，請依照下列步驟進行：

1. 使用 [OpenPGP簡化後的GPG加密工具產生公用／私用金鑰對](https://www.openpgp.org/about/standard/)。 為此，請安裝GPG實用程式或GNuPG軟體。

   >[!NOTE]
   >
   >您可使用開放原始碼免費軟體來產生金鑰。 不過，請務必遵循貴組織的准則，並使用IT/安全性組織建議的PGP公用程式。

1. 安裝該實用程式後，在Mac終端或Windows電腦中運行以下命令。

   `gpg --full-generate-key`

1. 出現提示時，請指定您的索引鍵所需的參數。 所需參數為：

   * **鍵類型**: RSA
   * **鍵長**: 1024 - 4096比特
   * **真實姓名** 和電 **子郵件地址**: 允許跟蹤建立密鑰對的人。 輸入連結至您的組織或部門的名稱和電子郵件地址。
   * **注釋**: 將標籤添加到注釋欄位可讓您在「控制面板」鍵清單中輕鬆標識鍵。
   * **有效期**: 日期或「0」，表示無到期日。
   * **密碼短語**
   ![](assets/gpg_command.png)

1. 確認後，指令碼將生成一個鍵，您可以將其導出到檔案，或直接貼上到「控制面板」中。 要導出檔案，請運行此命令，然後運行生成的鍵的指標。

   `gpg -a --export <fingerprint>`

1. 若要將公開金鑰安裝至「控制面板」，請存 **[!UICONTROL GPG Keys]** 取標籤，然後選取所要的例項。

1. Click the **[!UICONTROL Install Key]** button.

   ![](assets/gpg_install_button.png)

1. 貼上已從PGP加密工具產生的公開金鑰。 您也可以直接拖放公開金鑰檔案。

   >[!NOTE]
   >
   >公開金鑰應採用OpenPGP格式。

   ![](assets/gpg_install_paste.png)

1. Click the **!UICONTROL Install Key]** button.

在安裝公開金鑰後，它會顯示在清單中。 您可以使用 **...** 按鈕，以下載或複製其指紋。

![](assets/gpg_install_download.png)

然後，此金鑰便可用於Adobe Campaign工作流程。 使用資料擷取活動時，您可使用它來加密資料。

如需詳細資訊，請參閱Adobe Campaign檔案：

| Campaign Classic | Campaign Standard |
---------|----------
| [壓縮或加密檔案](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#zipping-or-encrypting-a-file) | [管理加密的資料](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/importing-data.html#managing-encrypted-data) |
| [資料擷取（檔案）活動](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/action-activities/extraction--file-.html) | [擷取檔案活動](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/extract-file.html) |

## 解密資料 {#decrypting-data}

「控制面板」可讓您解密傳入Adobe Campaign例項的外部資料。

若要這麼做，您必須直接從「控制面板」產生GPG金鑰對。

* 公 **開金鑰** (public key)將會與外部系統共用，外部系統會使用它來加密要傳送至Campaign的資料。
* Campaign **將使用** 「私密金鑰」解密傳入的加密資料。

要在「Control Panel（控制面板）」中生成鍵對，請執行以下步驟：

1. 存取標 **[!UICONTROL GPG Keys]** 簽，然後選取所要的Adobe Campaign例項。

1. Click the **[!UICONTROL Generate Key]** button.

   ![](assets/gpg_generate.png)

1. 指定索引鍵的名稱，然後按一下 **!UICONTROL Generate Key]**。 此名稱可協助您識別促銷活動工作流程中用於解密的金鑰

   ![](assets/gpg_generate_name.png)

一旦產生金鑰對，公開金鑰就會顯示在清單中。 請注意，解密密鑰對是在沒有到期日的情況下生成的。

您可以使用 **...** 按鈕，以下載公開金鑰或複製其指紋。

![](assets/gpg_generate_list.png)

公共密鑰隨後可用於與任何外部系統共用。 Adobe Campaign將能夠在資料載入活動中使用私密金鑰來解密使用公開金鑰加密的資料。

如需詳細資訊，請參閱Adobe Campaign檔案：

| Campaign Classic | Campaign Standard |
---------|----------
| [在處理前解壓縮或解密檔案](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#unzipping-or-decrypting-a-file-before-processing) | [管理加密的資料](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/importing-data.html#managing-encrypted-data) |
| [資料載入（檔案）活動](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/action-activities/data-loading--file-.html) | [載入檔案活動](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/load-file.html) |