---
product: campaign
solution: Campaign
title: 關於 SFTP 管理
description: 進一步瞭解「控制面板」中的 SFTP 管理
testing: SSECD-836 2
feature: Control Panel, SFTP Management
role: Admin
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
TQID: 'https://experienceleague.adobe.com/UZHhTNCld6p1RFGh3DY-2r3VRiLNxCtP0anuPxPnWVE'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e8445399-14db-4931-a0bb-477780230387
    internal-label: SFTP Management
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 100%
---
# 關於 SFTP 管理 {#about-sftp-management}

在「控制面板」中，您可以與所有連線至您可存取之 Campaign 執行個體的 SFTP 伺服器互動。 大部分執行個體都已連線 SFTP 伺服器 (在某些情況下，開發和預備執行個體可能未連線至任何 SFTP 伺服器)。

使用 SFTP 用戶端軟體存取 SFTP 伺服器，您可線上尋找和下載該軟體。 若要透過用戶端應用程式或 API 連線至伺服器，您必須設定公開 SSH 金鑰，並將連線至 SFTP 伺服器的 IP 位址新增至允許清單。

「控制面板」可以讓您執行下列動作，管理您的 SFTP 伺服器：

* 監視其&#x200B;**儲存容量**，
* 管理 **IP 位址允許清單**：新增或刪除一台或多台伺服器的 IP 位址範圍，
* 管理&#x200B;**公開 SSH 金鑰**&#x200B;以存取您的伺服器。

以下各節提供這些動作的詳細資訊。
