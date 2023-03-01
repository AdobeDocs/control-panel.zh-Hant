---
product: campaign
solution: Campaign
title: 續約子網域的 SSL 憑證
description: 瞭解如何續約子網域的 SSL 憑證
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 963c2af5cdca80ebc2cd79e0708dc4dfe8c6ec1e
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 100%

---

# 正在續約 SSL 憑證 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="SSL 憑證續約"
>abstract="若要續約 SSL 憑證，您必須產生 CSR、購買子網域的 SSL 憑證並安裝憑證套裝。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renew-ssl/renewing-subdomain-certificate.html?lang=zh-Hant" text="正在產生憑證申請檔 (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renew-ssl/renewing-subdomain-certificate.html?lang=zh-Hant" text="安裝 SSL 憑證"

SSL 憑證續約流程包含 3 個步驟：

1. **產生憑證申請檔 (CSR)**

   您必須在購買憑證之前，先針對您打算保護的執行個體和子網域產生憑證申請檔。您需要提供產生 CSR 所需的一些資訊 (例如通用名稱、組織名稱和地址等等)。[了解更多](generate-csr.md)

1. **購買 SSL 憑證**

   產生 CSR 後，您可以使用它從貴公司核准的憑證機構購買的 SSL 憑證。

1. **安裝 SSL 憑證**

   安裝購買的 SSL 憑證到所需的子網域上以保護它們。 [了解更多](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png)利用 [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=zh-Hant) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=zh-Hant) 在影片中瞭解此功能

**相關主題：**

* [傳遞能力最佳實務指南 — Adobe Campaign 的 SSL 憑證請求流程](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=zh-Hant)
* [子網域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
* [監視子網域](../../subdomains-certificates/using/monitoring-subdomains.md)
