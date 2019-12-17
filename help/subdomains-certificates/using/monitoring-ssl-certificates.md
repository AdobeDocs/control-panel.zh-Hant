---
title: 監視子域的SSL證書
description: 瞭解如何監控子網域的SSL憑證
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# 監視子域的SSL證書 {#monitoring-ssl-certificates}

Adobe Campaign建議您保護裝載著陸頁面的子網域，尤其是收集客戶敏感資訊的子網域。

**SSL(安全通訊端層** )加密可確保您委派給Adobe的子網域安全無虞。 當您的客戶填寫網頁表格或造訪Adobe Campaign代管的登陸頁面時，依預設會透過非安全通訊協定(HTTP)傳送資訊。 為確保額外的安全性，請使用HTTPS通訊協定來保護傳送的資訊。 例如，您的「http://info.mywebsite.com/」子網域位址現在會是「https://info.mywebsite.com/」。

**委派的子網域本身不會安裝SSL憑證**。 它們會安裝在相關的子網域上，主要是裝載著陸頁面、資源頁面等的子網域。

**SSL憑證會提供特定時段** （1年、60天等）。 一旦憑證過期，您在存取登陸頁面或使用子網域的資源時可能會遇到問題。 為避免此問題，「控制面板」可讓您監控子網域的SSL憑證，並啟動其續約程式。

![](assets/no_certificate.png)

如果您的子網域的其中一個SSL憑證即將過期，您可以直接從「控制面板」續約。 如需更多相關資訊，請參閱本節：續 [約子網域的SSL憑證](../../subdomains-certificates/using/renewing-subdomain-certificate.md)。
