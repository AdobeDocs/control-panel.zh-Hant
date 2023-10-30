---
title: 發行說明 2023 年
description: 本頁面列出了「控制面板」的所有 2023 版本。
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 100%

---

# 發行說明 2023 年 {#rn-2023}

## 2023 年 9 月 {#september-2023}

<table>
<thead>
<tr>
<th><strong>DMARC 與 BIMI 記錄管理</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>您現在可以直接從「控制面板」新增 DMAR C和 BIMI 記錄：

<ul><li><strong>DMARC 記錄</strong>提供驗證寄件者網域的方式，並防止未經授權而惡意使用網域。 <a href="../subdomains-certificates/using/dmarc.md">瞭解如何新增 DMARC 記錄</a></li>
<li><strong>BIMI 記錄</strong>可讓您在郵箱提供者的收件匣中，於您的電子郵件旁邊顯示核准的標誌，以提升品牌認知度和信任度。 <a href="../subdomains-certificates/using/bimi.md">瞭解如何新增 BIMI 記錄</a></li></ul>
</td>
</tr>
</tbody>
</table>

## 2023 年 6 月 {#june-2023}

* 您現在可以直接從子網域清單將已委派子網域的 SSL 憑證委派給 Adobe。 [了解更多](../subdomains-certificates/using/delegate-ssl.md)

* 警報電子郵件寄件者已變更為 `"alert@notifications.campaign.adobe.com"`。

## 2023 年 5 月改進項目 {#may-2023}

**子網域的 SSL 憑證委派給 Adobe**

您現在可以透過 Adobe 管理子網域的 SSL 憑證。 如果您是使用 CNAME 設定子網域，就會自動產生和提供憑證記錄，以便在您的網域託管解決方案中產生憑證。

請注意，只有在設定新的子網域時才可使用此功能。您無法為現有的委派子網域委派憑證。[了解更多](../subdomains-certificates/using/setting-up-new-subdomain.md)

>[!NOTE]
>
>Adobe 受管理 SSL 是免費提供給使用者的功能。

## 2023 年 3 月 {#march-2023}

**CNAME 子網域委派移除**

您現在可以移除由 CNAME 設定的子網域委派。 [了解更多](../subdomains-certificates/using/remove-delegated-subdomains.md)

## 2023 年 2 月 {#february-2023}

**已委派給 Adobe 的子網域委派移除**

您現在可以移除已完全委派給 Adobe 的子網域委派。[了解更多](../subdomains-certificates/using/remove-delegated-subdomains.md)

>[!NOTE]
>
>已使用 CNAME 設定的子網域目前無法使用委派移除功能。

**服務行事曆**

服務行事曆現提供行事曆檢視，以追蹤執行個體發生的重要事件。 此外，針對訂閱「控制面板」警示的使用者，已新增資訊至向其傳送的通知。 [了解更多](../service-events/service-events.md)

![](assets/do-not-localize/gif-calendar.gif)

## 2023 年 1 月 {#january-2023}

**新混合託管模式功能**

擁有混合託管模式的客戶現在可將 IP 位址新增至允許清單，以存取 MID 執行個體。 [了解更多](../instances-settings/using/ip-allow-listing-instance-access.md)

**憑證申請檔 (CSR) 增強功能**

在產生憑證申請檔期間，城市/位置欄位現為選用欄位。
