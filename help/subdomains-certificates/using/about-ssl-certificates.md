---
title: 關於SSL憑證
description: 進一步瞭解SSL憑證
translation-type: tm+mt
source-git-commit: 6bc165f995d34d21b5bce379db3095317db10906

---


# 關於SSL憑證 {#about-ssl-certificates}

Adobe Campaign建議您保護裝載著陸頁面的子網域，尤其是收集客戶敏感資訊的子網域。

**SSL(安全通訊端層** )加密可確保您委派給Adobe的子網域安全無虞。 當您的客戶填寫網頁表格或造訪Adobe Campaign代管的登陸頁面時，依預設會透過非安全通訊協定(HTTP)傳送資訊。 為確保額外的安全性，請使用HTTPS通訊協定來保護傳送的資訊。 例如，您的「http://info.mywebsite.com/」子網域位址現在會是「https://info.mywebsite.com/」。

**委派的子網域本身不會安裝SSL憑證**。 它們會安裝在相關的子網域上，主要是裝載著陸頁面、資源頁面等的子網域。

**SSL憑證會提供特定時段** （1年、60天等）。 一旦憑證過期，您在存取登陸頁面或使用子網域的資源時可能會遇到問題。 為避免此問題，「控制面板」可讓您監控子網域的SSL憑證，並啟動其續約程式。

有關子域委託的詳細資訊，請 [參閱](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html)。
