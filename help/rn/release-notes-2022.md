---
title: 發行說明 2022 年
description: 本頁面列出了「控制面板」的所有 2022 版本。
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9fb18bb6-c4e4-48aa-849c-d9129add5266
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 100%

---

# 發行說明 2022 年 {#rn-2022}

## 2022 年 10 月 {#october-2022}

電子郵件警示現在會在您的其中一個 SSL 憑證於 30 天或更短時間內到期時通知您。 [了解更多](../performance-monitoring/using/email-alerting.md)

## 2022 年 9 月 {#september-2022}

擁有混合託管模型的客戶現在可以設定新的子網域。 [了解更多](../subdomains-certificates/using/setting-up-new-subdomain.md)

## 2022 年 8 月 {#august-2022}

* 擁有混合託管模型的客戶現在可以驗證其子網域。 [了解更多](../subdomains-certificates/using/monitoring-subdomains.md)
* 組織單位 (OU) 欄位現在在憑證產生請求 (CSR) 中為選用欄位。 [了解更多](../subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2022 年 7 月 {#july-2022}

<table>
<thead>
<tr>
<th><strong>子網域用於混合託管模型的憑證安裝</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>使用混合託管模型的客戶現在可以從「控制面板」續約其子網域的 SSL 憑證。</p><p>如需詳細資訊，請參閱<a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2022 年 6 月 {#june-2022}

### 新增功能?

<table>
<thead>
<tr>
<th><strong>佔用 SFTP 伺服器空間的前 10 個檔案</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在您可以識別 SFTP 伺服器上佔用最多空間的前 10 個檔案。 <a href="../sftp/using/sftp-storage-management.md">了解更多</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>服務行事曆提醒</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>服務行事曆現在允許您設定提醒，以便在執行個體的事件發生之前透過電子郵件通知您。 <a href="../service-events/service-events.md">了解更多</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>子網域的 CSR 產生增強功能</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>對 CSR 的產生過程進行了一些功能增強。 <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">了解更多</a></p><ul><li>產生 CSR 時，現在可以選擇所包含的子網域中之一作為「一般名稱」。</li><li>現在產生 CSR 之前，可以複製 CSR 摘要。</li><li>產生 CSR 之後，可以從作業記錄中重新下載。 此功能不適用於此版本之前產生的憑證。</li></ul><p>

</td>
</tr>
</tbody>
</table>

### 功能改進

**執行個體設定**

* 「控制面板」中 GPG 金鑰的最大數量已增加到 60 個。 [了解更多](../instances-settings/using/gpg-keys-management.md)

## 2022 年 5 月 {#may-2022}

<table>
<thead>
<tr>
<th><strong>混合託管模型可使用控制面板的程度</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>控制面板現在可供混合託管模型的客戶使用。 這些客戶可以利用控制面板的功能，在控制面板的行銷執行個體提供他們的 MID/RT 執行個體 URL。 </p><p>如需詳細資訊，請參閱<a href="../instances-settings/using/external-accounts.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>輸送量及延時監視更新</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>已增強輸送量及延時監視能力：<ul><li>您現在可以識別影響執行個體輸送量的前 5 個傳遞的 ID。</li><li>Campaign Classic v7/v8 客戶現在可以顯示特定頻道的延時。</p></li><p>如需詳細資訊，請參閱<a href="../performance-monitoring/using/throughputs-latencies.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


## 2022 年 4 月 {#april-2022}

<table>
<thead>
<tr>
<th><strong>監視執行個體上的主要聯絡人和事件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以監視執行個體上過去和即將發佈的版本和服務審查，並為某項請求或問題存取 Adobe 的主要聯絡人清單。 </p><p>如需詳細資訊，請參閱<a href="../service-events/service-events.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2022 年 3 月 {#march-2022}

<table>
<thead>
<tr>
<th><strong>輸送量和延時監視能力</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>輸送量和延時監視功能適用於所有 Campaign Standard 和 v8 客戶，以及版本編號為 9032、9330、9346 或 9349 且已具有獨立部署 (沒有任何中型執行個體) 的 Campaign v7 客戶。</p><p>如需詳細資訊，請參閱<a href="../performance-monitoring/using/throughputs-latencies.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2022 年 2 月 {#february-2022}

<table>
<thead>
<tr>
<th><strong>工作流程參數監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以監視可能需要特別注意的工作流程參數，以避免執行個體上出現任何問題。  </p><p>如需詳細資訊，請參閱<a href="../performance-monitoring/using/workflow-monitoring.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

## 2022 年 1 月 {#january-2022}

<table>
<thead>
<tr>
<th><strong>作用中查詢監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>允許您可以藉由控制面板監視在執行個體上執行時間最長的查詢。 </p><p>如需詳細資訊，請參閱<a href="../performance-monitoring/using/database-active-queries.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>輸送量和延時監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以監視執行個體上一段時間內的傳遞輸送量和延時趨勢。 </p><p>如需詳細資訊，請參閱<a href="../performance-monitoring/using/throughputs-latencies.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新子網域上的 SSL 憑證作業</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，即使傳遞能力稽核仍在進行中，也可以對新設定的子網域執行 SSL 憑證作業。</p><p>如需詳細資訊，請參閱<a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>
