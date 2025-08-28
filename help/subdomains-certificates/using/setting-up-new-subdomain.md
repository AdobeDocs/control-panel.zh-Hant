---
product: campaign
solution: Campaign
title: 設定新的子網域
description: 瞭解如何為您的 Campaign 執行個體設定新的子網域
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: d92781c3-14cc-4716-a131-580ccff46d6e
source-git-commit: 0b7cb860592508f7323bcd30345d1853e4a4ac94
workflow-type: tm+mt
source-wordcount: '1526'
ht-degree: 99%

---


# 設定新的子網域 {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="設定新的子網域和管理憑證"
>abstract="您必須設定新的子網域和管理子網域的 SSL 憑證，才能開始使用 Adobe Campaign 傳送電子郵件或發佈登陸頁面。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=zh-Hant" text="監視 SSL 憑證"

## 必讀 {#must-read}

本頁面提供如何透過完整子網域委派或 CNAME 來設定新子網域的資訊。 本章節將介紹這兩種方法的全域概念：[子網域品牌化](../../subdomains-certificates/using/subdomains-branding.md)。

**相關主題：**

* [監視子網域](../../subdomains-certificates/using/monitoring-subdomains.md)

### 執行個體選擇

子網域設定僅適用於&#x200B;**生產**&#x200B;執行個體。

如果您在精靈中選擇的執行個體先前沒有設定子網域，則第一個設定的子網域將成為該執行個體的&#x200B;**主要子網域**，而日後您將無法變更該子網域。因此，將利用此主子網域為其他子網域建立&#x200B;**反向 DNS 記錄**。 **其他子網域的回覆和退信地址會由主要子網域產生。**

### 將子網域的 SSL 憑證委派給 Adobe

設定新的子網域時，您可以讓 Adobe 管理 SSL 憑證。 強烈建議您這樣做，因為 Adobe 每年都會在憑證到期前，自動建立並更新憑證。

如果您使用 CNAME 來設定子網域委派，Adobe 將提供憑證記錄，以用於網域託管解決方案來產生憑證。

