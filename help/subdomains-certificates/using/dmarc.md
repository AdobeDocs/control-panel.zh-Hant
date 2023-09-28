---
product: campaign
solution: Campaign
title: 新增DMARC記錄
description: 瞭解如何為子網域新增DMARC記錄。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: fc026f157346253fc79bde4ce624e7efa3373af2
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 0%

---


# 新增DMARC記錄 {#dmarc}

## 關於DMARC記錄 {#about}

網域型訊息驗證、報告及一致性(DMARC)是一種電子郵件驗證通訊協定標準，可協助組織保護其電子郵件網域免受網路釣魚和詐騙攻擊。 它可讓您決定信箱提供者應如何處理未通過SPF和DKIM檢查的電子郵件，提供驗證傳送者網域的方式，並防止未經授權而惡意使用網域。

## 限制和必要條件 {#limitations}

* SPF和DKIM記錄是建立DMARC記錄的先決條件。
* 只能使用完整子網域委派的子網域新增DMARC記錄。 [進一步瞭解子網域設定方法](subdomains-branding.md#subdomain-delegation-methods)

## 為子網域新增DMARC記錄 {#add}

若要為子網域新增DMARC記錄，請遵循下列步驟：

1. 從子網域清單中，按一下所需子網域旁的省略符號按鈕，然後選取 **[!UICONTROL Subdomain details]**.

1. 按一下 **[!UICONTROL Add TXT record]** 按鈕，然後選擇 **[!UICONTROL DMARC]** 從 **[!UICONTROL Record Type]** 下拉式清單。

   ![](assets/dmarc-add.png)

1. 選擇 **[!UICONTROL Policy Type]** 當您的其中一封電子郵件失敗時，收件者伺服器應該遵循的規則。 可用的原則型別為：

   * 無,
   * 隔離（垃圾郵件資料夾位置），
   * 拒絕（封鎖電子郵件）。

   如果您的子網域剛剛設定，建議您將此值設為「無」，直到子網域完全設定且電子郵件正確傳送為止。 一切設定正確後，您就可以將原則型別變更為「隔離」或「拒絕」。

   >[!NOTE]
   >
   > DMARC記錄原則型別設為「無」時，無法建立BIMI記錄。

1. 填寫應接收DMARC報表的電子郵件地址。 當您的其中一封電子郵件失敗時，DMARC報告會自動傳送至您選擇的電子郵件地址：

   * 彙總DMARC報表可提供高階資訊，例如在指定期間內失敗的電子郵件數量。
   * 取證DMARC失敗報告會提供詳細資訊，例如失敗的電子郵件來自哪個IP位址。

1. 依預設，選取的DMARC原則會套用至所有電子郵件。 您可以變更此引數，以僅套用至特定百分比的電子郵件。

   逐步部署DMARC時，您一開始可能會收到一小部分的訊息。 當來自您網域的更多訊息通過接收伺服器的驗證時，請使用更高的百分比更新您的記錄，直到您達到100%。

   >[!NOTE]
   >
   >如果您的網域使用BIMI，您的DMARC原則必須具有百分比值100%。 BIMI不支援這個值設定為小於100%的DMARC原則。

   ![](assets/dmarc-add2.png)

1. DMARC報告每24小時傳送一次。 您可以在以下位置變更報表傳送頻率： **[!UICONTROL Reporting Interval]** 欄位。 最小授權間隔為1小時，而最大授權值為2190小時（即3個月）。

1. 在 **SPF** 和 **[!UICONTROL DKIM Identifier Alignment]** 欄位，指定在檢查電子郵件的SPF和DKIM驗證時，收件者伺服器的嚴格程度。

   * **[!UICONTROL Relaxed]** 模式：即使電子郵件是從子網域傳送，伺服器仍接受驗證，
   * **[!UICONTROL Strict]** 只有當傳送者網域與SPF和DKIM網域完全相符時，模式才會接受驗證。

   假設我們正在使用 `http://www.luma.com` 網域。 在「寬鬆」模式中，來自 `marketing.luma.com` 子網域將由伺服器授權，但在「嚴格」模式下將會遭到拒絕。

1. 按一下 **[!UICONTROL Add]** 以確認建立DMARC記錄。

處理DMARC記錄建立作業之後（大約5分鐘），就會顯示在子網域的詳細資訊畫面中。 [瞭解如何監視子網域的TXT記錄](gs-txt-records.md#monitor)