---
product: campaign
solution: Campaign
title: 設定新的子網域
description: 瞭解如何為您的 Campaign 執行個體設定新的子網域
translation-type: tm+mt
source-git-commit: 2d84a5ebe8dbf42264c94f882a51180aae2a58a6
workflow-type: tm+mt
source-wordcount: '1140'
ht-degree: 47%

---


# 設定新的子網域{#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="設定新的子網域和管理憑證"
>abstract="您必須設定新的子網域和管理子網域的 SSL 憑證，才能開始使用 Adobe Campaign 傳送電子郵件或發佈登陸頁面。"
>additional-url="https://docs.adobe.com/content/help/zh-Hant/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="如何監視子網域的 SSL 憑證"

## 必讀 {#must-read}

>[!IMPORTANT]
>
>「控制面板」的子網域設定提供測試版，而且必須經常更新和修改，恕不另行通知。

本頁提供如何使用完整子網域委派或CNAME來設定新子網域的資訊。 本節將介紹這兩種方法的全局概念：[子網域品牌推廣](../../subdomains-certificates/using/subdomains-branding.md)。

**相關主題：**

* [監視子網域](../../subdomains-certificates/using/monitoring-subdomains.md)

### 實例選擇

子域配置僅適用於&#x200B;**production**&#x200B;實例。

如果您在嚮導中選擇的實例先前沒有設定子域，則第一個配置的子域將成為該實例的&#x200B;**主子域**，而您將來將無法更改該子域。

因此，將使用此主子域為其他子域建立&#x200B;**反向DNS記錄**。 **其他子網域的回覆和退信地址會從主要子網域產生。**

### 命名空間配置

設定命名伺服器時，請務必&#x200B;**不要將根子網域委派給 Adobe**。否則，網域只能與 Adobe 搭配使用。您不能用於任何其他用途，例如傳送內部電子郵件給您組織的員工。

此外，**請勿為此新子網域建立個別的區域檔案**。

## 完全子網域委派{#full-subdomain-delegation}

若要將子網域完全委派至Adobe Campaign，請遵循下列步驟。

