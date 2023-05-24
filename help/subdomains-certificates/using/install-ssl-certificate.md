---
product: campaign
solution: Campaign
title: 續約子網域的 SSL 憑證
description: 瞭解如何續約子網域的 SSL 憑證
feature: Control Panel
role: Architect
level: Experienced
exl-id: af440b5d-1d21-44fb-831f-f2bdd6011b82
source-git-commit: 9be5a3ae48dccf74f509aa95fee29bbfdafddcdf
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 90%

---

# 安裝 SSL 憑證 {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="SSL 憑證安裝"
>abstract="安裝您從貴組織核准的憑證機構購買的 SSL 憑證。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=zh-Hant" text="關於子網域名稱"

購買 SSL 憑證後，您就可以將它安裝在您的執行個體上。繼續操作之前，請確定您已瞭解下列必要條件：

* 憑證簽署要求 (CSR) 必須從「控制面板」產生。否則，您將無法從「控制面板」安裝憑證。
* 證書籤名請求(CSR)應與已配置為使用Adobe的子域匹配。 例如，它不能包含比已配置的子域多的子域。
* 憑證應具有目前日期。您不能安裝具有未來日期的憑證，也不應安裝過期的應憑證 (即有效的開始日期和結束日期)。
* 憑證應由受信任的憑證機構 (CA) 核發，例如 Comodo、DigiCert、GoDaddy 等等。
* 憑證大小應為 2048 位元，演算法應為 RSA。
* 憑證應為 X.509 PEM 格式。
* 支援 SAN 憑證。
* 不支援萬用字元憑證。
* ZIP 檔案或憑證不應受密碼保護。
* ZIP 檔案應在個別檔案中只包含下列內容：
   * 終端實體憑證。
   * 中繼憑證鏈 (依適當順序排列)。
   * 根憑證 (選填)。

請依照下列步驟以安裝憑證：

1. 在「**[!UICONTROL Subdomains & Certificates]**」卡片中，選取所需的執行個體，再按一下 **[!UICONTROL Manage Certificate]** 按鈕。

   ![](assets/renewal1.png)

1. 選取「**[!UICONTROL 3 - Install Certificate Bundle]**」，然後按一下「**[!UICONTROL Next]**」以啟動精靈，引導您完成憑證安裝流程。

   ![](assets/install1.png)

1. 選取包含要安裝之憑證的 .zip 檔案，然後按一下「**[!UICONTROL Submit]**」。

   ![](assets/install2.png)

>[!NOTE]
>
>此憑證將會安裝在 CSR 中包含的所有網域/子網域上。憑證中出現的任何其他網域/子網域都不會考慮在內。

安裝 SSL 憑證後，憑證的到期日和狀態圖示會隨之更新。
