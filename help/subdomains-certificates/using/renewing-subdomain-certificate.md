---
title: 續約子網域的SSL憑證
description: 瞭解如何續約子網域的SSL憑證
translation-type: tm+mt
source-git-commit: 2c5a4f4f48e975bd9c9de4a86d2691cfddf58354

---


# 續約子網域的SSL憑證 {#renewing-subdomains-ssl-certificates}

>[!NOTE]
>
>在1月底，將提供從控制面板續約憑證的測試版。

## 關於憑證續約 {#about-certificate-renewal-process}

SSL憑證續約程式包含3個步驟：

1. **產生憑證簽署要求(CSR)** Adobe客戶服務會為您產生CSR。 您需要提供產生CSR所需的一些資訊（例如公用名稱、組織名稱和地址等）。
1. **購買SSL憑證**&#x200B;當產生CSR後，您就可以下載CSR，並使用它從您公司核准的認證機構購買SSL憑證。
1. **安裝SSL憑證**&#x200B;購買SSL憑證後，即可將它安裝在所需的子網域上。

>[!NOTE]
>
>只有完全授權的子網域才能透過「控制面板」 **續約SSL憑證** 。

## 產生憑證簽署要求(CSR) {#generating-csr}

若要產生憑證簽署要求(CSR)，請遵循下列步驟：

1. 在資訊 **[!UICONTROL Subdomains & Certificates]**卡中，選取所要的例項，然後按一下**[!UICONTROL Manage Certificate]** 按鈕。

   ![](assets/renewal1.png)

1. 選 **[!UICONTROL Generate a CSR]**擇，然**[!UICONTROL Next]** 後按一下啟動嚮導，引導您完成CSR生成過程。

   ![](assets/renewal2.png)

1. 此時會顯示表單，其中包含產生CSR所需的所有詳細資訊。

   請確定您完整且正確地填寫所要求的資訊，否則不會續約憑證（如有必要，請連絡您的內部團隊、安全性和IT團隊），然後按一下 **[!UICONTROL Next]**。

   * **[!UICONTROL Organization]**:正式組織名稱。
   * **[!UICONTROL Organization Unit]**:連結至子網域的單位(範例：行銷，IT)。
   * **[!UICONTROL Instance]**（預填）:與子網域相關聯之促銷活動例項的URL。
   ![](assets/renewal3.png)

1. 選擇要包含在CSR中的子域，然後按一下 **[!UICONTROL OK]**。

   ![](assets/renewal4.png)

1. 選定的子網域會顯示在清單中。 針對每個子網域，選取要包含的子網域，然後按一下 **[!UICONTROL Next]**。

   ![](assets/renewal5.png)

1. 將顯示要包括在CSR中的子域的概要。 按一 **[!UICONTROL Submit]**下以確認您的請求。

   ![](assets/renewal6.png)

1. 系統會自動產生並下載與您選取範圍對應的。csr檔案。 您現在可以使用它，從您公司核准的認證機構購買SSL憑證。

## 向CSR購買證書 {#purchasing-certificate}

從「控制面板」取得「認證簽署要求CSR」後，請向貴組織核准的認證機構購買SSL憑證。

## 安裝SSL憑證 {#installing-ssl-certificate}

在購買SSL憑證後，您就可以將它安裝在您的例項上。 在繼續之前，請確定您已瞭解下列必要條件：

* 憑證簽署要求(CSR)必須是從「控制面板」產生。 否則，您將無法從「控制面板」安裝憑證。
* 請確定憑證簽署要求(CSR)符合已委派給Adobe的子網域。 例如，它不能包含已委託的子網域。
* 憑證必須有目前的日期。 將來無法安裝具有日期的憑證。

若要安裝憑證，請依照下列步驟進行：

1. 在資訊 **[!UICONTROL Subdomains & Certificates]**卡中，選取所要的例項，然後按一下**[!UICONTROL Manage Certificate]** 按鈕。

   ![](assets/renewal1.png)

1. 按一 **[!UICONTROL Install SSL Certificate]**下，**[!UICONTROL Next]** 然後啟動精靈，引導您完成憑證安裝程式。

   ![](assets/install1.png)

1. 選取包含要安裝之憑證的。zip檔案，然後按一下 **[!UICONTROL Submit]**。

   ![](assets/install2.png)

安裝SSL憑證後，憑證的到期日和狀態圖示會隨之更新。

您的子網域URL位址將從 **http** 變 **更**。