>[!NOTE]
>
>Adobe 受管理 SSL 是免費提供給使用者的功能。[了解更多 SSL 憑證管理相關資訊](monitoring-ssl-certificates.md#management)

### 名稱伺服器設定

設定命名伺服器時，請務必&#x200B;**不要將根子網域委派給 Adobe**。否則，網域只能與 Adobe 搭配使用。您不能用於任何其他用途，例如傳送內部電子郵件給您組織的員工。

此外，**請勿為此新子網域建立個別的區域檔案**。

## 完全子網域委派 {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="cp_add_new_subdomain"
>title="新增新的子網域"
>abstract="Adobe 建議完全委派子網域。 不過，您可以使用 CNAME 或自訂方法來設定子網域。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=zh-Hant" text="設定新的子網域"
>additional-url="https://helpx.adobe.com/tw/enterprise/using/support-for-experience-cloud.html" text="聯絡客戶服務"

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_create_delegate"
>title="建立並委派子網域"
>abstract="建立您要在托管解決方案中與 Adobe Campaign 搭配使用的子網域，並將其委派給 Adobe。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=zh-Hant" text="設定新的子網域"

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_submit"
>title="提交您的子網域"
>abstract="確認並提交在先前步驟中設定的子網域。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=zh-Hant" text="設定新的子網域"

若要將子網域完全委派給 Adobe Campaign，請執行以下步驟。

![](assets/do-not-localize/how-to-video.png)在利用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=zh-Hant#subdomains-and-certificates) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/subdomain-delegation.html?lang=zh-Hant#subdomains-and-certificates) 的影片中瞭解此功能

1. 在&#x200B;**[!UICONTROL 子網域和憑證]**&#x200B;卡片中，選取所需的生產執行個體，然後按一下&#x200B;**[!UICONTROL 設定新子網域]**。

   ![](assets/subdomain1.png)

1. 按一下&#x200B;**[!UICONTROL 下一步]**&#x200B;以確認採取完全委派的方法。

   ![](assets/subdomain3.png)

1. 在您組織使用的託管解決方案中，建立所需的子網域和名稱伺服器。若要這麼做，請複製並貼上精靈中顯示的 Adobe Nameserver 資訊。如需進一步瞭解如何在託管解決方案中建立子網域，請參考[教學課程影片](https://video.tv.adobe.com/v/30175)。

   >[!NOTE]
   >
   > 對於 Adobe Campaign Standard，委派的子網域可讓您同時傳送&#x200B;**行銷**&#x200B;和&#x200B;**異動**&#x200B;通訊。

   ![](assets/subdomain4.png)

1. 在使用對應的 Adobe 名稱伺服器資訊建立子網域後，請按一下&#x200B;**[!UICONTROL 下一步]**。

1. 如果您已選取 Campaign v7/v8 執行個體，請為子網域選取所需的使用案例：**行銷通訊**&#x200B;或&#x200B;**異動和營運通訊**。[本章節](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases)介紹子網域使用案例的全域概念。

   ![](assets/subdomain5.png)

1. 輸入您建立到託管解決方案的子網域，再按一下&#x200B;**[!UICONTROL 提交]**。

   請務必填寫要委派之子網域的&#x200B;**完整名稱**。例如，若要委派「email.weretail.com」子網域，請輸入「email.weretail.com」。


1. 若要委派 Adobe 產生子網域的 SSL 憑證，請啟用&#x200B;**[!UICONTROL 為子網域選擇 Adobe 管理的 SSL]** 選項。 [了解更多 SSL 憑證委派相關資訊](delegate-ssl.md)

   ![](assets/subdomain6.png)

在提交子網域後，控制面板將執行各種檢查及設定步驟。 詳細資訊，請參閱[子網域確認和設定](#subdomain-checks-and-configuration)。

## 利用 CNAME 設定子網域 {#use-cnames}

>[!CONTEXTUALHELP]
>id="cp_add_cname_subdomain_create_delegate"
>title="設定您的子網域"
>abstract="在此畫面中，指定您要使用 CNAME 設定的子網域。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=zh-Hant" text="設定新的子網域"

>[!CONTEXTUALHELP]
>id="cp_add_cname_records"
>title="產生記錄"
>abstract="導覽至您的託管解決方案，以產生此畫面中顯示的 DNS 記錄清單。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=zh-Hant" text="設定新的子網域"

>[!CONTEXTUALHELP]
>id="cp_add_cname_subdomain_submit"
>title="提交您的子網域"
>abstract="確認並提交在先前步驟中設定的子網域。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=zh-Hant" text="設定新的子網域"

若要使用 CNAME 來設定子網域，請遵循下列步驟。

![](assets/do-not-localize/how-to-video.png)在利用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=zh-Hant#subdomains-and-certificates) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html?lang=zh-Hant) 的影片中瞭解此功能

1. 在&#x200B;**[!UICONTROL 子網域和憑證]**&#x200B;卡片中，選取所需的生產執行個體，然後按一下&#x200B;**[!UICONTROL 設定新子網域]**。

   ![](assets/subdomain1.png)

1. 選取 **[!UICONTROL CNAME]** 方法，然後按一下&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/cname-method-selection.png)

1. 如果您已選取 Campaign v7/v8 執行個體，請為子網域選取所需的使用案例：**行銷通訊**&#x200B;或&#x200B;**異動和營運通訊**。 [本章節](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases)介紹子網域使用案例的全域概念。

   ![](assets/cname-use-case.png)

1. 輸入您建立到託管解決方案的子網域。

   若要委派 Adobe 產生子網域的 SSL 憑證，請啟用&#x200B;**[!UICONTROL 為子網域選擇 Adobe 管理的 SSL]** 選項。 [了解更多 SSL 憑證委派相關資訊](delegate-ssl.md)

   ![](assets/cname-adobe-managed.png)

   >[!NOTE]
   >
   >請務必填寫子網域的&#x200B;**完整名稱**&#x200B;以進行設置。舉例來說，若要設定「usoffers.email.weretail.com」子網域，請輸入「usoffers.email.weretail.com」。

1. 要放置在 DNS 伺服器顯示中的記錄清單。 逐一複製這些記錄，或下載 CSV 檔案，然後導覽至您的網域託管解決方案，以產生相符的 DNS 記錄。

   ![](assets/cname-generate-record.png)

1. 請確定先前步驟中的所有 DNS 記錄都已產生至您的網域託管解決方案。 如果所有項目都已正確設定，請選取第一個陳述式，然後按一下&#x200B;**[!UICONTROL 下一步]**&#x200B;以確認。

   如果要建立記錄並稍後提交子網域設定，請選取第二個陳述式。 然後，您就可以直接從子網域管理畫面&#x200B;**[!UICONTROL 處理]**&#x200B;區域恢復子網域設定。請注意，要放置在伺服器上的 DNS 記錄將由控制面板保留 30 天。 在這段期間之後，您必須從頭開始設定子網域。

   >[!NOTE]
   >
   >如果您選擇不將 SSL 憑證委派給 Adobe，這會是子網域設定的最後一個步驟。 按一下&#x200B;**[!UICONTROL 提交]**&#x200B;按鈕。

   ![](assets/cname-confirmation.png)

1. 如果您選擇將子網域的憑證委派給 Adobe，則會自動產生憑證記錄。逐一複製這些記錄，或下載 CSV 檔案，然後瀏覽至網域託管解決方案，以產生相符的憑證。

   ![](assets/cname-csr-generation.png)

1. 請確定已在網域託管解決方案中產生所有憑證記錄。 如果所有項目都已正確設定，請選取第一個陳述式，然後按一下&#x200B;**[!UICONTROL 提交]**&#x200B;以確認。

   ![](assets/cnames-submit.png)

在提交子網域後，控制面板將執行各種檢查及設定步驟。 詳細資訊，請參閱[子網域確認和設定](#subdomain-checks-and-configuration)。

## 子網域檢查和設定 {#subdomain-checks-and-configuration}

1. 提交子網域後，「控制面板」會確認它是否正確指向 Adobe NS 記錄，以及此子網域不存在開始授權 (SOA) 記錄。

   >[!NOTE]
   >
   >請注意，子網域設定執行時，「控制面板」中的其他請求將會進入佇列，並只會在子網域設定完成後才執行，以免出現任何效能問題。

1. 如果確認成功，「控制面板」將會開始設定包含 DNS 記錄、其他 URL、收件匣等等的子網域。

   ![](assets/subdomain7.png)

   您可以按一下子網域設定的&#x200B;**[!UICONTROL 詳細資料]**&#x200B;按鈕，以取得有關設定進度的詳細資訊。

   ![](assets/subdomain_audit.png)

1. 最後，**傳遞團隊**&#x200B;將會收到關於新子網域的通知，以便稽核該子網域。設定子網域後，稽核流程最多需要 10 個工作天的時間。

   >[!IMPORTANT]
   >
   >執行的檢查包括回饋迴圈和垃圾郵件投訴迴圈測試。因此，我們不建議在稽核完成之前使用子網域，因為這可能導致子網域信譽不佳。
   >
   >不過，請注意，即使傳遞能力稽核仍在處理中，您也可以在子網域上執行與 SSL 憑證相關的作業。

1. 程序結束時，子網域將設定為與您的 Adobe Campaign 執行個體搭配使用，並會建立下列元素：

   * 具有下列 DNS 記錄&#x200B;**的**&#x200B;子網域：SOA、MX、CNAME、DKIM、SPF、TXT，
   * 託管鏡射、資源、追蹤頁面和網域金鑰的&#x200B;**其他子網域**，
   * **收件匣**：寄件人、錯誤、回覆。

   依預設，「控制面板」的「回覆」收件匣會設為清除電子郵件，且無法重新檢視。如果您想要監視行銷活動的「回覆」收件匣，請勿使用此位址。

您可以按一下&#x200B;**[!UICONTROL 子網域詳細資訊]**&#x200B;和&#x200B;**[!UICONTROL 寄件者資訊]**&#x200B;按鈕，以取得子網域的詳細資訊。

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## 疑難排解 {#troubleshooting}

* 在某些情況下，子網域會完成設定，但可能無法成功驗證子網域。子網域會持續列在&#x200B;**[!UICONTROL 已設定]**&#x200B;清單中，而且會包含作業記錄，其中會提供關於錯誤的資訊。如果您無法解決問題，請聯絡客戶服務。
* 如果在設定後，子網域顯示為「未驗證」，請啟動新的子網域驗證 (**...** / **[!UICONTROL 驗證子網域]**)。如果它仍顯示相同的狀態，原因可能是對收件者結構描述進行某些自訂，而無法使用標準流程進行驗證。請嘗試使用該子網域傳送行銷活動。
* 如果子網域設定在進行傳遞稽核步驟時花費太長時間（超過 10 個工作日），請聯繫客戶服務。
