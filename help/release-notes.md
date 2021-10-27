---
product: campaign
solution: Campaign
title: 「控制面板」發行版本
description: 最新「控制面板」發行說明。
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 23c2cd3172a846c1006fc172acf07cae1f222a9c
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 71%

---

# 「控制面板」發行版本 {#control-panel-releases}

您可以在此處找到最新「控制面板」發行版本的資訊。

>[!NOTE]
>
>所有管理員使用者都可存取控制面板。 授予使用者管理員存取權限的步驟已詳載於[本章節](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html#discover-control-panel)。
>
>若是Campaign Classicv7，請注意您的執行個體必須托管在AWS上，並以最新的 [Gold Standard](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/gs-release/gs-overview.html?lang=zh-Hant) 建置或 [最新GA版本編號(21.1)](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/latest-release.html?lang=zh-Hant#release-notes). 在[本章節](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=zh-Hant#getting-your-campaign-version)中瞭解如何確認您的版本。 若要檢查您的執行個體是否託管在 AWS 上，請按照[本頁面](faq.md)詳述的步驟操作。

## 2021 年 10 月 {#october-2021}

**IP範圍和公鑰有效期**

您現在可以設定IP範圍和公開金鑰可用時間。 請參閱 [IP範圍允許清單](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) 和 [金鑰管理](sftp/using/key-management.md#installing-ssh-key) 區段。

**IP範圍和公開密鑰版本**

您現在可以編輯 [IP範圍](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) 和 [公用金鑰](sftp/using/key-management.md#editing-public-keys) 由您建立。 請注意，此功能不適用於目前「控制面板」發行版本之前建立的項目。

**SFTP IP範圍和公開金鑰過期的警報**

電子郵件警報功能現在包含SFTP IP的警報，允許清單過期和SFTP公開金鑰過期。 [了解更多](performance-monitoring/using/email-alerting.md)

**透過Campaign v8提供完整支援**

此 **子網域** 和 **憑證** Adobe Campaign v8上的「控制面板」現在支援管理功能。

## 2021 年 8 月 {#august-2021}

**支援Campaign v8**

「控制面板」現在可供Adobe Campaign v8使用，但 **子網域** 和 **憑證** 尚未支援的管理功能。 深入了解 [Campaign v8檔案](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html){target=&quot;_blank&quot;}

## 2020 年 10 月 {#october-2020}

**子網域設定使用 CNAME**

「控制面板」現在允許您直接從介面設定子網域以使用 CNAME 與 Adobe 協作。[顯示全文](subdomains-certificates/using/setting-up-new-subdomain.md)

**資料庫監視增強功能**

資料庫監視已通過其他度量得到增強，這些度量允許您獲取有關佔用資料庫空間的資源的詳細資訊。 [顯示全文](performance-monitoring/using/database-monitoring.md)

## 2020 年 6 月 {#june-2020}

**子網域傳遞稽核**

委派新子網域後，「控制面板」現在可讓您追蹤傳遞團隊所執行的稽核。[詳細內容](subdomains-certificates/using/setting-up-new-subdomain.md)

**GPG 金鑰管理**

「控制面板」現在可讓您產生一對 GPG 金鑰，讓您可以輕鬆解密從外部傳到 Campaign 的資料。此外，我們新增了一項功能，讓您可以安裝公用 GPG 金鑰來加密離開 Campaign 的資料。[詳細內容](instances-settings/using/gpg-keys-management.md)

**作用中設定檔監控**

「控制面板」現在可讓您監控執行個體使用的作用中設定檔數目，而且會計算這些設定檔數目以結算費用。[詳細內容](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>從「控制面板」進行作用中設定檔監控的功能會在測試版提供，且可能會不時更新和修改，恕不另行通知。

## 2020 年 5 月 {#may-2020}

**CNAME 子網域的憑證管理**

「控制面板」現在可讓您續約已透過 CNAME 方法設定之子網域的 SSL 憑證。[了解更多](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2020 年 4 月 {#april-2020}

**Google TXT 記錄管理**

您可以透過 Campaign「控制面板」，將 Google TXT 網站驗證記錄新增至所有用於傳送電子郵件至 Gmail 地址的子網域。[詳細內容](subdomains-certificates/using/managing-txt-records.md)

**資料庫空間監視**

Campaign「控制面板」具備資料庫監視功能，可讓您隨選及隨時檢視您的資料庫空間使用率。[詳細內容](performance-monitoring/using/database-monitoring.md)

**電子郵件警報**

Campaign「控制面板」具備即時電子郵件警報功能，可讓您登入「控制面板」並註冊接收警報。當您的系統存在效能降低的風險，或是需要採取行動來確保日後提供高效能的時候，您就會收到警報。[詳細內容](performance-monitoring/using/email-alerting.md)

## 2020 年 1 月 {#january-2020}

*2020 年 1 月 22 日*

我們已新增管理員使用者的功能，讓他們從「控制面板」設定子網域並續約 SSL 憑證。

如需詳細資訊，請參閱以下頁面：
* [設定新的子網域](subdomains-certificates/using/setting-up-new-subdomain.md)
* [續約子網域的 SSL 憑證](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>這些功能將會在測試版中提供，且可能會不時更新和修改，恕不另行通知。

## 2019 年 9 月 {#september-2019}

*2019 年 9 月 16 日*

我們已新增功能，讓管理員使用者將 IP 位址新增至允許清單，以便連線至 Campaign Classic 執行個體。
此外，管理員使用者現在可以檢視 Campaign Classic 執行個體的清單和資格，以建立升級。

如需詳細資訊，請參閱[專屬文件](instances-settings/using/ip-allow-listing-instance-access.md)。

## 2019 年 8 月 {#august-2019}

我們已新增管理員使用者的功能，讓他們在其網域的 SSL 憑證到期之前收到通知。如需詳細資訊，請參閱[詳細文件](subdomains-certificates/using/monitoring-ssl-certificates.md)。

此外，管理員使用者現在可以刪除已新增用於來存取 SFTP 伺服器的 SSH 金鑰。

## 2019 年 7 月 {#july-2019}

我們已新增管理員使用者的功能，讓他們對 Campaign Classic 執行個體設定有更全面的控制。全新的「控制面板」功能包括新增與 Adobe Campaign 連線的 URL，以進行資料/檔案傳輸。

如需詳細資訊，請參閱[詳細文件](instances-settings/using/url-permissions.md)。
