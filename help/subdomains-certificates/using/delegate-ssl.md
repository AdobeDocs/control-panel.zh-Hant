---
product: campaign
solution: Campaign
title: 將子網域的 SSL 憑證委派給 Adobe
description: 了解如何將子網域的 SSL 憑證委派給 Adobe
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a2b3d409-704b-4e81-ae40-b734f755b598
source-git-commit: 31d181770474428a7b42e96f2e603cc820db48d4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 61%

---

# 將子網域的 SSL 憑證委派給 Adobe {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="將子網域的 SSL 憑證委派給 Adobe"
>abstract="控制面板可讓您將子網域的 SSL 憑證交由 Adobe 管理。如果您是使用 CNAME 設定子網域，就會自動產生和提供憑證記錄，以便在您的網域託管解決方案中產生憑證。"

強烈建議將子網域的 SSL 憑證委派給 Adobe 管理，因為 Adobe 每年都會在憑證過期前，自動建立並更新憑證。

如果您使用 CNAME 來設定子網域委派，Adobe 將提供憑證記錄，以用於網域託管解決方案來產生憑證。

設定新的子網域時，或針對已委派的子網域，都可以執行將 SSL 憑證委派給 Adobe。

>[!NOTE]
>
>Adobe 受管理 SSL 是免費提供給使用者的功能。將子網域的憑證委派給 Adobe 是透明的，對您的行銷活動和傳遞能力沒有影響。 [了解更多 SSL 憑證管理相關資訊](monitoring-ssl-certificates.md#management)


## 委派新子網域的 SSL 憑證 {#new}

若要在設定新子網域時委派 SSL 憑證，請啟用子網域設定精靈的&#x200B;**[!UICONTROL 為子網域選擇 Adobe 管理的 SSL]** 選項。 憑證產生程式會依您的子網域委派方法而有所不同：

* **完整子網域委派**： Adobe會自動要求並安裝SSL憑證，您無需採取任何動作。 提交子網域設定後，系統就會立即處理憑證安裝請求，做為子網域設定工作流程的一部分。 [深入瞭解完整子網域委派](setting-up-new-subdomain.md#full-subdomain-delegation)

* **CNAME委派**：稍後將在設定精靈中提供要複製到您的託管解決方案的憑證記錄。 提交子網域設定之前，您需要在網域託管解決方案中產生這些憑證記錄。 [深入瞭解CNAME委派](setting-up-new-subdomain.md#use-cnames)

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## 針對已委派的子網域委派 SSL 憑證 {#delegated}

若要針對已委派的子網域委派 SSL 憑證，請按一下所需子網域旁的省略符號按鈕，然後按一下&#x200B;**[!UICONTROL 切換到受管理的 SSL]**。

![](assets/delegate-ssl-list.png){width="70%" align="left"}

憑證產生程式取決於子網域的原始設定方式：

### 完全委派的子網域

對於使用完整子網域委派(具有Adobe名稱伺服器)設定的子網域，Adobe會自動請求並安裝SSL憑證。 在您按一下&#x200B;**[!UICONTROL 切換至受管理的SSL]**&#x200B;並進行確認後，憑證安裝要求會立即送出，無需您採取任何額外動作。

### CNAME委派的子網域

對於使用CNAME委派設定的子網域，會顯示一個對話方塊，其中包含Adobe自動產生的憑證記錄。 逐一複製這些記錄，或下載 CSV 檔案，然後瀏覽至網域託管解決方案，以產生相符的憑證。

請確定已在網域託管解決方案中產生所有憑證記錄。 如果所有項目都已正確設定，請確認記錄建立完成，然後按一下&#x200B;**[!UICONTROL 提交]**。

![](assets/delegate-ssl.png){width="70%" align="left"}
