---
product: campaign
solution: Campaign
title: GPG 金鑰管理
description: 瞭解如何管理 GPG 金鑰，以在 Adobe Campaign 中加密和解密資料。
feature: Control Panel, Encryption
role: Admin
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: de33a10a168358d0f38ca776fbcd88e0ccf63ce2
workflow-type: ht
source-wordcount: '1146'
ht-degree: 100%

---

# GPG 金鑰管理 {#gpg-keys-management}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_gpg_management"
>title="關於 GPG 金鑰"
>abstract="在此索引標籤中，您可在行銷執行個體上安裝和/或產生 GPG 金鑰，以將傳送自 Campaign 的資料加密並將傳入的資料解密。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=zh-Hant" text="關於效能監視"

## 關於 GPG 加密 {#about-gpg-encryption}

GPG 加密可讓您使用一套公私金鑰配對，並遵循 [OpenPGP](https://www.openpgp.org/about/standard/) 規範保護您的資料。

實施之後，您可以在傳輸前解密傳入資料，並加密傳出資料，以確保沒有有效相符金鑰配對的任何人都不會存取這些資料。

若要使用 Campaign 實施 GPG 加密，管理員使用者必須直接從控制面板在行銷執行個體安裝及/或產生 GPG 金鑰。

之後，您將能夠：

* **加密已傳送的資料**：使用已安裝的公開金鑰加密資料後，Adobe Campaign 會傳送資料。

* **解密傳入的資料**：Adobe Campaign 會從外部系統接收使用從「控制面板」下載的公開金鑰加密的資料。 Adobe Campaign 會使用從「控制面板」產生的私密金鑰來解密資料。

## 加密資料 {#encrypting-data}

「控制面板」可以讓您加密從 Adobe Campaign 執行個體傳出的資料。

為此，您需要從 PGP 加密工具產生 GPG 金鑰配對，然後將公開金鑰安裝到「控制面板」。之後，您就可以在從執行個體傳送資料之前先加密資料。請依照下列步驟以執行此操作。

>[!NOTE]
>
>您最多可以在「控制面板」中安裝 60 個 GPG 金鑰。

![](assets/do-not-localize/how-to-video.png)在[影片](#video)中探索此功能

1. 使用 PGP 加密工具，按照 [OpenPGP 規範](https://www.openpgp.org/about/standard/)產生公開/私密金鑰配對。要執行此操作，請安裝 GPG 公用程式或 GNuGP 軟體。

   >[!NOTE]
   >
   >可使用開放原始碼免費軟體來產生金鑰。 不過，請務必遵循組織的方針，並使用您的 IT/安全組織建議的 GPG 公用程式。

1. 安裝公用程式後，在 Mac 終端機或 Windows 命令中執行以下命令。

   `gpg --full-generate-key`

1. 出現提示時，請為您的金鑰指定所需的參數。必要的參數包括：

   * **金鑰類型**：RSA
   * **金鑰長度**：3072 - 4096 位元
   * **實際名稱**&#x200B;和&#x200B;**電子郵件地址**：允許追蹤誰建立了金鑰配對。輸入連結至組織或部門的名稱和電子郵件地址。
   * **評論**：在評論欄位中新增標籤，可協助您輕鬆識別用來加密資料的金鑰。
     >[!IMPORTANT]
     >
     >確定此欄位未留空且已填入註解。

   * **期限**：日期或以「0」表示無過期日期。
   * **複雜密碼**

   ![](assets/do-not-localize/gpg_command.png)

1. 確認後，指令碼會以其相關聯的指紋產生金鑰，您可將其匯出至檔案，或直接貼至「控制面板」。若要匯出檔案，請執行此命令，後面加上您產生的金鑰指紋。

   `gpg -a --export <fingerprint>`

1. 若要將公開金鑰安裝至「控制面板」，請開啟&#x200B;**[!UICONTROL 執行個體設定]**&#x200B;卡片，然後選取 **[!UICONTROL GPG 金鑰]**&#x200B;標籤與所需的執行個體。

1. 按一下&#x200B;**[!UICONTROL 安裝金鑰]**&#x200B;按鈕。

   ![](assets/gpg_install_button.png)

1. 貼上從 PGP 加密工具產生的公開金鑰。 您也可以直接拖放您匯出的公開金鑰檔案。

   >[!NOTE]
   >
   >公開金鑰應為 OpenPGP 格式。

   ![](assets/gpg_install_paste.png)

1. 按一下&#x200B;**[!UICONTROL 安裝金鑰]**&#x200B;按鈕。

安裝公開金鑰後，其隨即會顯示於清單中。 您可以使用 **...** 按鈕，來下載或複製其指紋。

![](assets/gpg_install_download.png)

然後即可在 Adobe Campaign 工作流程中使用該金鑰。 使用資料擷取活動時，您可以用其來加密資料。

![](assets/do-not-localize/how-to-video.png)在[影片](#video)中探索此功能

如需有關此主題的詳細資訊，請參閱 Adobe Campaign 文件：

**Campaign v7/v8：**

* [壓縮或加密檔案](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=zh-Hant)
* [使用案例：使用安裝於「控制面板」的金鑰加密和匯出資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=zh-Hant#use-case-gpg-encrypt)

**Campaign Standard:**

* [管理已加密的資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=zh-Hant)
* [使用案例：使用安裝於「控制面板」的金鑰加密和匯出資料](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=zh-Hant#use-case-gpg-encrypt)

## 解密資料 {#decrypting-data}

「控制面板」可以讓您將傳入 Adobe Campaign 執行個體的外部資料解密。

若要執行此操作，您需要直接從「控制面板」產生 GPG 金鑰配對。

* **公開金鑰**&#x200B;將與外部系統共用，外部系統會用其來加密要傳送至 Campaign 的資料。
* **私密金鑰**&#x200B;將由 Campaign 用來將傳入的加密資料解密。

![](assets/do-not-localize/how-to-video.png)在[影片](#video)中探索此功能

若要在「控制面板」中產生金鑰配對，請依照下列步驟進行：

1. 開啟&#x200B;**[!UICONTROL 執行個體設定]**&#x200B;卡片，然後選取 **[!UICONTROL GPG 金鑰]**&#x200B;標籤和所需的 Adobe Campaign 執行個體。

1. 按一下&#x200B;**[!UICONTROL 產生金鑰]**&#x200B;按鈕。

   ![](assets/gpg_generate.png)

1. 指定金鑰的名稱，然後按一下&#x200B;**[!UICONTROL 產生金鑰]**。此名稱可協助您識別用於 Campaign 工作流程解密的金鑰

   ![](assets/gpg_generate_name.png)

產生金鑰配對後，公開金鑰隨即顯示在清單中。請注意，產生解密金鑰配對時沒有過期日。

您可以使用 **...** 按鈕，以下載公開金鑰或複製其指紋。

![](assets/gpg_generate_list.png)

然後，便可與任何外部系統共用該公開金鑰。Adobe Campaign 能夠使用資料載入活動中的私密金鑰，將以公開金鑰加密的資料進行解密。

如需詳細資訊，請參閱 Adobe Campaign 文件：

**Campaign v7 與 v8：**

* [在處理前解壓縮或解密檔案](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=zh-Hant)
* [使用案例：匯入使用「控制面板」產生的金鑰加密的資料](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=zh-Hant#use-case-gpg-decrypt)

**Campaign Standard:**

* [管理已加密的資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=zh-Hant)
* [使用案例：匯入使用「控制面板」產生的金鑰加密的資料](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=zh-Hant#use-case-gpg-decrypt)

## 監視 GPG 金鑰

若要存取為執行個體安裝和產生的 GPG 金鑰，請開啟&#x200B;**[!UICONTROL 執行個體設定]**&#x200B;卡片，然後選取 **[!UICONTROL GPG 金鑰]**&#x200B;標籤。

![](assets/gpg_list.png)

此清單會顯示已安裝並為執行個體產生的所有加密和解密 GPG 金鑰，以及每個金鑰的詳細資訊：

* **[!UICONTROL 名稱]**：安裝或產生金鑰時定義的名稱。
* **[!UICONTROL 使用案例]**：此欄指定金鑰的使用案例：

  ![](assets/gpg_icon_encrypt.png)：已安裝用於資料加密的金鑰。

  ![](assets/gpg_icon_decrypt.png)：金鑰已產生以允許資料進行解密。

* **[!UICONTROL 指紋]**：金鑰的指紋。
* **[!UICONTROL 過期]**：金鑰的過期日期。 請注意，「控制面板」會在接近金鑰到期日時提供視覺指示：

   * 緊急 (紅色) 會在 30天 前顯示。
   * 警告 (黃色) 會在 60 天前顯示。
   * 金鑰到期後，將會顯示「已到期」紅色橫幅。

  >[!NOTE]
  >
  >請注意，「控制面板」不會傳送任何電子郵件通知。

根據最佳實務，建議您移除任何不再需要的金鑰。 若要執行此操作，請按一下 **...** 按鈕，然後選取&#x200B;**[!UICONTROL 刪除金鑰]。**

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>在移除金鑰之前，請確定其並未用於任何 Adobe Campaign 工作流程，以避免其失敗。

## 教學課程影片 {#video}

以下影片說明如何產生和安裝用於資料加密的 GPG 金鑰。

其他有關 GPG 金鑰管理的作法影片，請參閱 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=zh-Hant#instance-settings) 和 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=zh-Hant#instance-settings) 教學課程頁面。

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)
