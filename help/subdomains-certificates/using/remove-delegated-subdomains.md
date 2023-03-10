---
product: campaign
solution: Campaign
title: 移除子網域委派
description: 了解如何移除給 Adobe 的子網域委派。
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 349eb8778a19263b83b70b8c920c401aff7fa24a
workflow-type: ht
source-wordcount: '509'
ht-degree: 100%

---

# 移除給 Adobe 的子網域委派 {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="移除子網域委派"
>abstract="此畫面可讓您移除給 Adobe 的子網域委派。 請記住，此流程無法取消，且必須等到執行完成之後才能復原。<br><br>如果您嘗試移除選定執行個體的主要網域委派，系統會要求您選擇取代的網域。"

「控制面板」可讓您移除已委派給 Adobe 的子網域委派。

>[!NOTE]
>
>已使用 CNAME 設定的子網域目前無法使用委派移除功能。

## 重要備註 {#important}

在繼續操作之前，請仔細考慮一旦觸發移除流程會發生的影響：

* 一旦觸發流程，子網域委派移除作業將無法取消，且在流程執行完成之前無法復原。
* 當另一子網域正在進行類似流程時，無法移除其他子網域委派。
* 在移除子網域委派之後，必須等到移除 3 天之後，才能重新委派。

## 移除子網域委派 {#steps}

若要移除給 Adobe 的子網域委派，請執行下列步驟：

1. 按一下要移除的網域委派旁的刪節號按鈕，然後選取&#x200B;**[!UICONTROL Remove delegated subdomain]**。

   ![](assets/undelegate-subdomain.png)

1. 檢閱免責聲明並確認移除給 Adobe 的網域委派。

1. 檢閱與子網域相關聯執行個體的資訊，包括相關 IP 相關性與品牌設定。

   如果您正在移除選定執行個體的主要網域委派，則需利用&#x200B;**[!UICONTROL Replacement Domain]**&#x200B;清單選擇其取代網域。

   按一下&#x200B;**[!UICONTROL Next]**&#x200B;繼續移除。

   ![](assets/undelegate-subdomain-details.png)

1. 檢閱顯示的摘要。 若要確認移除，請輸入您要移除委派的網域 URL，然後按一下&#x200B;**[!UICONTROL Submit]**。

   ![](assets/undelegate-submit.png)

在委派移除開始之後，待處理作業會顯示在作業記錄，直到完成為止。

![](assets/undelegate-job.png)

## 錯誤代碼 {#FAQ}

本區段列出錯誤訊息，在嘗試移除子網域委派時，您可能會遇見該訊息：

| 錯誤代碼 | 訊息 | 說明 |
|  ---  |  ---  |  ---  |
| 8002 | 無法處理請求的委派網域移除，因為正在進行類似的重疊請求，請在 3 天後再試一次 | 已在進行選定執行個體的子網域委派移除作業。 請等待 3 天再開始新的移除作業。 |
| 8003 | 此執行個體不支援請求的委派網域移除。 | 由於技術問題，選定子網域不支援委派移除，請聯絡客戶服務部門。 |
| 8004 | 不允許請求的委派網域移除，因為此執行個體中只有一個網域。 | 選定執行個體僅委派單一子網域。 不允許移除委派。 |
| 8005 | 此設定不支援請求的委派網域移除。 | 由於技術問題，選定子網域不支援委派移除，請聯絡客戶服務部門。 |
| 8006 | 由於未知原因，不允許請求的委派網域移除。請聯絡客戶服務。 | 由於未知問題，選定執行個體不支援移除委派，請聯絡客戶服務部門。 |
