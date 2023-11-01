---
title: 產品文件
description: 控制面板文件。
feature: Control Panel
role: Admin
level: Experienced
exl-id: 2b2cfaed-e42e-4c3a-a8d8-224b936890ab
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 100%

---

# 說明中心 {#control-panel-documentation}

>[!CONTEXTUALHELP]
>id="cp_overview"
>title="關於「控制面板」"
>abstract="「控制面板」首頁可讓您存取所有可在 Campaign 執行個體上執行的動作。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/accessing-control-panel.html?lang=zh-Hant" text="存取「控制面板」"

「Campaign 控制面板」可讓您以 Campaign Standard 和 v7/v8 產品管理員的身分，管理設定並追蹤每個 Campaign 執行個體的使用量，協助您提升工作效率。

## 新增功能

**使用者介面**

* 「控制面板」現在提供其他語言版本。 [了解更多](discover/using/discovering-the-interface.md#supported-languages-languages)

**作用中設定檔監控**

* 如果您正在使用多個執行個體，現在可以監視組織有權使用的作用中設定檔數量，以及組織內所有執行個體中使用的設定檔總數。[了解更多](performance-monitoring/using/active-profiles-monitoring.md)

**DMARC 記錄**

* 多個電子郵件地址現在可以接收彙總報告和失敗報告電子郵件。 [了解更多](subdomains-certificates/using/dmarc.md)
* 如果子網域同時存在 DMARC 和 BIMI 記錄，則已進行變更：

   * 無法刪除 DMARC 記錄。 如果要刪除其中一個，您必須先刪除 BIMI 記錄。
   * DMARC 記錄可加以編輯，但不允許將原則降級至「無」且其百分比值必須為 100。

>[!CAUTION]
>
>* 控制面板僅限管理員使用者存取。[瞭解更多](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=zh-Hant#discover-control-panel)
>
>* 對於 Campaign v7，則套用部署限制。 [了解更多](faq.md#v7-restrictions)

## 其他資源 {#additional-resources}

<table>
    <tr>
        <td><b>Campaign Standard</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/control-panel-overview.html?lang=zh-Hant">「控制面板」教學課程影片</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=zh-Hant">Campaign Standard 產品文件</a></li>
        </ul>
        </td>
        <td><b>Campaign v7</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/control-panel-overview.html?lang=zh-Hant">「控制面板」教學課程影片</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic/using/campaign-classic-home.html?lang=zh-Hant">Campaign v7 產品文件</a></li>
        </ul>
        </td>
        <td><b>Campaign v8</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-learn/control-panel/control-panel-overview.html?lang=zh-Hant">「控制面板」教學課程影片</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/campaign-home.html?lang=zh-Hant">Campaign v8 產品文件</a></li>
        </ul>
        </td>
    </tr>
</table>
