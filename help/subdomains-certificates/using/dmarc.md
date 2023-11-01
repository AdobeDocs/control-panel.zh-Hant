---
product: campaign
solution: Campaign
title: 新增 DMARC 記錄
description: 瞭解如何為子網域新增 DMARC 記錄。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 2ca66983-5beb-495a-9639-a31905500cff
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 83%

---

# 新增 DMARC 記錄 {#dmarc}

## 關於 DMARC 記錄 {#about}

網域型郵件驗證、報告及一致性 (DMARC) 是一種電子郵件驗證通訊協定標準，可協助組織保護其電子郵件網域免受網路釣魚和詐騙攻擊。 它可讓您決定郵箱提供者應如何處理未通過 SPF 和 DKIM 檢查的電子郵件，提供了一種驗證傳送者網域的方式，並防止未經授權而惡意使用網域。

有關 DMARC 實作的詳細資訊，請參閱 [Adobe 傳遞能力最佳實務指南](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html?lang=zh-Hant)

## 限制和先決條件 {#limitations}

* SPF 和 DKIM 記錄是建立 DMARC 記錄的先決條件。
* 只能使用完整子網域委派為子網域新增 DMARC 記錄。 [進一步瞭解子網域設定方法](subdomains-branding.md#subdomain-delegation-methods)
* 如果子網域同時存在 DMARC 和 BIMI 記錄：
   * 無法刪除 DMARC 記錄。 如果要刪除 DMARC 記錄，請先刪除 BIMI 記錄。
   * DMARC 記錄可加以編輯，但不允許將 DMARC 原則降級至「無」且其百分比值必須為 100。

## 為子網域新增 DMARC 記錄 {#add}

若要為子網域新增 DMARC 記錄，請遵循下列步驟：

1. 從子網域清單中，按一下所需子網域旁的省略符號按鈕，然後選取 **[!UICONTROL 子網域詳細資料]**.

1. 按一下 **[!UICONTROL 新增TXT記錄]** 按鈕，然後選擇 **[!UICONTROL DMARC]** 從 **[!UICONTROL 記錄型別]** 下拉式清單。

   ![](assets/dmarc-add.png)

1. 選擇 **[!UICONTROL 原則型別]** 當您的其中一封電子郵件失敗時，收件者伺服器應該遵循的規則。 可用的原則型別為：

   * **[!UICONTROL 無]**,
   * **[!UICONTROL 隔離]** （垃圾郵件資料夾位置），
   * **[!UICONTROL 拒絕]** （封鎖電子郵件）。

   依據最佳實務的要求，建議您逐步推出 DMARC 實作，方法是將 DMARC 原則從 p=none 提升至 p=quarantine，再提升至 p=reject，讓您瞭解 DMARC 的潛在影響。

   * **步驟 1：**&#x200B;分析您收到的意見回饋並使用 (p=none)，這會告知接收者，對於驗證失敗的郵件不執行任何動作，但仍會傳送電子郵件報告給寄件者。 此外，如果合法郵件驗證失敗，請檢閱並修正 SPF/DKIM 的問題。

   * **步驟 2：** 判斷 SPF 和 DKIM 是否一致，並通過所有合法電子郵件的驗證，然後將原則移至 (p=quarantine)，這會通知接收電子郵件伺服器隔離驗證失敗的電子郵件 (這通常意味著將這些郵件放在垃圾郵件資料夾中)。 如果原則設定為隔離，建議您從一小部分電子郵件開始。

   * **步驟 3：**&#x200B;將原則調整為 (p=reject)。 注意：請謹慎使用此原則，並判斷其是否適合您的組織。 p=reject 原則會告訴接收者，完全拒絕 (退回) 驗證失敗的網域的所有電子郵件。 啟用此原則後，只有經過網域驗證為 100% 驗證的電子郵件才有機會進入收件匣。

   >[!NOTE]
   >
   > DMARC 記錄原則型別設為「無」時，無法建立 BIMI 記錄。

1. 填寫應接收 DMARC 報告的電子郵件地址。 您可以新增多個電子郵件地址 (以逗號分隔)。 當您的其中一封電子郵件失敗時，DMARC 報告會自動傳送至您選擇的電子郵件地址：

   * 彙總 DMARC 報告可提供高階資訊，例如在指定期間內失敗的電子郵件數量。
   * 取證 DMARC 失敗報告會提供詳細資訊，例如失敗的電子郵件來自哪個 IP 位址。

1. 如果 DMARC 原則設為「無」，請輸入套用至 100% 電子郵件的百分比。

   如果原則設定為「拒絕」或「隔離」，建議您從一小部分電子郵件開始。 隨著越來越多的來自您網域的電子郵件通過接收伺服器的驗證，請使用較高的百分比緩慢更新您的記錄。

   >[!NOTE]
   >
   >如果您的網域使用 BIMI，您的 DMARC 原則必須具有百分比值 100%。 BIMI 不支援這個值設定為小於 100% 的 DMARC 原則。

   ![](assets/dmarc-add2.png)

1. DMARC 報告每 24 小時傳送一次。 您可以在以下位置變更報表傳送頻率： **[!UICONTROL 報告間隔]** 欄位。 最小授權間隔為 1 小時，而最大授權值為 2190 小時 (即 3 個月)。

1. 在 **SPF** 和 **[!UICONTROL DKIM識別碼對齊]** 欄位，指定在檢查電子郵件的SPF和DKIM驗證時，收件者伺服器的嚴格程度。

   * **[!UICONTROL 寬鬆]** 模式：即使電子郵件是從子網域傳送，伺服器仍接受驗證，
   * **[!UICONTROL 嚴格]** 只有當傳送者網域與SPF和DKIM網域完全相符時，模式才會接受驗證。

   假設我們正在使用`http://www.luma.com`網域。在「寬鬆」模式中，來自`marketing.luma.com`子網域的電子郵件將由伺服器授權，但在「嚴格」模式下將會遭到拒絕。

1. 按一下 **[!UICONTROL 新增]** 以確認建立DMARC記錄。

建立 DMARC 記錄之後 (大約 5 分鐘)，它就會顯示在子網域的詳細資訊畫面中。 [瞭解如何監視子網域的 TXT 記錄](gs-txt-records.md#monitor)
