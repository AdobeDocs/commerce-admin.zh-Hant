---
title: 共用目錄概觀
description: 瞭解B2B為Adobe Commerce提供的共用目錄，以及如何使用共用目錄，以自訂價格維護不同公司帳戶的閘道目錄。
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# 共用目錄概觀

Adobe Commerce適用的B2B可讓您維持閘道 _已共用_ 不同公司的自訂定價目錄。 除了標準以外， _主要_，產品目錄，它可讓客戶存取具有不同定價結構的兩種共用目錄。

如果 [共用目錄功能](enable-basic-features.md) 在設定中啟用時，原始主要目錄在管理員中仍然可見，但在店面中只能看到「預設（一般）」公用共用目錄。 此外，可建立僅對特定成員可見的自訂目錄 [公司](account-companies.md) 帳戶。

對於 `Default (General)` 公用共用目錄，您必須指派產品以在店面中顯示目錄。 預設為空白，不包含任何產品。

>[!NOTE]
>
>**[B2B版本1.3.0](release-notes.md#b2b-v130) 及更新版本**  — 建立共用目錄時，每一個 [類別許可權](../catalog/category-permissions.md) 目錄的「 」設為 _[!UICONTROL Allow for the Display Product Prices]_和_[!UICONTROL Add to Cart]_ 適用於在目錄許可權設定中指派此存取權的客戶群組。 之前，這些設定會自動設為 `Deny` 即使目錄許可權設定為 `Allow`.

>[!IMPORTANT]
>
>所有現有 [群組許可權設定](../configuration-reference/catalog/catalog.md#category-permissions) 被忽略 **_全部_** 目錄中的類別，當 **_[!UICONTROL Shared Catalog]_** 功能已啟用。 [!UICONTROL Shared Catalog] 完全控制啟用目錄時目錄中的所有類別許可權。

此 _[!UICONTROL Shared Catalogs]_頁面可讓您存取用來管理共用目錄的工具。 此頁面與標準頁面類似 [管理員工作區](../getting-started/admin-workspace.md)，包含篩選器和動作控制項。 網格會列出所有共用目錄，包括預設的公用共用目錄，以及您設定的所有自訂目錄。

![共用目錄](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## 存取 [!UICONTROL Shared Catalogs] 頁面

在 _管理員_ 側欄，前往 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## 動作控制項

此 [動作控制項](../getting-started/admin-actions-control.md) 您可以使用位於左上角的整批動作控制項來刪除不再需要的所選共用目錄。 在格線中， _[!UICONTROL Actions]_欄包含管理共用目錄的完整工具選項。

![共用目錄動作](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| 控制 | 說明 |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | 決定共用目錄中可用的產品選擇和自訂價格。 |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | 決定哪些公司可以存取共用目錄。 |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | 決定型錄明細資訊，包括名稱、型錄型態、客戶稅捐類別及摘要。 |
| [!UICONTROL Delete] | 刪除選取的共用目錄。 |

{style="table-layout:auto"}

## 欄說明

| 標題 | 說明 |
|--- |--- |
| [!UICONTROL Select] | 選取共用目錄記錄以套用動作。 標頭中的控制項可用來選取網格中的所有共用目錄記錄，或取消選取網格中的所有共用目錄記錄。 若要選取個別共用目錄，請選取核取方塊。 |
| [!UICONTROL ID] | 建立目錄時依序指派的唯一數值識別碼。 |
| [!UICONTROL Name] | 共用目錄的名稱。 依預設，可使用預設（一般）共用目錄。 |
| [!UICONTROL Type] | 識別共用目錄型別，如下所示： <br/>**[!UICONTROL Public]**— 安裝Adobe Commerce的B2B時，會自動建立預設的公共共用目錄。 它最初指派給 `General` 和 `Not Logged In` 客戶群組，且在與公司無關聯的來賓和個人登入客戶中可見。 系統一次僅支援一個公用共用目錄。<br/>**[!UICONTROL Custom]**  — 自訂共用目錄包含的定價僅對已指派公司帳戶的登入關聯可見。 您可以視需要建立儘可能多的自訂共用目錄。 |
| [!UICONTROL Customer Tax Class] | 指定給對應客戶群組的稅捐類別。 此欄不會出現在預設格線中，但可以透過變更欄版面配置來新增。 |
| [!UICONTROL Created At] | 建立共用目錄的日期和時間。 |
| [!UICONTROL Created By] | 建立共用目錄之存放區管理員的名字和姓氏。 |
| [!UICONTROL Action] | 列出套用至所選目錄的動作。 選項： `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
