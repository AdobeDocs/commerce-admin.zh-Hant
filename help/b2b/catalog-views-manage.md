---
title: 管理目錄檢視設定
description: 瞭解如何檢閱為B2B共用目錄建立的Adobe Commerce Optimizer目錄檢視，並指派可保護它們的受限制存取金鑰。
feature: B2B, Companies, Catalog Management
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: f9f21f675d5c608547db790f33d1aa9be90a36eb
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%
---
# 管理目錄檢視設定

安裝[!DNL Adobe Commerce Optimizer Connector for B2B]擴充功能後，[目錄檢視]頁面會列出為自訂共用目錄建立的[!DNL Adobe Commerce Optimizer] [目錄檢視投影](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}。  _投影_&#x200B;是聯結器將共用目錄資料同步到[!DNL Adobe Commerce Optimizer]時建立的目錄檢視。 聯結器會為共用目錄中的每個存放區檢視建立個別的投影，因此共用目錄可以有多個目錄檢視。 在店面體驗中，這些目錄檢視僅供指派給相關共用目錄的公司存取。

例如，假設Acme Industrial已指派給一個共用目錄EU Business，它屬於EU網站。 該網站有兩個商店檢視：

- `English (UK)`

- `German (Germany)`

聯結器將共用目錄專案為兩個[!DNL Adobe Commerce Optimizer]目錄檢視：

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

公司有英文和德文目錄檢視，但只有一個共用目錄指派。 每個存放區檢視都會顯示其對應目錄檢視中的資料。

當兩個目錄檢視使用相同的網站和客戶群組定價範圍時，它們可以共用相同的價格簿。

## 目錄檢視驗證

聯結器會使用受限制的存取金鑰保護目錄檢視。 Adobe Commerce會使用私密金鑰，為授權購買者簽署存取權杖。 在傳回受保護的目錄資料之前，[!DNL Adobe Commerce Optimizer]會針對與要求的目錄檢視相關聯的對應公開金鑰來驗證權杖。

若要設定權杖存留期或停用權杖發行，請參閱[服務> ACO目錄檢視](/help/configuration-reference/services/aco-catalog-view.md)。

您可以檢閱這些目錄檢視，並從共用目錄的&#x200B;_[!UICONTROL Catalog Views]_標籤或關聯公司的_[!UICONTROL Catalog Views]_&#x200B;區段管理其指派的金鑰，兩者都會列出相同的目錄檢視和目前的金鑰指派。 請參閱[編輯受限制的存取金鑰](#edit-restricted-access-keys)，以取得每個位置的確切導覽路徑。

若要監視與[!DNL Adobe Commerce Optimizer]的共用目錄資料同步處理，請參閱[目錄檢視同步處理狀態監視](/help/systems/catalog-view-sync-status.md)。

## 目錄檢視參考

{{$include /help/_includes/catalog-views-reference-table.md}}

## 編輯受限制的存取金鑰

{{$include /help/_includes/edit-restricted-access-keys.md}}

如需其他詳細資料，請參閱[管理受限制的存取金鑰](/help/systems/restricted-access-keys.md)。

>[!MORELIKETHIS]
>
> - [B2B共用目錄投影](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}
> - [服務> ACO目錄檢視](/help/configuration-reference/services/aco-catalog-view.md)
> - [目錄檢視同步處理狀態監視](/help/systems/catalog-view-sync-status.md)
> - [管理您的共用目錄](catalog-shared-manage.md)
> - [管理公司帳戶](account-company-manage.md)
