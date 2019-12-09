---
title: 設定新子網域
description: 瞭解如何為您的促銷活動例項設定新的子網域
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# 設定子網域 {#setting-up-subdomain}

「控制面板」可讓您將子網域完全委派給Adobe Campaign。 若要這麼做，請依照下列詳細步驟進行。

>[!NOTE]
>
>「控制面板」不支援使用CNAME進行子網域委派。 有關此方法的詳細資訊，請參 [閱本頁](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。

1. 在資訊 **[!UICONTROL Subdomains & Certificates]**卡中，選取所要的例項，然後按一下**[!UICONTROL Setup new subdomain]** 按鈕。

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >此按 **[!UICONTROL Setup new subdomain]**鈕僅適用於「生產」例項。

1. 選取方 **[!UICONTROL Delegation to Adobe]**法，然後按一下**[!UICONTROL Next]**。

   ![](assets/subdomain3.png)

1. 在您組織使用的代管解決方案中建立所需的子網域。 若要這麼做，請複製精靈中顯示的Adobe Nameserver資訊，然後貼到您的代管解決方案中。

   如需如何在代管解決方案中建立子網域的詳細資訊，請參閱可從精靈存取的教學課程影片。

   ![](assets/subdomain4.png)

   使用對應的Adobe名稱伺服器資訊建立子網域後，按一下 **[!UICONTROL Next]**。

1. 選擇子網域的所需使用案例：

   * **行銷通訊**:用於商業目的的通訊。 範例：銷售電子郵件宣傳。
   * **交易與營運通訊**:交易通訊包含的資訊旨在完成收件者與您一起開始的程式。 範例：購買確認、密碼重設電子郵件。 組織通訊與組織內外的資訊、想法和意見交換有關，無商業目的。
   依此方式劃分子網域是提供能力的最佳實務。 這樣，每個子域的信譽就會被隔離和保護。 例如，如果行銷通訊的子網域最終被網際網路服務供應商列入黑名單，您的交易通訊子網域將不會受到影響，而且會持續傳送通訊。

   ![](assets/subdomain5.png)

   >[!NOTE]
   >
   >您只能選擇為實例配置的使用案例。 如果實例僅配置為「行銷通信」，則您將無法選擇「事務和運營通信」使用案例。

1. 輸入您使用Adobe Nameserver資訊建立在代管解決方案中的子網域，然後按一下「送 **[出]**」。

   >[!NOTE]
   >
   > 請確定您填入要委 **派的** 完整子網域。 例如，若要委派&quot;usoffers.email.weretail.com&quot;子網域，請輸入&quot;usoffers.email.weretail.com&quot;。

   ![](assets/subdomain6.png)

1. 提交子網域後，「控制面板」會執行各種作業來設定子網域，並檢查它是否正確指向「促銷活動」例項（命名空間記錄建立、促銷活動例項設定、「授權開始」記錄驗證等）。

   您可以隨時按一下按鈕，以取得有關設定進度的詳細 **[!UICONTROL Process details]**資訊。

   ![](assets/subdomain7.png)

在程式結束時，您會得到什麼？
* 具有以下DNS記錄的子域- SOA、MX、CNAME、DKIM、SPF、TXT。
* 托管鏡像、資源、跟蹤頁和域密鑰的其他子域
* Inbox —— 發送者、錯誤、回覆
* 最終，子網域將設定為可搭配您的Adobe Campaign例項運作
