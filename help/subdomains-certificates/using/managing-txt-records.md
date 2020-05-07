---
title: 管理TXT記錄
description: 瞭解如何管理TXT記錄以進行網域擁有權驗證。
translation-type: tm+mt
source-git-commit: 7c2dd60c70b5f9c0b2567df289582b972a7f76b8
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---


# 管理TXT記錄 {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="管理TXT記錄"
>abstract="有些服務（例如Google）會要求您在網域設定中新增TXT記錄，以確認您擁有網域。"

## 關於TXT記錄 {#about-txt-records}

TXT記錄是一種DNS記錄，用於提供域的文本資訊，可由外部源讀取。

為了確保高收件匣率和低垃圾郵件率，Google等服務要求您在網域設定中新增TXT記錄，以確認您擁有網域。

目前，Gmail是最受歡迎的電子郵件地址提供商之一。 為了確保電子郵件的傳送能力良好，並能成功傳送至Gmail位址，Adobe Campaign可讓您在您的子網域中新增特殊的Google網站驗證TXT記錄，以確保其經過驗證。

其他資源：

* [Campaign Standard教學課程影片](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/google-txt-record-management.html)
* [Campaign Classic教學課程影片](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/google-txt-record-management.html)

## 新增子網域的Google TXT記錄 {#adding-a-google-txt-record}

若要將Google TXT記錄新增至您用來以電子郵件傳送Gmail位址的子網域，請依照下列步驟進行：

1. 導覽至資 **[!UICONTROL Subdomain and Certificates]** 訊卡。

1. 選擇實例，然後開啟要向其添加DNS記錄的子域的詳細資訊。

   ![](assets/txt_subdomaindetails.png)

1. 按一下 **[!UICONTROL Add TXT record]** 按鈕，然後輸入G套裝管理工具中產生的值。 如需詳細資訊，請參閱 [G套裝管理說明](https://support.google.com/a/answer/183895)。

   ![](assets/txt_addtxt.png)

1. 按一下按 **[!UICONTROL Add]** 鈕以確認。

   ![](assets/txt_txtadded.png)

新增TXT記錄後，您必須由Google驗證。 若要這麼做，請導覽至G套裝管理工具，然後啟動驗證步驟(請參閱 [G套裝管理說明](https://support.google.com/a/answer/183895))。

要刪除記錄，請從記錄清單中選擇該記錄，然後按一下刪除按鈕。

>[!NOTE]
>
>從DNS記錄清單中刪除的唯一記錄是您先前新增的記錄（在我們的例子中是Google TXT記錄）。
