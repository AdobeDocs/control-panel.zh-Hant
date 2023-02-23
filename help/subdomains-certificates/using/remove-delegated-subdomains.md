---
product: campaign
solution: Campaign
title: 移除子網域的委派
description: 了解如何移除子網域的委派以Adobe。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 5a8c4c4d1c5c527135901cd41f2b0936af8737b4
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 2%

---

# 移除子網域的委派以Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="移除子網域委派"
>abstract="此畫面可讓您移除要Adobe的子網域委派。 請記住，提交後，此程式無法還原或停止。<br><br>如果您嘗試移除所選執行個體之主要網域的委派，系統會要求您選擇要取代它的網域。"

「控制面板」可讓您移除已委派給Adobe的子網域委派，包括CNAME設定。

## 重要備註 {#important}

在繼續操作之前，請仔細考慮刪除過程觸發後發生的影響：

* 子網域委派移除無法還原，且在進程執行進行之前，一旦啟動即將無法復原。
* 當另一個子網域上的類似程式正在進行中時，無法移除其他子網域委派。
* 在子網域上移除的委派，必須等到移除後3天才能重新委派。

## 移除子網域委派 {#steps}

若要移除要Adobe的子網域委派，請執行下列步驟：

1. 按一下要刪除的域委派旁的刪節號按鈕，然後選擇 **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. 檢閱免責聲明並確認移除要Adobe的網域委派。

1. 檢閱與子網域相關聯之例項的相關資訊，包括相關IP相關性和品牌設定。

   如果您正在移除所選執行個體之主要網域的委派，則需要選取要使用 **[!UICONTROL Replacement Domain]** 清單。

   按一下 **[!UICONTROL Next]** 繼續移除。

   ![](assets/undelegate-subdomain-details.png)

1. 檢閱顯示的摘要。 若要確認移除，請輸入您要移除委派之網域的URL，然後按一下 **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

委派移除開始後，待處理作業會顯示在作業記錄中，直到完成為止。

![](assets/undelegate-job.png)

## 錯誤代碼 {#FAQ}

本節列出嘗試移除子網域委派時可能遇到的錯誤訊息：

| 錯誤碼 | 訊息 | 說明 |
|  ---  |  ---  |  ---  |
| 8002 | 請求的委派域刪除無法處理，因為正在進行類似的重疊請求，請在3天後嘗試 | 所選實例的子域委派刪除作業已在進行中。 等待3天，開始新的刪除作業。 |
| 8003 | 此實例不支援請求的委派域刪除。 | 由於技術問題，所選子網域不支援移除委派，請聯絡客戶服務。 |
| 8004 | 不允許刪除請求的委派域，因為此實例中只有一個域。 | 只為所選實例委派了一個子域。 不允許刪除委派。 |
| 8005 | 此配置不支援刪除請求的委派域。 | 由於技術問題，所選子網域不支援移除委派，請聯絡客戶服務。 |
| 8006 | 由於未知原因，不允許刪除請求的委派域。 請聯絡客戶服務。 | 由於未知問題，所選執行個體不支援移除委派，請聯絡客戶服務。 |
