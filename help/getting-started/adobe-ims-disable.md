---
title: 停用Commerce管理員與Adobe ID的整合
description: 請依照此選擇性程式來停用Adobe Commerce與Adobe IMS的管理員整合。
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# 停用Commerce管理員與Adobe ID的整合

{{ee-feature}}

已將Commerce執行個體與Adobe IMS驗證工作流程整合的商家可能需要停用此選擇性整合。

IMS整合停用後，Commerce部署會還原為預設的Commerce驗證工作流程和密碼原則。 啟用或停用此整合時，只會影響管理員使用者工作流程。

另請參閱 [您的管理員帳戶](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) 以概略瞭解Commerce管理員登入。

## 步驟1：停用整合

您無法從Admin停用這項整合。 若要停用Adobe IMS與Commerce的整合，並將Commerce驗證恢復為預設狀態，您必須從命令列介面停用整合。

若要停用整合：

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce在成功時顯示下列訊息：

```terminal
Admin Adobe IMS integration is disabled.
```

## 步驟2：建立或擷取您的Commerce密碼

停用整合後，管理員使用者必須使用Commerce密碼登入管理員。

* 記得先前已有的Commerce密碼（即在進行IMS整合之前建立的Commerce密碼）的Commerce管理員使用者，可使用此密碼登入管理員。

* 不具有既有Commerce密碼或忘記密碼的Commerce管理員使用者必須建立新密碼。 若要建立新密碼，管理員使用者可以使用 [!UICONTROL Forgot your password?] 功能，用來建立新密碼。 另請參閱 [重設客戶密碼](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce不接受空白密碼欄位。

## 停用整合後

IMS整合停用後，預設的Commerce驗證工作流程會繼續，並再次提示管理員使用者輸入密碼。

停用IMS整合會刪除啟用整合時輸入的認證(`Organization ID`， `Client ID`、和 `Client Secret` 值)。
