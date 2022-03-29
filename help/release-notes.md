---
product: campaign
solution: Campaign
title: 「控制面板」發行版本
description: 此頁列出了控制面板的所有新功能和改進
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 84fe0aeb10bc5e535a7ab54a3316a51a1a32b3ca
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 63%

---

# 「控制面板」發行版本 {#control-panel-releases}

此頁列出了控制面板的所有新功能和改進。

>[!NOTE]
>
>控制面板僅可供管理員用戶訪問。 瞭解有關中權限的詳細資訊 [此部分](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=zh-Hant#discover-control-panel)。
>
>對於活動v7，您的實例必須托管在Amazon Web Services(AWS)上，並升級到最新版本 [活動穩定構建](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=zh-Hant#rn-statuses) （或建9032或更高）。 在[本章節](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=zh-Hant#getting-your-campaign-version)中瞭解如何確認您的版本。 若要檢查您的執行個體是否託管在 AWS 上，請按照[本頁面](faq.md#hosted-aws)詳述的步驟操作。

## 2022 年 3 月 {#march-2022}

<table>
<thead>
<tr>
<th><strong>吞吐量和延遲監視可用性</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>吞吐量和延遲監控現在可供所有具有獨立部署（沒有任何中間實例）的內部版本號9032、9330、9346或9349的Campaign Standard和v8客戶使用。</p><p>有關詳細資訊，請參閱 <a href="performance-monitoring/using/thoughputs-latencies.md">詳細文檔。</a></p>
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
<p>您現在可以監視可能需要特別注意的工作流程參數，以避免執行個體上出現任何問題。  </p><p>如需詳細資訊，請參閱<a href="performance-monitoring/using/workflow-monitoring.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

## 2022 年 1 月 {#january-2022}

<table>
<thead>
<tr>
<th><strong>使用中查詢監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>允許您可以藉由控制面板監視在執行個體上執行時間最長的查詢。 </p><p>如需詳細資訊，請參閱<a href="performance-monitoring/using/database-active-queries.md">詳細文件</a>以瞭解詳情。</p>
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
<p>您現在可以監視執行個體上一段時間內的傳遞輸送量和延時趨勢。 </p><p>如需詳細資訊，請參閱<a href="performance-monitoring/using/thoughputs-latencies.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>新子域上的SSL證書操作</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，即使可交付性審核仍在進行中，也可以對新設定的子域執行SSL證書操作。</p><p>如需詳細資訊，請參閱<a href="subdomains-certificates/using/renewing-subdomain-certificate.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

## 2021 年 10 月 {#october-2021}

<table>
<thead>
<tr>
<th><strong>IP範圍與公鑰有效期</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在，可以為IP範圍和公鑰的可用性設定持續時間。 </p><p>有關詳細資訊，請參閱 <a href="sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list">IP範圍允許清單</a> 和 <a href="sftp/using/key-management.md#installing-ssh-key">密鑰管理</a> 的下界。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP範圍和公鑰版本</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>現在可以編輯 <a href="sftp/using/ip-range-allow-listing.md#editing-ip-ranges">IP範圍</a> 和 <a href="sftp/using/key-management.md#editing-public-keys">公鑰</a> 你創造的。 請注意，此功能不適用於當前「控制面板」發佈前建立的項目。
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SFTP IP範圍和公鑰到期警報</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件警報功能現在包括有關SFTP IP的警報，允許列出過期和SFTP公鑰過期。</p><p>如需詳細資訊，請參閱<a href="performance-monitoring/using/email-alerting.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>透過 Campaign v8 提供完整支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>的 <strong>子域</strong> 和 <strong>證書</strong> 管理功能現在由Adobe Campaignv8上的控制面板支援。</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2021 年 8 月 {#august-2021}

<table>
<thead>
<tr>
<th><strong>支援活動v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>控制面板現在可用於Adobe Campaignv8，但 <strong>子域</strong> 和 <strong>證書</strong> 管理權能，但尚不受支援。</p><p>有關詳細資訊，請參閱 <a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html" target="blank">市場活動v8文檔</a>。</p>
</td>
</tr>
</tbody>
</table>

## 2020 年 10 月 {#october-2020}

<table>
<thead>
<tr>
<th><strong>利用 CNAME 設定子網域</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>「控制面板」現在允許您直接從介面設定子網域以使用 CNAME 與 Adobe 協作。</p><p>如需詳細資訊，請參閱<a href="subdomains-certificates/using/setting-up-new-subdomain.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>資料庫監視增強功能</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>資料庫監視已通過其他度量得到增強，這些度量允許您獲取有關佔用資料庫空間的資源的詳細資訊。</p><p>如需詳細資訊，請參閱<a href="performance-monitoring/using/database-monitoring.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

## 2020 年 6 月 {#june-2020}

<table>
<thead>
<tr>
<th><strong>子網域傳遞稽核</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>委派新子網域後，「控制面板」現在可讓您追蹤傳遞團隊所執行的稽核。</p><p>如需詳細資訊，請參閱<a href="subdomains-certificates/using/setting-up-new-subdomain.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>GPG 金鑰管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>「控制面板」現在可讓您產生一對 GPG 金鑰，讓您可以輕鬆解密從外部傳到 Campaign 的資料。此外，我們新增了一項功能，讓您可以安裝公用 GPG 金鑰來加密離開 Campaign 的資料。</p><p>如需詳細資訊，請參閱<a href="instances-settings/using/gpg-keys-management.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>使用中設定檔監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>「控制面板」現在可讓您監控執行個體使用的作用中設定檔數目，而且會計算這些設定檔數目以結算費用。</p><p>如需詳細資訊，請參閱<a href="performance-monitoring/using/active-profiles-monitoring.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>從「控制面板」進行作用中設定檔監控的功能會在測試版提供，且可能會不時更新和修改，恕不另行通知。

## 2020 年 5 月 {#may-2020}

<table>
<thead>
<tr>
<th><strong>CNAME 子網域的憑證管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>「控制面板」現在可讓您續約已透過 CNAME 方法設定之子網域的 SSL 憑證。</p><p>如需詳細資訊，請參閱<a href="subdomains-certificates/using/renewing-subdomain-certificate.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

## 2020 年 4 月 {#april-2020}

<table>
<thead>
<tr>
<th><strong>Google TXT 記錄管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您可以透過 Campaign「控制面板」，將 Google TXT 網站驗證記錄新增至所有用於傳送電子郵件至 Gmail 地址的子網域。</p><p>如需詳細資訊，請參閱<a href="subdomains-certificates/using/managing-txt-records.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>資料庫空間監視</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Campaign「控制面板」具備資料庫監視功能，可讓您隨選及隨時檢視您的資料庫空間使用率。</p><p>如需詳細資訊，請參閱<a href="performance-monitoring/using/database-monitoring.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>電子郵件警示</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Campaign「控制面板」具備即時電子郵件警報功能，可讓您登入「控制面板」並註冊接收警報。當您的系統存在效能降低的風險，或是需要採取行動來確保日後提供高效能的時候，您就會收到警報。</p><p>如需詳細資訊，請參閱<a href="performance-monitoring/using/email-alerting.md">詳細文件</a>以瞭解詳情。</p>
</td>
</tr>
</tbody>
</table>

## 2020 年 1 月 {#january-2020}

我們已新增管理員使用者的功能，讓他們從「控制面板」設定子網域並續約 SSL 憑證。

如需詳細資訊，請參閱以下頁面：
* [設定新的子網域](subdomains-certificates/using/setting-up-new-subdomain.md)
* [續約子網域的 SSL 憑證](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>這些功能將會在測試版中提供，且可能會不時更新和修改，恕不另行通知。

## 2019 年 9 月 {#september-2019}

我們為管理員用戶添加了新功能，以便將IP地址添加到允許清單中，以便連接到Campaign v7/v8實例。
此外，管理員用戶現在可以查看市場活動v7/v8實例的清單以及生成升級的資格。

如需詳細資訊，請參閱[專屬文件](instances-settings/using/ip-allow-listing-instance-access.md)。

## 2019 年 8 月 {#august-2019}

我們已新增管理員使用者的功能，讓他們在其網域的 SSL 憑證到期之前收到通知。如需詳細資訊，請參閱[詳細文件](subdomains-certificates/using/monitoring-ssl-certificates.md)。

此外，管理員使用者現在可以刪除已新增用於來存取 SFTP 伺服器的 SSH 金鑰。

## 2019 年 7 月 {#july-2019}

我們添加了新功能，使管理員用戶能夠更好地控制Campaing v7/v8實例設定。 全新的「控制面板」功能包括新增與 Adobe Campaign 連線的 URL，以進行資料/檔案傳輸。

如需詳細資訊，請參閱[詳細文件](instances-settings/using/url-permissions.md)。
