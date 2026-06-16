---
title: 管理員許可權
description: 瞭解管理員使用者帳戶以及如何使用角色來授予存放區管理功能的存取權。
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
TQID: https://experienceleague.adobe.com/7xyouYohAbOKbwVCxZPamD-7gEiqGrqEAAg9FDm8z-U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# 管理員許可權

Adobe Commerce和Magento Open Source使用角色和許可權，建立管理員的不同存取層級。 第一次設定存放區時，您會收到具有完整許可權之管理員角色的一組登入認證。 不過，您可以根據在您網站上工作的其他人的「須知」來限制許可權等級。 例如，設計團隊的成員只能存取內容設計工具，而不能存取具有客戶和訂單資訊的區域。

此外，您可以進一步將管理員存取許可權製為僅限特定網站，或一組網站及其相關資料。 如果在同一Commerce安裝中有多個品牌或業務單位擁有不同的商店，您可以提供每個業務單位的管理員存取權，但會隱藏和保護其資料，不讓其他管理員使用者存取。

當管理員使用者的存取許可權制在特定網站或商店時，未獲授權的網站或商店將看不到或顯示為灰色。 系統只會針對使用者顯示所允許網站和商店的銷售和其他資料。

- ![Adobe Commerce](../assets/adobe-logo.svg) （僅限Adobe Commerce）依預設，系統會在使用者將變更套用至存放區時，自動記錄（記錄）其所執行的所有動作。 可在[動作記錄報告](action-log-report.md)中檢閱管理員動作。 在商店的進階管理設定中，設定[管理動作記錄](action-log.md)中的記錄。

![管理員 — 所有使用者帳戶](./assets/users-all.png){width="700" zoomable="yes"}
