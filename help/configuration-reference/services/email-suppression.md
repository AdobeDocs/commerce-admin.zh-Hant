---
title: '[!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]'
description: 檢閱Commerce管理員的[!UICONTROL Adobe Services] &gt； [!UICONTROL Email Suppression]頁面上的組態設定。
feature: Configuration, Communications
badgeSaas: label="僅限SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於Adobe Commerce as a Cloud Service和Adobe Commerce Optimizer專案（Adobe管理的SaaS基礎結構）。"
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f4d7033067a99421224ab2159b1b95775e5e949f
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]

{{config}}

[!UICONTROL Email Suppression]可讓系統管理員關閉特定類別的自動化系統電子郵件，而不會影響商店的其餘電子郵件，或需要開發人員參與。 使用此功能暫時或永久停止特定通知，例如，在資料移轉期間訂購電子郵件，或行銷電子郵件。

>[!IMPORTANT]
>
>此功能絕不會抑制與安全性相關的管理員通知，例如雙因素驗證代碼和管理員密碼重設電子郵件。

此頁面上的設定會套用至[商店檢視](../../getting-started/websites-stores-views.md#scope-settings)，因此您可以隱藏不同商店門面的不同電子郵件類別。

>[!NOTE]
>
>關閉隱藏會立即恢復正常的電子郵件傳送，但是在隱藏期間傳送的電子郵件不會排入佇列。

## [!UICONTROL Email Suppression]

![電子郵件隱藏](./assets/email-suppression.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Email Suppression] | 存放區檢視 | 功能的主開啟/關閉開關。 設為`No` （預設）時，會忽略此頁面上的其他所有設定，所有電子郵件都會正常傳送。 |
| [!UICONTROL Disabled Functional Areas] | 存放區檢視 | 選取已隱藏其電子郵件的一或多個業務類別。 檢視[企業類別](#business-categories)，瞭解每個類別包含哪些內容。 |
| [!UICONTROL Disabled Template IDs] | 存放區檢視 | 選用的以逗號分隔的特定電子郵件範本清單，可個別隱藏（無論類別為何）。 使用範本代碼（例如，`customer_password_forgot_email_template`）或您在Admin中建立的自訂範本數值範本ID。 |

{style="table-layout:auto"}

### 業務類別 {#business-categories}

| 類別 | 包含的一般電子郵件 |
|--- |--- |
| 客戶帳戶 | 帳戶建立、密碼重設、帳戶資訊變更。 |
| Order Management | 訂單確認、商業發票、出貨、銷退折讓單、訂單取消。 |
| 退貨(RMA) | 退貨商品授權通知。 |
| 結帳與付款 | 結帳和透過連結付費的相關電子郵件。 |
| 行銷 | 電子報、產品通知、希望清單分享、傳送電子郵件給朋友、提醒、邀請、贈品登入。 |
| 商店點數與獎勵 | 禮品卡、獎勵積分、商店信用餘額變更。 |
| B2B | 公司、可轉讓報價單及採購單通知。 |
| 系統通知 | 作業通知，例如，排程的匯入、匯出和連絡人表單電子郵件。 |

{style="table-layout:auto"}
