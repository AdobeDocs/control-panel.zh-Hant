---
product: campaign
solution: Campaign
title: 電子郵件警示
description: 瞭解如何在市場活動實例出現問題時接收電子郵件通知
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: a2c007fbf5446c92a6366882eb873deeadd5edf5
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# 電子郵件警示 {#email-alerting}

為了給您的工作提供更大的靈活性，控制面板配備了即時電子郵件警報功能。

要訂閱這些警報，請執行以下步驟：

1. 按一下 **[!UICONTROL Alerting notifications]** 按鈕，然後按一下 **[!UICONTROL Subscribe]**。

   ![](assets/subscribing.png)

1. 系統會發送一封電子郵件以確認您的訂閱。

   ![](assets/email_subscription.png)

1. 訂閱後，控制面板將通知系統問題並建議採取相應操作。 電子郵件警報將發送給已註冊的所有人 **所有實例** 他們是管理員。

   ![](assets/alert_sample.png)

警報清單如下：

* **SFTP儲存使用**:您的SFTP伺服器中的一台已達80%或更多的容量。 請參閱 [SFTP儲存管理](../../sftp/using/sftp-storage-management.md)。

* **資料庫使用**:您的實例的一個資料庫已達到其容量的80%或更高。 請參閱 [資料庫監視](../../performance-monitoring/using/database-monitoring.md)。

* **SSL證書過期**:您的子域之一的SSL證書已過期或將在60天或更短時間內過期。 請參閱 [監視子域的SSL證書](../../subdomains-certificates/using/monitoring-ssl-certificates.md)。

* **SFTP IP允許列出過期**:您定義的IP範圍之一已過期或將在10天或更短時間內過期。 請參閱 [IP範圍允許清單](../../sftp/using/ip-range-allow-listing.md)。

* **SFTP公鑰過期**:您定義的其中一個公鑰已過期或將在10天或之內過期。 請參閱 [密鑰管理](../../sftp/using/key-management.md)。

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->