---
title: 管理子網域的SSL憑證
description: 瞭解如何監控子網域的SSL憑證並啟動其續約程式
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# 管理子網域的SSL憑證 {#managing-subdomains-ssl-certificates}

此 **[!UICONTROL Subdomains and Certificates]** 卡可讓您查看您的登陸頁面和資源所在的子網域和相關子網域，以及安裝了SSL憑證的子網域。 您也可以輕鬆查看哪些子網域有過期的憑證，以便預測其過期。

如果憑證即將到期，您就可以使用所有必要資訊來啟動客戶服務要求，以續約憑證並確保執行個體正常運作。

>[!NOTE]
>
>Adobe 建議您在相關子網域的 SSL 憑證&#x200B;**接近到期日時**&#x200B;進行更新。根據您的組織而定，憑證更新可能需要數天的時間，我們建議您為此程序分配適當的時間。

## 監控SSL憑證 {#monitoring-ssl-certificates}

選取資訊卡時，可直接存取每個例項的子網域清 **[!UICONTROL Subdomains & Certificates]** 單。

子網域依SSL憑證的最近到期日排列，並提供過期的視覺化資訊（以天為單位）:

* **綠色**:子網域未在未來60天內到期的憑證。
* **橙色**:一或多個子網域有一個憑證，將在未來60天內到期。
* **紅色**:一或多個子網域有一個憑證，將在未來30天內到期。

![](assets/visual_alert2.png)

To get more details on a subdomain's certificates, click the **[!UICONTROL Certificate Details]** button.

![](assets/certificate_details4.png)

所有相關子網域的清單都會顯示在其憑證上。 它通常包含著陸頁面、資源頁面等的子網域。

![](assets/monitoring_subdomains_details2.png)

如有必要，您可以從此窗口啟動證書續約請求。 有關此的詳細資訊，請參閱以下章節。

## 啟動SSL憑證續約 {#initiating-ssl-certificate-renewal}

>[!NOTE]
>
>控制面板不會自動管理憑證續約。 它只允許您準備 **要傳送至Adobe Campaign客戶服務的請求** ，以開始續約程式。

SSL憑證續約程式包含3個步驟：

1. **產生憑證簽署要求(CSR)** Adobe客戶服務會根據透過客戶服務入口網站提出的要求，為您產生CSR。 您需要提供產生CSR所需的一些資訊（例如公用名稱、組織名稱和地址等）。 在「控制面板」中，您可以在開始續約程式時看到所需項目的清單。 有關此的詳細資訊，請參閱以下章節。
1. **購買SSL憑證**&#x200B;當客戶服務產生CSR後，您就可以下載SSL憑證，並從您公司核准的認證授權機構購買SSL憑證。
1. **安裝SSL憑證購**&#x200B;買SSL憑證後，您必須將它提供給Adobe客戶服務。 將會安裝憑證，您會在控制面板中看到憑證的更新到期日。

要在「控制面板」中啟動SSL證書續約，請執行以下步驟：

1. Open the **[!UICONTROL Subdomains & Certificates]** card, then click the **[!UICONTROL Certificate details]** icon of the subdomain with expiring certificates.

   ![](assets/renewal1.png)

1. 隨即顯示相關子網域的清單。這通常會包括登陸頁面、資源頁面等等的子網域。Click the **[!UICONTROL Ticket Details]** button to initiate the certificates renewal process.

   ![](assets/renewal2.png)

1. 會顯示表單，並提供續約SSL憑證所需的所有詳細資訊。 確保完整、正確地填寫所要求的資訊（如有必要，請連絡您的內部團隊、安全性和IT團隊）。 否則，無法產生憑證簽署要求，您將無法續約憑證。

   * **[!UICONTROL IMS Org]**:組織的ID。
   * **[!UICONTROL Instance]**:與子網域關聯的促銷活動例項URL。
   * **[!UICONTROL Common name]**:這通常是追蹤子網域URL，與即將過期的憑證的子網域相關聯。
   * **[!UICONTROL Subdomains]**:連結至具有過期憑證之子網域的子網域。 如果您想要將單一SSL憑證套用至其他子網域，則可將其新增至此清單。 在這種情況下，請確定這些子網域與相同的IMS組織和例項URL相關聯。
   >[!CAUTION]
   >
   >The **[!UICONTROL IMS Org]** and **[!UICONTROL Instance]** fields are filled in automatically by the Control Panel and should not be modified.

   ![](assets/renewal3.png)

1. 表單完成後，按一下按 **[!UICONTROL Copy Details]** 鈕將資訊儲存到剪貼簿。

   >[!NOTE]
   >
   >如果您未清除瀏覽器歷史記錄，您輸入的資訊將會儲存，讓您稍後使用它來續約憑證。

1. Click the **[!UICONTROL Log new ticket]** button. 系統會自動將您重新導向至「Adobe Campaign客戶服務登入頁面」。

   ![](assets/renewal4.png)

1. 登入，然後使用「SSL憑證CSR要求」主旨建立新的支援票證。
將先前複製的所有資訊貼入票證正文，然後按一下「提交」。

   >[!NOTE]
   >
   >如果您沒有為組織歸檔支援案例的權限，請將您複製到剪貼簿的所有資訊傳遞給您的支援聯繫人，並請他們為您開啟新的客戶服務票證。

**相關主題：**

* [Campaign standard教學課程影片](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/managing-ssl-certificates.html)
* [Campaign Classic教學課程影片](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-ssl-certificates.html)
