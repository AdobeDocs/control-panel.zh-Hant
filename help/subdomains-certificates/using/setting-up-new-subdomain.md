---
title: 設定新的子網域
description: 瞭解如何為您的 Campaign 執行個體設定新的子網域
translation-type: tm+mt
source-git-commit: 198c974d269289a6a9e5a87314662dba0bc85aff
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 96%

---


# 設定新的子網域{#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="設定新的子網域和管理憑證"
>abstract="您必須設定新的子網域和管理子網域的 SSL 憑證，才能開始使用 Adobe Campaign 傳送電子郵件或發佈登陸頁面。"
>additional-url="https://docs.adobe.com/content/help/zh-Hant/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="如何監視子網域的 SSL 憑證"

>[!IMPORTANT]
>
>從「控制面板」委派子網域的功能會在測試版提供，且可能會不時更新和修改，恕不另行通知。

## 完全子網域委派{#full-subdomain-delegation}

「控制面板」可讓您將子網域完全委派給 Adobe Campaign。請依照下列步驟以執行此操作。

>[!NOTE]
>
>如果選取的執行個體沒有先前設定好的子網域，則委派給 Adobe 的第一個子網域將成為該執行個體的&#x200B;**主要子網域**，而您將來並無法進行任何變更。
>
>使用主要子網域為其他子網域建立反向 DNS 記錄。其他子網域的回覆和退信地址會從主要子網域產生。

1. 在「**[!UICONTROL Subdomains & Certificates]**」卡片中，選取所需的生產執行個體，再按一下「**[!UICONTROL Setup new subdomain]**」。

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >子網域委派僅適用於&#x200B;**生產**&#x200B;執行個體。

1. 按一下「**[!UICONTROL Next]**」以確認完全委派方法。

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >「控制面板」目前不支援 [CNAME](#use-cnames) 和自訂方法。

1. 在您組織使用的託管解決方案中，建立所需的子網域和名稱伺服器。若要這麼做，請複製並貼上精靈中顯示的 Adobe Nameserver 資訊。如需進一步瞭解如何在託管解決方案中建立子網域，請參考[教學課程影片](https://video.tv.adobe.com/v/30175?captions=chi_hant)。

   >[!IMPORTANT]
   >
   >設定命名伺服器時，請務必&#x200B;**不要將根子網域委派給 Adobe**。否則，網域只能與 Adobe 搭配使用。您不能用於任何其他用途，例如傳送內部電子郵件給您組織的員工。
   >
   >此外，**請勿為此新子網域建立個別的區域檔案**。

   ![](assets/subdomain4.png)

   使用對應的 Adobe 名稱伺服器資訊建立子網域後，請按一下「**[!UICONTROL Next]**」。

1. 選取子網域所需的使用案例：

   * **行銷通訊**：用於商業目的的通訊。範例：銷售電子促銷活動。
   * **交易與營運通訊**：交易通訊包含的資訊旨在完成收件者與您開展的流程。範例：購買確認函、密碼重設電子郵件。組織通訊與組織內外的資訊、構思和意見交換有關，並無任何商業目的。
   ![](assets/subdomain5.png)

   **根據使用案例劃分子網域是傳遞能力的最佳實務**。如此一來，就能分隔和保護每個子網域的信譽。例如，如果行銷通訊的子網域最終被網際網路服務供應商新增至區塊清單，您的交易通訊子網域將不會受到影響，而且會持續傳送通訊。

   **您可以為行銷和交易使用案例委派子網域**：

   * 若是行銷使用案例，子網域將會設定在 **MID** (Mid sourcing) 執行個體上。
   * 若是交易使用案例，子網域將會設定在 ALL **RT** (Message Center/即時傳送訊息) 執行個體上，以確保連線能力。因此，子網域將會搭配您所有 RT 執行個體一起運作。
   >[!NOTE]
   >
   >如果您使用 Campaign Classic，「控制面板」可讓您查看哪些 RT/MID 執行個體已連線至您正在使用的行執行個體。如需詳細資訊，請參閱[本章節](../../instances-settings/using/instance-details.md)。

1. 輸入您建立到託管解決方案的子網域，再按一下「**[!UICONTROL Submit]**」。

   請務必填寫要委派之子網域的&#x200B;**完整名稱**。舉例來說，若要委派「usoffers.email.weretail.com」子網域，請輸入「usoffers.email.weretail.com」。

   ![](assets/subdomain6.png)

1. 提交子網域後，「控制面板」會檢查它是否正確指向 Adobe NS 記錄，以及此子網域不存在開始授權 (SOA) 記錄。

1. 如果檢查成功，「控制面板」將會開始設定包含 DNS 記錄、其他 URL、收件箱等等的子網域。您可以按一下 **[!UICONTROL Process details]**&#x200B;按鈕，以取得有關設定進度的詳細資訊。

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >在某些情況下會完成委派，但可能無法成功驗證子網域。子網域將直接進入 **[!UICONTROL Verified subdomains]**&#x200B;清單，並含有狀態&#x200B;**[!UICONTROL Unverified]** 以及提供錯誤相關資訊的工作記錄。如果您無法解決問題，請聯絡客戶服務。
   >
   >請注意，子網域委派執行時，透過「控制面板」中的其他請求將會進入佇列，並只會在子網域委派完成後才執行，以免出現任何效能問題。

程序結束時，子網域將設定為與您的 Adobe Campaign 執行個體搭配使用，並會建立下列元素：

* 具有下列 **DNS 記錄**&#x200B;的&#x200B;**子網域**：SOA、MX、CNAME、DKIM、SPF、TXT，
* 託管鏡射、資源、追蹤頁面和網域金鑰的&#x200B;**其他子網域**，
* **收件匣**：寄件人、錯誤、回覆。

>[!NOTE]
>
>依預設，「控制面板」的「回覆」收件匣會設為清除電子郵件，且無法重新檢視。如果您想要監視行銷活動的「回覆」收件匣，請勿使用此位址。

您可以按一下 **[!UICONTROL Subdomain details]**&#x200B;和 **[!UICONTROL Sender info]** 按鈕，以取得子網域的詳細資訊。

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

>[!IMPORTANT]
>
>在處理階段後，您應向 Adobe 客戶服務確認已提交稽核請求，讓傳遞團隊稽核已建立的新子網域。委派子網域後，稽核流程最多需要 3 至 10 個工作天的時間。
>
>執行的檢查包括意見反應機制和垃圾郵件投訴迴圈測試。因此，我們不建議在稽核完成之前使用子網域，因為這可能導致子網域信譽不佳。

## CNAME 的使用{#use-cnames}

「控制面板」不支援使用 CNAME 進行子網域委派。若要使用此方法，請聯絡 Adobe 客戶服務。

**相關主題：**

* [委派子網域 (教學課程影片)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [子網域名稱](../../subdomains-certificates/using/subdomains-branding.md)
* [監視子網域](../../subdomains-certificates/using/monitoring-subdomains.md)