---
title: 停用Commerce與Adobe ID的管理員整合
description: 請依照此選擇性程式來停用Adobe Commerce與Adobe IMS的管理員整合。
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/KL6Cx3ymElo7ROx5SUJtlqtKivnw7-heqPWGksGP-pg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 351
ht-degree: 0%

---

# 停用Commerce與Adobe ID的管理員整合

{{ee-feature}}

已將Commerce執行個體與Adobe IMS驗證工作流程整合的商家，可能需要停用此選擇性整合。

IMS整合停用後，Commerce部署會還原為預設的Commerce驗證工作流程和密碼原則。 啟用或停用此整合時，只會影響管理員使用者工作流程。

如需Commerce管理員登入的概觀，請參閱[您的管理員帳戶](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=zh-Hant)。

## 步驟1：停用整合

您無法從Admin停用這項整合。 若要停用Adobe IMS與Commerce的整合，並將Commerce驗證恢復為預設狀態，您必須從命令列介面停用整合。

若要停用整合：

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce在成功時顯示下列訊息：

```
Admin Adobe IMS integration is disabled.
```

## 步驟2：建立或擷取您的Commerce密碼

停用整合後，管理員使用者必須使用Commerce密碼登入管理員。

* 記得先前已有的Commerce密碼（亦即在IMS整合之前建立的Commerce密碼）的Commerce管理員使用者，可使用此密碼登入管理員。

* 沒有既有Commerce密碼或忘記密碼的Commerce管理員使用者必須建立新密碼。 若要建立新密碼，管理員使用者可以使用Commerce登入頁面上的[!UICONTROL Forgot your password?]功能來建立新密碼。 請參閱[重設客戶密碼](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html?lang=zh-Hant)。 Commerce不接受空白的密碼欄位。

## 停用整合後

IMS整合停用後，預設的Commerce驗證工作流程會繼續，並再次提示管理員使用者輸入密碼。

停用IMS整合將會從Commerce組態檔中刪除啟用整合時輸入的認證（`Organization ID`、`Client ID`和`Client Secret`值）。
