---
title: 「控制面板」發行版本
translation-type: tm+mt
source-git-commit: 759d3ca0c3cafa84067c31a48432b0bfe2df186f
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 70%

---


# 「控制面板」發行版本{#control-panel-releases}

您可以在此處找到最新「控制面板」發行版本的資訊。

>[!NOTE]
>
>請注意，「控制面板」僅適用於託管在 AWS 的客戶，我們目前並不支援混合環境。存取「控制面板」並不需要升級。請確定您是管理員使用者，才能加以存取。

## 2020年6月 {#june-2020}

**子網域傳遞能力審核**

委派新子網域後，「控制面板」現在可讓您追蹤「傳遞性」團隊執行的稽核。 [詳細內容](subdomains-certificates/using/setting-up-new-subdomain.md)

**GPG 金鑰管理**

「控制面板」現在可讓您產生一對 GPG 金鑰，讓您可以輕鬆解密從外部傳到 Campaign 的資料。此外，我們新增了一項功能，讓您可以安裝公用 GPG 金鑰來加密離開 Campaign 的資料。[詳細內容](instances-settings/using/gpg-keys-management.md)

**刪除「白名單」/「黑名單」**

「白名單」和「黑名單」詞語都已從Adobe Campaign檔案中移除。 產品UI、選項名稱和內部代碼中可能仍會出現這些詞語，但在即將發行的促銷活動版本中，這些詞語會以「blocklist」和「allowlist」取代。

**活動配置檔案監控**

「控制面板」現在可讓您監控執行個體使用並計為計費用的作用中描述檔數目。 [詳細內容](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>Beta版提供「控制面板」中的作用中描述檔監控功能，並會經常更新和修改，恕不另行通知。
>
>此功能適用於AWS上代管的客戶，這些客戶來自Campaign Standard 10368構建版和Campaign Classic 8931構建版。 如果您使用舊版軟體，則需要升級才能使用此功能。

## 2020年5月 {#may-2020}

**CNAME 子網域的憑證管理**

「控制面板」現在可讓您續約已透過 CNAME 方法委派之子網域的 SSL 憑證。[詳細內容](subdomains-certificates/using/renewing-subdomain-certificate.md)

## 2020 年 4 月{#april-2020}

**Google TXT 記錄管理**

您可以透過 Campaign「控制面板」，將 Google TXT 網站驗證記錄新增至所有用於傳送電子郵件至 Gmail 地址的子網域。[詳細內容](subdomains-certificates/using/managing-txt-records.md)

**資料庫空間監視**

Campaign「控制面板」具備資料庫監視功能，可讓您隨選及隨時檢視您的資料庫空間使用率。[詳細內容](performance-monitoring/using/database-monitoring.md)

**電子郵件警報**

Campaign「控制面板」具備即時電子郵件警報功能，可讓您登入「控制面板」並註冊接收警報。當您的系統存在效能降低的風險，或是需要採取行動來確保日後提供高效能的時候，您就會收到警報。[詳細內容](performance-monitoring/using/email-alerting.md)

## 2020 年 1 月{#january-2020}

*2020 年 1 月 22 日*

我們已新增管理員使用者的功能，讓他們從「控制面板」委派子網域並續約 SSL 憑證。

如需詳細資訊，請參閱以下頁面：
* [設定新子網域](subdomains-certificates/using/setting-up-new-subdomain.md)
* [續約子網域的 SSL 憑證](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>這些功能將會在測試版中提供，且可能會不時更新和修改，恕不另行通知。

## 2019 年 9 月{#september-2019}

*2019 年 9 月 16 日*

我們已新增功能，讓管理員使用者將IP位址新增至允許清單，以便連線至Campaign Classic例項。
此外，管理員使用者現在可以檢視 Campaign Classic 執行個體的清單和資格，以建立升級。

如需詳細資訊，請參閱[專屬文件](instances-settings/using/ip-whitelisting-instance-access.md)。

## 2019 年 8 月{#august-2019}

我們已新增管理員使用者的功能，讓他們在其網域的 SSL 憑證到期之前收到通知。如需詳細資訊，請參閱[詳細文件](subdomains-certificates/using/monitoring-ssl-certificates.md)。

此外，管理員使用者現在可以刪除已新增用於來存取 SFTP 伺服器的 SSH 金鑰。

## 2019 年 7 月{#july-2019}

我們已新增管理員使用者的功能，讓他們對 Campaign Classic 執行個體設定有更全面的控制。全新的「控制面板」功能包括新增與 Adobe Campaign 連線的 URL，以進行資料/檔案傳輸。

如需詳細資訊，請參閱[詳細文件](instances-settings/using/url-permissions.md)。
