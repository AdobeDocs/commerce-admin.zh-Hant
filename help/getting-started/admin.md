---
title: 管理員是什麼？
description: 瞭解 [!DNL Commerce] 管理員，商家可在此設定產品和促銷活動、管理訂單及執行其他管理任務。
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 管理員是什麼？

您的商店 _管理員_ 是受密碼保護的後台，身為商家，您可以在此設定產品和促銷活動、管理訂單及執行其他管理任務。 所有基本設定任務和存放區管理作業都是從 _管理員_.

如需額外安全性， _管理員_ 登入受到保護 [雙因素驗證](../systems/security-two-factor-authentication.md)、和，可設定為需要 [驗證碼](../systems/security-captcha.md). 若要進一步瞭解，請前往 [設定管理員安全性](../systems/security-admin.md).

![管理員側邊欄和控制面板](./assets/admin-dashboard.png){width="700" zoomable="yes"}

您的初始 [登入](admin-signin.md) 憑證是在Adobe Commerce或Magento Open Source安裝期間設定的。 如果您忘記密碼，則會將暫時密碼傳送至與帳戶關聯的電子郵件地址。 若要提高安全性，請將存放區設定為需要區分大小寫的使用者名稱和增強式密碼。

除了預設的Admin使用者帳戶外，您的企業可以建立儘可能多的帳戶 [其他帳戶](../systems/permissions-users-all.md) 您管理商店及支援客戶帳戶所需的相關資訊。 每個帳戶都可以與特定的 [角色](../systems/permissions-user-roles.md) 和存取層級（根據業務） _需要知道_. 與每個管理員使用者帳戶相關聯的電子郵件地址必須是唯一的。

{{ims-admin-note}}

## 使用資料集合

第一次登入 _管理員_，系統會要求您授予Adobe許可權，以便收集所有管理員使用者的使用情況資料。 透過允許管理員使用資料收集，您可以協助Adobe改善使用Adobe Commerce管理員及相關產品和服務的體驗。

![允許管理員使用資料收集](./assets/admin-usage-data.png){width="600"}

使用資料中未識別個別使用者。 您的資料收集設定可隨時變更，從 [管理員使用情況](../configuration-reference/advanced/admin.md#admin-usage) 設定。

對於Adobe Commerce，允許資料收集也會啟用 _產品內指引_，可將互動式內容帶至 _管理員_. 提供說明、工具提示、逐步指南、入門資訊、功能公告等。
