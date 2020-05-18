---
title: 續約子網域的SSL憑證
description: 瞭解如何續約子網域的SSL憑證
translation-type: tm+mt
source-git-commit: bc29433167d4699ad9b840381abd0d5bbff8c630
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---


# 續約子網域的SSL憑證 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="新增SSL憑證"
>abstract="若要新增SSL憑證，您必須產生CSR、購買子網域的SSL憑證並安裝憑證套裝。"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="產生憑證簽署要求(CSR)"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="如何安裝SSL憑證"

>[!IMPORTANT]
>
>從「控制面板」進行子網域委派的測試版可供使用，但必須經常更新和修改，恕不另行通知。

## 關於憑證續約 {#about-certificate-renewal-process}

SSL憑證續約程式包含3個步驟：

1. **產生憑證簽署要求(CSR)** Adobe客戶服務會為您產生CSR。 您需要提供產生CSR所需的一些資訊（例如公用名稱、組織名稱和地址等）。
1. **購買SSL憑證**&#x200B;當產生CSR後，您就可以下載CSR，並使用它從您公司核准的認證授權機構購買SSL憑證。
1. **安裝SSL憑證**&#x200B;購買SSL憑證後，即可將它安裝在所需的子網域上。

## 產生憑證簽署要求(CSR) {#generating-csr}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="生成CSR"
>abstract="您必須在購買憑證之前，先針對您打算保護的例項和子網域產生憑證簽署要求。"

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="選擇CSR的子域"
>abstract="您可以選擇將所有或僅特定子網域納入您的認證簽署請求。 只有選取的子網域才會透過購買的SSL憑證取得認證。"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="產生憑證簽署要求(CSR)"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="關於子網域品牌"

若要產生憑證簽署要求(CSR)，請遵循下列步驟：

1. 在資訊 **[!UICONTROL Subdomains & Certificates]** 卡中，選取所要的例項，然後按一下 **[!UICONTROL Manage Certificate]** 按鈕。

   ![](assets/renewal1.png)

1. 選 **[!UICONTROL 1 - Generate a CSR]**&#x200B;擇，然 **[!UICONTROL Next]** 後按一下啟動嚮導，引導您完成CSR生成過程。

   ![](assets/renewal2.png)

1. 此時會顯示表單，其中包含產生CSR所需的所有詳細資訊。

   請確定您完整且正確地填寫所要求的資訊，否則不會續約憑證（如有必要，請連絡您的內部團隊、安全性和IT團隊），然後按一下 **[!UICONTROL Next]**。

   * **[!UICONTROL Organization]**: 正式組織名稱。
   * **[!UICONTROL Organization Unit]**: 連結至子網域的單位(範例： 行銷，IT)。
   * **[!UICONTROL Instance]** （預填）: 與子網域相關聯之促銷活動例項的URL。
   ![](assets/renewal3.png)

1. 選擇要包含在CSR中的子域，然後按一下 **[!UICONTROL OK]**。

   ![](assets/renewal4.png)

1. 選定的子網域會顯示在清單中。 針對每個子網域，選取要包含的子網域，然後按一下 **[!UICONTROL Next]**。

   ![](assets/renewal5.png)

1. 將顯示要包括在CSR中的子域的概要。 按一 **[!UICONTROL Submit]** 下以確認您的請求。

   ![](assets/renewal6.png)

1. 系統會自動產生並下載與您選取範圍對應的。csr檔案。 您現在可以使用它，從您公司核准的認證機構購買SSL憑證。

   >[!NOTE]
   >
   >如果CSR未儲存／下載，則會遺失，您必須重新產生。

## 向CSR購買證書 {#purchasing-certificate}

從「控制面板」取得「認證簽署要求CSR」後，請向貴組織核准的認證機構購買SSL憑證。

## 安裝SSL憑證 {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="安裝SSL憑證"
>abstract="安裝您從貴組織核准的認證機構購買的SSL憑證。"
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="關於子網域品牌"

在購買SSL憑證後，您就可以將它安裝在您的例項上。 在繼續之前，請確定您已瞭解下列必要條件：

* 憑證簽署要求(CSR)必須是從「控制面板」產生。 否則，您將無法從「控制面板」安裝憑證。
* 憑證簽署要求(CSR)應符合已委派給Adobe的子網域。 例如，它不能包含已委託的子網域。
* 憑證應具有目前的日期。 將來無法安裝具有日期的憑證，也不應過期（即有效的開始日期和結束日期）。
* 憑證應由受信任的憑證授權機構(CA)核發，例如Comodo、DigiCert、GoDaddy等。
* 憑證大小應為2048位元，演算法應為RSA。
* 憑證應為X.509 PEM格式。
* 支援SAN證書。
* 不支援萬用字元憑證。
* ZIP檔案或憑證不應受密碼保護。
* ZIP檔案最好在個別檔案中僅包含下列內容：
   * 終端實體憑證。
   * 中級憑證鏈（依適當順序排列）。
   * 根證書（可選）。

若要安裝憑證，請依照下列步驟進行：

1. 在資訊 **[!UICONTROL Subdomains & Certificates]** 卡中，選取所要的例項，然後按一下 **[!UICONTROL Manage Certificate]** 按鈕。

   ![](assets/renewal1.png)

1. 選 **[!UICONTROL 3 - Install Certificate Bundle]**&#x200B;擇，然後單 **[!UICONTROL Next]** 擊啟動嚮導，該嚮導將引導您完成證書安裝過程。

   ![](assets/install1.png)

1. 選取包含要安裝之憑證的。zip檔案，然後按一下 **[!UICONTROL Submit]**。

   ![](assets/install2.png)

>[!NOTE]
>
>此憑證將安裝在CSR中包含的所有網域／子網域上。 證書中存在的任何附加域／子域都不會被考慮在內。

安裝SSL憑證後，憑證的到期日和狀態圖示會隨之更新。

**相關主題：**

* [新增SSL憑證（教學課程影片）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [子網域品牌](../../subdomains-certificates/using/subdomains-branding.md)
* [監控子網域](../../subdomains-certificates/using/monitoring-subdomains.md)