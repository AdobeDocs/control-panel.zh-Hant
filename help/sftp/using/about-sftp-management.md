---
product: campaign
solution: Campaign
title: 關於 SFTP 管理
description: 在「控制面板」中瞭解有關SFTP管理的詳細資訊
testing: SSECD-836 2
feature: Control Panel
role: Architect
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 16%

---

# 關於 SFTP 管理 {#about-sftp-management}

在「控制面板」中，您可以與所有連線至您可存取之 Campaign 執行個體的 SFTP 伺服器互動。 大多數實例已連接SFTP伺服器（在某些情況下，開發和階段實例可能未連接到任何SFTP伺服器）。

訪問SFTP伺服器時使用SFTP客戶端軟體，您可以線上查找和下載該軟體。 要連接到伺服器，必須通過此類客戶端應用程式或API設定公共SSH密鑰，並將連接到SFTP伺服器的IP地址添加到允許清單。

通過「控制」面板，您可以執行以下操作來管理SFTP伺服器：

* 監視 **儲存容量**。
* 管理 **允許列出IP地址**:添加或刪除一個或多個伺服器的IP地址範圍，
* 管理 **公共SSH密鑰** 來接近你的服務員。

以下各節提供了有關這些操作的詳細資訊。
