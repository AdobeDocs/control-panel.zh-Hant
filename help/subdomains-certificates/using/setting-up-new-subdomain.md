---
title: 設定新子網域
description: 瞭解如何為您的促銷活動例項設定新的子網域
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# 設定新子網域 {#setting-up-subdomain}

## 完全子域委派 {#full-subdomain-delegation}

「控制面板」可讓您將子網域完全委派給Adobe Campaign。 若要這麼做，請依照下列步驟進行：

1. 在卡片 **[!UICONTROL Subdomains & Certificates]**中，選取所要的生產例項，然後按一下**[!UICONTROL Setup new subdomain]**。

   >[!NOTE]
   >
   >子域委派僅適用於 **生產** 例項。

   ![](assets/subdomain1.png)

1. 按一下 **[!UICONTROL Next]**以確認完全委託方法。

   >[!NOTE]
   >
   >[CNAME](#use-cnames) 和自訂方法目前不受控制面板支援。

   ![](assets/subdomain3.png)

1. 在您組織使用的代管解決方案中建立所需的子網域和名稱伺服器。 若要這麼做，請複製並貼上精靈中顯示的Adobe Nameserver資訊。

   如需如何在代管解決方案中建立子網域的詳細資訊，請參閱本教學課程影片。

   ![](assets/subdomain4.png)

   使用對應的Adobe名稱伺服器資訊建立子網域後，按一下 **[!UICONTROL Next]**。

1. 選擇子網域的所需使用案例：

   * **行銷通訊**:用於商業目的的通訊。 範例：銷售電子郵件宣傳。
   * **交易與營運通訊**:交易通訊包含的資訊旨在完成收件者與您一起開始的程式。 範例：購買確認、密碼重設電子郵件。 組織通訊與組織內外的資訊、想法和意見交換有關，無商業目的。
   >[!NOTE]
   >
   >根據使用案例劃分子網域是提供能力的最佳實務。 這樣，每個子域的信譽就會被隔離和保護。
   >
   >例如，如果行銷通訊的子網域最終被網際網路服務供應商列入黑名單，您的交易通訊子網域將不會受到影響，而且會持續傳送通訊。

   ![](assets/subdomain5.png)

1. 輸入您建立的子網域至您的代管解決方案，然後按一下 **[!UICONTROL Submit]**。

   >[!NOTE]
   >
   > 請務必填寫要委 **派的子網域** 的完整名稱。 例如，若要委派&quot;usoffers.email.weretail.com&quot;子網域，請輸入&quot;usoffers.email.weretail.com&quot;。

   ![](assets/subdomain6.png)

1. 提交子域後，控制面板將檢查它是否指向Adobe NS記錄，以及此子域不存在授權開始(SOA)記錄。

1. 如果檢查成功，「控制面板」將開始設定包含DNS記錄、其他URL、收件箱等的子域。 您可以按一下按鈕，以取得有關設定進度的詳細 **[!UICONTROL Process details]**資訊。

   ![](assets/subdomain7.png)

在程式結束時，子網域將設定為可搭配您的Adobe Campaign例項運作，並會建立下列元素：

* **具有** 下列 **DNS記錄的子網域**:SOA、MX、CNAME、DKIM、SPF、TXT、
* **托管鏡像** 、資源、跟蹤頁和域密鑰的附加子域、
* **Inbox**:發件人、錯誤、回覆。

## CNAME的使用 {#use-cnames}

Adobe不建議使用CNAME進行子網域委派，也不支援透過「控制面板」使用。

若要使用此方法，請連絡您的Adobe客戶服務。
