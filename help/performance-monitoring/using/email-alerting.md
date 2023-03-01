---
product: campaign
solution: Campaign
title: 電子郵件警示
description: 了解如何在Campaign執行個體發生問題時接收電子郵件通知
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 3%

---

# 電子郵件警示 {#email-alerting}

為了為您的工作提供更大的彈性，「控制面板」已配備即時電子郵件警報功能。

## 警報清單 {#list}

警報清單如下：

* **SFTP儲存空間使用情況**:您的其中一部SFTP伺服器已達其容量的80%或以上。 請參閱 [SFTP 儲存空間管理](../../sftp/using/sftp-storage-management.md)。

* **資料庫使用**:您的實例的資料庫已達到其容量的80%或更多。 請參閱 [資料庫監視](../../performance-monitoring/using/database-monitoring.md).

* **SFTP IP允許清單過期**:您定義的其中一個IP範圍已過期，或將在10天或更短時間內過期。 請參閱 [IP範圍允許清單](../../sftp/using/ip-range-allow-listing.md).

* **SFTP公開金鑰過期**:您定義的其中一個公開金鑰已過期，或將在10天或更短時間內過期。 請參閱 [金鑰管理](../../sftp/using/key-management.md).

* **SSL憑證過期**:您的子網域其中一個SSL憑證已過期，或將在30天或更短時間內過期。 請參閱 [監控子網域的SSL憑證](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>此外，「控制面板」可讓您 **設定提醒** 以便在執行個體上發生事件之前（發行和服務審核），透過電子郵件收到通知。
>
>若要這麼做，您必須已訂閱電子郵件警報，並設定所需近期事件的提醒。 [了解如何為即將發生的事件設定提醒](../../service-events/service-events.md#reminders)

## 訂閱警示 {#subscribe}

若要訂閱這些警報，請執行下列步驟：

1. 按一下 **[!UICONTROL Alerting notifications]** 按鈕（可從「控制面板」中的任何位置取得），然後按一下 **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. 系統會傳送電子郵件以確認您的訂閱。

   ![](assets/email_subscription.png)

1. 訂閱後，「控制面板」會通知系統問題，並建議要採取的動作。 電子郵件警報會傳送給已註冊的每個人 **所有例項** 是的管理員。

   ![](assets/alert_sample.png)