![](assets/do-not-localize/how-to-video.png) 使用促銷活動類別或促銷活動標 [準來](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=en#subdomains-and-certificates) 探索視 [訊中的這項功能](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=en#subdomains-and-certificates)

1. 在「**[!UICONTROL Subdomains & Certificates]**」卡片中，選取所需的生產執行個體，再按一下「**[!UICONTROL Setup new subdomain]**」。

   ![](assets/subdomain1.png)

1. 按一下　**[!UICONTROL Next]**　以確認完全委派方法。

   ![](assets/subdomain3.png)

1. 在您組織使用的託管解決方案中，建立所需的子網域和名稱伺服器。若要這麼做，請複製並貼上精靈中顯示的 Adobe Nameserver 資訊。如需進一步瞭解如何在託管解決方案中建立子網域，請參考[教學課程影片](https://video.tv.adobe.com/v/30175?captions=chi_hant)。

   ![](assets/subdomain4.png)

1. 使用對應的 Adobe 名稱伺服器資訊建立子網域後，請按一下「**[!UICONTROL Next]**」。

1. 如果您選取了Campaign Classic例項，請為子網域選取所需的使用案例：**行銷通訊**&#x200B;或&#x200B;**交易與營運通訊**。 有關子域使用案例的全局概念在[本節](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases)中介紹。

   ![](assets/subdomain5.png)

1. 輸入您建立到託管解決方案的子網域，再按一下「**[!UICONTROL Submit]**」。

   請務必填寫要委派之子網域的&#x200B;**完整名稱**。舉例來說，若要委派「usoffers.email.weretail.com」子網域，請輸入「usoffers.email.weretail.com」。

   ![](assets/subdomain6.png)

提交子域後，控制面板將執行各種檢查和配置步驟。 有關詳細資訊，請參閱[子域檢查和配置](#subdomain-checks-and-configuration)。

## 子網域設定使用 CNAME {#use-cnames}

若要使用CNAME來設定子網域，請遵循下列步驟。

![](assets/do-not-localize/how-to-video.png) 使用促銷活動類別或促銷活動標 [準來](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=en#subdomains-and-certificates) 探索視 [訊中的這項功能](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=en)

1. 在「**[!UICONTROL Subdomains & Certificates]**」卡片中，選取所需的生產執行個體，再按一下「**[!UICONTROL Setup new subdomain]**」。

   ![](assets/subdomain1.png)

1. 選擇&#x200B;**[!UICONTROL CNAME]**&#x200B;方法，然後按一下&#x200B;**[!UICONTROL Next]**。

   ![](assets/cname-method-selection.png)

1. 如果您選取了Campaign Classic例項，請為子網域選取所需的使用案例：**行銷通訊**&#x200B;或&#x200B;**交易與營運通訊**。 有關子域使用案例的全局概念在[本節](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases)中介紹。

   ![](assets/cname-use-case.png)

1. 輸入您建立到託管解決方案的子網域，再按一下「**[!UICONTROL Next]**」。

   請務必填寫要設定的子網域&#x200B;**全稱**。 例如，若要設定&quot;usoffers.email.weretail.com&quot;子網域，請輸入&quot;usoffers.email.weretail.com&quot;。

   ![](assets/cname-submit.png)

1. 將顯示要放置在DNS伺服器中的記錄清單。 逐一複製這些記錄，或下載CSV檔案，然後導覽至您的網域代管解決方案，以產生相符的DNS記錄。

   ![](assets/cname-generate-record.png)

1. 請確定先前步驟中的所有DNS記錄都已產生至您的網域代管解決方案。 如果所有項目都已正確設定，請選取第一個陳述式，然後按一下&#x200B;**[!UICONTROL Submit]**&#x200B;以確認。

   ![](assets/cname-confirmation.png)

   >[!NOTE]
   >
   >如果要建立記錄並稍後提交子域配置，請選擇第二個語句，然後按一下&#x200B;**[!UICONTROL Submit later]**。 然後，您就可以直接從子域管理螢幕&#x200B;**[!UICONTROL Processing]**&#x200B;區域恢復子域配置。
   >
   >請注意，要放置在伺服器上的DNS記錄將由控制面板保存30天。 在這段期間之後，您必須從頭開始設定子網域。

提交子域後，控制面板將執行各種檢查和配置步驟。 有關詳細資訊，請參閱[子域檢查和配置](#subdomain-checks-and-configuration)。

## 子域檢查和配置{#subdomain-checks-and-configuration}

1. 提交子域後，控制面板將檢查它是否正確指向Adobe NS記錄，以及此子域不存在授權開始(SOA)記錄。

   >[!NOTE]
   >
   >請注意，當子網域設定執行時，控制面板中的其他要求將會進入佇列，並僅在子網域設定完成後才執行，以避免任何效能問題。

1. 如果檢查成功，「控制面板」將會開始設定包含 DNS 記錄、其他 URL、收件箱等等的子網域。

   ![](assets/subdomain7.png)

   按一下子域配置&#x200B;**[!UICONTROL Details]**&#x200B;按鈕，可以獲取有關配置進度的詳細資訊。

   ![](assets/subdomain_audit.png)

1. 最後，**傳遞團隊**&#x200B;將會收到關於新子網域的通知，以便稽核該子網域。在子網域設定後，稽核程式最多需要10個工作天。

   >[!IMPORTANT]
   >
   >執行的傳遞性檢查包括反饋迴路和垃圾郵件投訴迴路測試。 因此，我們不建議在稽核完成之前使用子網域，因為這可能導致子網域信譽不佳。

1. 程序結束時，子網域將設定為與您的 Adobe Campaign 執行個體搭配使用，並會建立下列元素：

   * 具有下列 DNS 記錄&#x200B;**的**&#x200B;子網域：SOA、MX、CNAME、DKIM、SPF、TXT，
   * 託管鏡射、資源、追蹤頁面和網域金鑰的&#x200B;**其他子網域**，
   * **收件匣**：寄件人、錯誤、回覆。

   依預設，「控制面板」的「回覆」收件匣會設為清除電子郵件，且無法重新檢視。如果您想要監視行銷活動的「回覆」收件匣，請勿使用此位址。

您可以按一下 **[!UICONTROL Subdomain details]**&#x200B;和 **[!UICONTROL Sender info]** 按鈕，以取得子網域的詳細資訊。

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## 疑難排解 {#troubleshooting}

* 在某些情況下，子網域配置會完成，但子網域可能無法成功驗證。 會將子網域持續列在 **[!UICONTROL Configured]** 清單中，而且會包含作業記錄，其中會提供關於錯誤的資訊。如果您無法解決問題，請聯絡客戶服務。
* 如果在設定後，子網域顯示為「未驗證」，請啟動新的子網域驗證　(**...** / **[!UICONTROL Verify subdomain]**)。如果它仍顯示相同的狀態，原因可能是對收件者架構進行某些自訂，而無法使用標準流程進行驗證。請嘗試使用該子網域傳送行銷活動。
* 如果子網域設定在進行傳遞稽核步驟時花費太長時間（超過 10 個工作日），請聯繫客戶服務。
