---
product: campaign
solution: Campaign
title: 新增子網域的Google網站驗證記錄
description: 瞭解如何為子網域新增Google網站驗證記錄，以進行網域所有權驗證。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 70%

---

# 新增 Google 網站驗證記錄 {#adding-a-google-txt-record}

為了確保達到高郵件到達率和低垃圾郵件率，Google 這類服務會要求您在網域設定中新增 TXT 記錄，以驗證您擁有該網域。

Gmail 是目前最受歡迎的電子郵件地址供應商之一。為了確保良好的傳遞率，並且成功傳送至 Gmail 地址，Adobe Campaign 可讓您在子網域中新增特殊的 Google 網站驗證 TXT 記錄，以確保其經過驗證。

若要將 Google TXT 記錄新增至您用來傳送電子郵件至 Gmail 地址的子網域，請執行下列步驟：

1. 從子網域清單中，按一下所需子網域旁的省略符號按鈕，然後選取 **[!UICONTROL 子網域詳細資料]**.

1. 按一下 **[!UICONTROL 新增TXT記錄]** 按鈕，然後選擇 **[!UICONTROL Google網站驗證]** 從 **[!UICONTROL 記錄型別]** 下拉式清單。

1. 輸入G Suite管理工具中產生的值。 如需詳細資訊，請參閱 [G Suite 管理員說明](https://support.google.com/a/answer/183895)。

   ![](assets/txt_addtxt.png)

1. 按一下 **[!UICONTROL 新增]** 按鈕確認。

   ![](assets/txt_txtadded.png)

新增 TXT 記錄後，該記錄必須獲得 Google 驗證。若要這麼做，請導覽至 G Suite 管理工具，然後啟動驗證步驟 (請參閱 [G Suite 管理員說明](https://support.google.com/a/answer/183895))。

若要刪除記錄，請從記錄清單中選取該記錄，然後按一下移除按鈕。

>[!NOTE]
>
>您只能從 DNS 記錄中刪除您先前新增的記錄 (在此情況中，即為 TXT 記錄)。

![](assets/do-not-localize/how-to-video.png)利用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates) 在影片中瞭解此功能
