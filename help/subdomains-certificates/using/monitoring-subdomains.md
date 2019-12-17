---
title: 監視子域的SSL證書
description: 瞭解如何監控子網域的SSL憑證
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# 監控子網域 {#monitoring-subdomains}

您必須監控子網域，以確保所有子網域皆已正確設定，以搭配Adobe Campaign運作。

選取卡片時，可直接存取每個生產例項的子網域清 **[!UICONTROL Subdomains & Certificates]**單。

![](assets/subdomains_list.png)

若要取得子網域的詳細資訊，請按一下 **[!UICONTROL Subdomain Details]**按鈕。
會顯示所有相關子網域的清單。 它通常包含著陸頁面、資源頁面等的子網域。

該選 **[!UICONTROL Sender info]**項卡提供有關已配置收件箱的資訊（發件人、回覆、錯誤電子郵件）。

![](assets/subdomain_details.png)


在子網域清單中， **[!UICONTROL Last verification]**欄會指出上次驗證子網域的時間。** 您隨時都可以按一下…… **./按**[!UICONTROL Verify subdomain]** 鈕。

>[!CAUTION]
>
>Adobe不建議使用沒有驗證日期的子網域，因為這可能表示這些子網域可能有某些可傳遞性問題。

![](assets/subdomain_verification.png)

啟動驗證時，會執行數個操作以檢查子域是否正確配置：

1. 「控制面板」會檢查子網域是否屬於例項租用戶。
1. 使用該子網域的例項會傳送電子郵件給一組「250ok」（協力廠商電子郵件分析和傳遞能力平台）的測試收件者。
1. 收到電子郵件後，250ok會讀取電子郵件標題並檢查SPF和DKIM是否已設定且有效。
1. 控制面板會持續輪詢250ok的傳送狀態約20分鐘。 如果SPF和DKIM通過，表示已驗證請求的子域，且已完全配置並準備用於發送電子郵件。
