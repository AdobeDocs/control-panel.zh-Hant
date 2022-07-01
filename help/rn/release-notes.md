---
title: 最新版本
description: 此頁列出了控制面板的所有新功能和改進
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 737ff99e60bb940980f3b7179672fdb984e6d4bf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 10%

---

# 最新版本 {#control-panel-releases}

此頁列出了控制面板的新功能和改進。

## 2022 年 6 月 {#june-2022}

### 新增功能?

<table>
<thead>
<tr>
<th><strong>佔用SFTP伺服器空間的前10個檔案</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，您可以識別SFTP伺服器上佔用空間最多的前10個檔案。 <a href="../sftp/using/sftp-storage-management.md">了解更多</a></p>
<img src="../assets/do-not-localize/sftp.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>服務日曆提醒</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>服務日曆現在允許您設定提醒，以便在實例上發生事件之前通過電子郵件通知您。 <a href="../service-events/service-events.md">了解更多</a></p>
<img src="../assets/do-not-localize/reminders.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>子域的CSR生成增強</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>對CSR的生成過程進行了一些改進。 <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">了解更多</a></p><ul><li>生成CSR時，現在可以選擇包含的子域之一作為「公用名稱」。</li><li>現在，在生成CSR之前，可以複製CSR摘要。</li><li>生成CSR後，可以從作業日誌中再次下載。 此功能不適用於此版本之前生成的證書。</li></ul><p>
<img src="../assets/do-not-localize/CSR.gif"/>
</td>
</tr>
</tbody>
</table>

### 功能改進

**執行個體設定**

* 「Control Panel（控制面板）」中GPG鍵的最大數量已增加到60個鍵。 [了解更多](../instances-settings/using/gpg-keys-management.md)

