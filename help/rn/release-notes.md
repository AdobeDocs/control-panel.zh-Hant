---
title: 最新版本
description: 本頁面列出了「控制面板」的所有新功能和改善項目。
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 26%

---

# 最新版本 {#control-panel-releases}

本頁面列出了「控制面板」的所有新功能和改善項目。

## 2023 年 10 月 {#october-2023}

**使用者介面**

* 控制面板現在提供其他語言版本。 [了解更多](../discover/using/discovering-the-interface.md#supported-languages-languages)

**作用中設定檔監控**

* 如果您使用多個執行個體，您現在可以監視組織有權使用的作用中設定檔數量，以及組織內所有執行個體中使用的設定檔總數。 [了解更多](../performance-monitoring/using/active-profiles-monitoring.md)

**DMARC記錄**

* 多個電子郵件地址現在可以接收彙總報告和失敗報告電子郵件。 [了解更多](../subdomains-certificates/using/dmarc.md)
* 如果子網域同時存在DMARC和BIMI記錄，則已進行變更：

   * 無法刪除DMARC記錄。 如果您想要刪除其中一個，您必須先刪除BIMI記錄。
   * DMARC記錄可以編輯，但原則降級為「無」是不允許的，其百分比值必須為100。

