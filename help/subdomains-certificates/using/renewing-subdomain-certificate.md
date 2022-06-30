---
product: campaign
solution: Campaign
title: 續約子網域的 SSL 憑證
description: 瞭解如何續約子網域的 SSL 憑證
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 5a5ac1a604fe5bdce07479ff84184abdb2e0ddba
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 28%

---

# 正在續訂SSL證書 {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="SSL證書續訂"
>abstract="要續訂SSL證書，您需要生成CSR，為子域購買SSL證書，並安裝證書包。"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="產生憑證簽署要求 (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="安裝SSL證書"

>[!IMPORTANT]
>
>從「控制面板」續訂SSL證書在測試版中提供，並且需要頻繁更新和修改，恕不另行通知。
>
>如果使用具有混合宿主模型的實例，則只能查看與委託子域關聯的證書，並且無法續訂這些證書。

SSL 憑證續約流程包含 3 個步驟：

1. **證書籤名請求(CSR)的生成**

   您必須在購買憑證之前，先針對您打算保護的執行個體和子網域產生憑證簽署要求。您需要提供產生 CSR 所需的一些資訊 (例如通用名稱、組織名稱和地址等等)。[了解更多](generate-csr.md)

1. **購買SSL證書**

   生成CSR後，您可以使用它從您公司批准的證書頒發機構購買SSL證書。

1. **安裝SSL證書**

   將購買的SSL證書安裝到所需的子域上以保護它們。 [了解更多](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) 使用 [市場活動v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#subdomains-and-certificates) 或 [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#adding-ssl-certificates)

**相關主題：**

* [可交付性最佳實踐指南 — Adobe Campaign的SSL證書申請流程](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html)
* [子網域品牌化](../../subdomains-certificates/using/subdomains-branding.md)
* [監視子網域](../../subdomains-certificates/using/monitoring-subdomains.md)
