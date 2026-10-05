---
product: campaign
solution: Campaign
title: 管理 TXT 記錄
description: 瞭解如何管理 TXT 記錄以進行網域擁有權驗證。
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 013d6674-0988-4553-a23e-b3ec23da5323
TQID: 'https://experienceleague.adobe.com/G8eirPm9hY0XRZTtMOBpmdwxuo3-Uvdo9LQjiSiElPU'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: a7760dfc-5c44-4d77-bb68-c50b1e265c93
    internal-label: Security and privacy
subfeature_v2:
  - id: f807e46f-d823-43a9-98be-82e0b2f3a05c
    internal-label: Subdomains and certificates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 100%
---
# 開始使用 TXT 記錄 {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="管理 TXT 記錄"
>abstract="TXT 記錄是一種 DNS 記錄，用於提供關於網域的文字資訊，可由外部來源讀取。 控制面板可讓您為子網域新增三種類型的記錄：Google 網站驗證、DMARC 和 BIMI 記錄。"

## 關於 TXT 記錄 {#about}

TXT 記錄是一種 DNS 記錄，用於提供關於網域的文字資訊，可由外部來源讀取。 「控制面板」可讓您將三種記錄類型新增至子網域：

* **Google TXT 記錄**&#x200B;可讓您驗證您是否擁有網域，確保高收件率和低垃圾郵件率。 [瞭解如何新增 Google TXT 記錄](managing-txt-records.md)
* **DMARC 記錄**&#x200B;提供了一種驗證寄件者網域的方式，並防止未經授權而惡意使用網域。 [瞭解如何新增 DMARC 記錄](dmarc.md)
* **BIMI 記錄**&#x200B;可讓您在郵箱提供者的收件匣中，於您的電子郵件旁邊顯示核准的標誌，以提升品牌認知度和信任度。 [瞭解如何新增 BIMI 記錄](bimi.md)

## 監視子網域的記錄 {#monitor}

您可以存取子網域的詳細資訊，以監視已為每個子網域新增的所有 TXT 記錄。

在此畫面中，所選子網域的所有 TXT 類型記錄都會顯示，並在其設定的「值」欄中顯示資訊。 若要刪除 Google TXT、DMARC 或 BIMI 記錄，請按一下省略符號按鈕，然後選取「刪除」。 如有必要，您也可以編輯 DMARC 和 BIMI 記錄。

![](assets/txt-records.png)
