---
title: 設定新子網域
description: 瞭解如何為您的促銷活動例項設定新的子網域
translation-type: tm+mt
source-git-commit: 9bcf83c85628a59671cd5580144d86bee88e35de

---


# 設定新子網域 {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id=&quot;cp_subdomain_management&quot;
>title=&quot;設定新子網域並管理憑證&quot;
>abstract=&quot;您需要設定新的子網域並管理您子網域的SSL憑證，以開始使用Adobe Campaign傳送電子郵件或發佈登陸頁面。&quot;
>additional-url=&quot;https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html&quot; text=&quot;How to monitor your subdomains&#39; SSL certificates&quot;

>[!IMPORTANT]
>
>從「控制面板」進行子網域委派的測試版可供使用，但必須經常更新和修改，恕不另行通知。

## 完全子域委派 {#full-subdomain-delegation}

「控制面板」可讓您將子網域完全委派給Adobe Campaign。 若要這麼做，請依照下列步驟進行。

>[!NOTE]
>
>如果選取的例項沒有先前設定的子網域，則委派給Adobe的第一個子網域將成為該例項的 **主要子網域** ，您將來將無法變更它。
>
>使用主子域為其他子域建立反向DNS記錄。 其他子網域的回覆和反彈位址會從主要子網域產生。

1. 在卡片 **[!UICONTROL Subdomains & Certificates]** 中，選取所要的生產例項，然後按一下 **[!UICONTROL Setup new subdomain]**。

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >子網域委派僅適用於 **生產** 例項。

1. 按一下 **[!UICONTROL Next]** 以確認完全委託方法。

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[CNAME](#use-cnames) 和自訂方法目前不受控制面板支援。

1. 在您組織使用的代管解決方案中建立所需的子網域和名稱伺服器。 若要這麼做，請複製並貼上精靈中顯示的Adobe Nameserver資訊。 如需如何在代管解決方案中建立子網域的詳細資訊，請參閱教學 [課程影片](https://video.tv.adobe.com/v/30175?captions=chi_hant)。

   >[!IMPORTANT]
   >
   >設定命名空間時，請務必 **不要將根子網域委派給Adobe**。 否則，網域將只能與Adobe搭配使用。 任何其他用途都不可能，例如傳送內部電子郵件給您組織的員工。
   >
   >此外， **請勿為此新子網域建立個別的區域** 檔案。

   ![](assets/subdomain4.png)

   使用對應的Adobe名稱伺服器資訊建立子網域後，按一下 **[!UICONTROL Next]**。

1. 選擇子網域的所需使用案例：

   * **行銷通訊**:用於商業目的的通訊。 範例：銷售電子郵件宣傳。
   * **交易與營運通訊**:交易通訊包含的資訊旨在完成收件者與您一起開始的程式。 範例：購買確認、密碼重設電子郵件。 組織通訊與組織內外的資訊、想法和意見交換有關，無商業目的。
   ![](assets/subdomain5.png)

   **根據使用案例劃分子網域是提供能力的最佳實務**。 這樣，每個子域的信譽就會被隔離和保護。 例如，如果行銷通訊的子網域最終被網際網路服務供應商列入黑名單，您的交易通訊子網域將不會受到影響，而且會持續傳送通訊。

   **您可以針對行銷和交易使用案例委派子網域**:

   * 對於行銷使用案例，子網域將設定在 **MID** (Mid sourcing)例項上。
   * 對於事務性使用案例，子網域將配置在所有 **RT** （消息中心／即時消息）實例上，以確保連接性。 因此，子網域將會與您的所有RT例項一起運作。
   >[!NOTE]
   >
   >如果您使用Campaign Classic,「控制面板」可讓您查看哪些RT/MID例項已連接至您正在使用的Marketing例項。 如需詳細資訊，請參閱[本小節](../../instances-settings/using/instance-details.md)。

1. 輸入您建立的子網域至您的代管解決方案，然後按一下 **[!UICONTROL Submit]**。

   請務必填寫要委 **派的子網域** 的完整名稱。 例如，若要委派&quot;usoffers.email.weretail.com&quot;子網域，請輸入&quot;usoffers.email.weretail.com&quot;。

   ![](assets/subdomain6.png)

1. 提交子網域後，控制面板會檢查它是否正確指向Adobe NS記錄，以及此子網域不存在授權開始(SOA)記錄。

1. 如果檢查成功，「控制面板」將開始設定包含DNS記錄、其他URL、收件箱等的子域。 您可以按一下按鈕，以取得有關設定進度的詳細 **[!UICONTROL Process details]** 資訊。

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >在某些情況下，委派會完成，但子網域可能無法成功驗證。 子域將直接進入清單， **[!UICONTROL Verified subdomains]** 其狀態 **[!UICONTROL Unverified]** 和作業日誌將提供錯誤資訊。 如果您無法解決問題，請聯絡客戶服務。
   >
   >請注意，當子網域委派執行時，控制面板中的其他請求將會進入佇列，並僅在子網域委派完成後才執行，以避免任何效能問題。

在程式結束時，子網域將設定為可搭配您的Adobe Campaign例項運作，並建立下列元素：

* **具有** 下列 **DNS記錄的子網域**:SOA、MX、CNAME、DKIM、SPF、TXT、
* **托管鏡像** 、資源、跟蹤頁和域密鑰的附加子域、
* **Inbox**:發件人、錯誤、回覆。

>[!NOTE]
>
>根據預設，「控制面板」的「回覆」收件匣設定為清除電子郵件，且無法重新檢視。 如果您想要監控行銷活動的「回覆」收件匣，請勿使用此位址。


按一下按鈕，即可取得子網域的詳細 **[!UICONTROL Subdomain Details]** 資訊。

![](assets/subdomain_details_general.png)

![](assets/subdomains_details_senderinfo.png)

>[!IMPORTANT]
>
>在處理階段後，您應向Adobe客戶服務確認已提交審核請求，讓交付能力團隊審核已建立的新子網域。 子網域被委派後，稽核程式最多需要3 10個工作天。
>
>執行的檢查包括反饋迴路和垃圾郵件投訴迴路測試。 因此，我們建議在審計完成之前不要使用子域，因為這可能導致子網域信譽不佳。

## CNAME的使用 {#use-cnames}

「控制面板」不支援使用CNAME進行子網域委派。 若要使用此方法，請聯絡Adobe客戶服務。

**相關主題：**

* [委派子網域（教學課程影片）](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [子網域品牌](../../subdomains-certificates/using/subdomains-branding.md)
* [監控子網域](../../subdomains-certificates/using/monitoring-subdomains.md)