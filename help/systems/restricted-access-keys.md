---
title: 管理Commerce中受限制的存取金鑰
description: 建立、指派及刪除受限制的存取金鑰，用以保護同步至Adobe Commerce Optimizer的B2B共用目錄檢視。
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
last-update: 2026-10-01
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
  - id: 601e4abe-d9bf-58de-a779-32ed6794dcbe
    internal-label: Data Import/Export
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%
---

# 管理受限制的存取金鑰

使用[限制存取金鑰]頁面來管理[!DNL Adobe Commerce Optimizer Connector for B2B]所建立之私人目錄檢視的存取金鑰。 聯結器會將B2B共用目錄設定從Adobe Commerce同步至Adobe Commerce Optimizer。

>[!NOTE]
>
>對於在非B2B案例中用來管理私人目錄（例如合作夥伴入口網站）的手動建立金鑰，請從[[!DNL Adobe Commerce Optimizer Studio]](https://experienceleague.adobe.com/zh-hant/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"}管理金鑰。

## 對象與可用性 {#audience}

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端基礎結構上的Adobe Commerce和內部部署專案。"}

使用B2B共用目錄與[!DNL Adobe Commerce Optimizer Connector for B2B]的Adobe Commerce on Cloud Infrastructure和內部部署商家可以使用[!UICONTROL Restricted Access Keys]頁面。 聯結器會自動安裝和啟用頁面。

第一次為共用目錄建立目錄檢視時，聯結器會自動產生並指定一個鍵。 您可以在此頁面檢視該金鑰，以及建立、指派或刪除其他金鑰。

## 存取「限制的存取金鑰」頁面 {#access-restricted-access-keys-page}

從管理區域，瀏覽至&#x200B;**[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**。

![限制存取金鑰頁面列出金鑰及其指派的目錄檢視](assets/restricted-access-keys.png){width="600" zoomable="yes"}

此頁面會列出每個索引鍵，無論其是否已指派給目錄檢視。 若要將索引鍵指派給特定目錄檢視，請改用該目錄檢視上的[!UICONTROL Edit Restricted Access Keys]動作。 請參閱[將金鑰指派給目錄檢視](#assign-keys-to-a-catalog-view)。

## 受限制的存取金鑰摘要 {#restricted-access-keys-summary}

格線每列包含一個索引鍵。

| 欄位 | 說明 |
| --- | --- |
| **金鑰識別碼** | 唯一金鑰識別碼。 |
| **標題** | 您為識別金鑰而提供的標籤。 |
| **指派的目錄檢視** | 此金鑰目前指派的目錄檢視。 |
| **於**&#x200B;到期 | 金鑰到期日。 |
| **動作** | 列層級動作。 請參閱[管理金鑰](#manage-keys)。 |

## 管理金鑰 {#manage-keys}

- **[!UICONTROL Create Key]** — 產生新的未指派金鑰組。 Commerce會產生金鑰組並儲存私密金鑰。 公開金鑰並未向[!DNL Adobe Commerce Optimizer]註冊，直到您將金鑰指派給目錄檢視為止。
- **[!UICONTROL View Public Key]** — 開啟金鑰之公開金鑰的唯讀檢視，以便視需要複製該金鑰以重新註冊或重新同步處理金鑰。 私密金鑰永遠不會顯示。
- **[!UICONTROL Delete]** — 移除金鑰並撤銷其在[!DNL Adobe Commerce Optimizer]中的遠端註冊。 已使用此金鑰核發的店面權杖在到期前都會保持有效。 此動作無法復原。

>[!NOTE]
>
>只能刪除過期的金鑰。 您無法指派或取消指派過期的金鑰。

## 建立金鑰

在[!UICONTROL Restricted Access Keys]頁面上，選取&#x200B;**[!UICONTROL Create Key]**&#x200B;以建立金鑰。

Commerce會產生新的金鑰組並儲存私密金鑰。 「限制存取金鑰」表格會更新為顯示唯一金鑰ID的新金鑰專案。 將金鑰指派給目錄檢視時，請使用此[!UICONTROL Key ID]。

公開金鑰並未向[!DNL Adobe Commerce Optimizer]註冊，直到您將金鑰指派給目錄檢視為止。 註冊之後，會更新「限制存取金鑰」表格專案，以顯示目錄指派和到期日。

## 指派或移除受限制的存取金鑰 {#assign-keys-to-a-catalog-view}

{{$include /help/_includes/edit-restricted-access-keys.md}}

## 鍵選取和旋轉 {#key-selection-and-rotation}

將多個金鑰指派給目錄檢視時，[!DNL Adobe Commerce]會自動使用指派的未過期金鑰（具有最晚到期日）來簽署權杖。

>[!IMPORTANT]
>
>尚未提供自動金鑰輪換功能。 金鑰預設為較長的到期期間。 若要手動旋轉索引鍵，請建立新的索引鍵，並將其與現有索引鍵一起指派給目錄檢視。 確認新金鑰已被使用後，請刪除舊金鑰。

若要變更套用至新建立金鑰的預設到期期間，請移至&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Restricted Access Keys]** > **[!UICONTROL Provisioning]** > **[!UICONTROL Default key lifetime (days)]**。 請參閱[服務> ACO限制存取金鑰](../configuration-reference/services/aco-restricted-access-keys.md)。

## 已知限制 {#known-limitations}

- 主要[!UICONTROL Restricted Access Keys]格線上沒有作用中或狀態指標。

  您可以在[!UICONTROL Edit Restricted Access Keys]頁面上看到連結狀態。 使用下拉式清單來檢視可用的金鑰及其狀態。 如果將索引鍵指派給目錄檢視，則會連結該索引鍵。 如果未指派，則沒有狀態。 您可以將這些索引鍵指派給正在編輯的目錄檢視。

  在[!UICONTROL Catalog View Sync Status]頁面中，您可以從目錄檢視詳細資料頁面（**[!UICONTROL View details]**&#x200B;動作）看到連結至目錄檢視的金鑰。 詳細資訊頁面也會顯示關鍵歷史記錄，包括從目錄檢視中指派或取消指派關鍵歷史記錄的時間。

- 尚未提供自動金鑰輪換功能。

>[!MORELIKETHIS]
>
> - [管理目錄檢視組態](/help/b2b/catalog-views-manage.md) — 從共用目錄或公司帳戶指派這些金鑰
> - [目錄檢視同步狀態監視](catalog-view-sync-status.md) — 監視並調解這些金鑰保護的目錄檢視
> - [服務> ACO限制存取金鑰](../configuration-reference/services/aco-restricted-access-keys.md) — 設定預設金鑰有效期
> - [服務> ACO目錄檢視](../configuration-reference/services/aco-catalog-view.md) — 設定店面存取權杖存留期，並啟用或停用發佈
> - [在&#x200B;*Adobe Commerce Optimizer Connector指南*&#x200B;中管理受限制的存取金鑰](https://experienceleague.adobe.com/zh-hant/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"} — 瞭解這些金鑰如何融入B2B共用目錄同步
> - *Adobe Commerce Optimizer指南*&#x200B;中的[受限制的存取金鑰](https://experienceleague.adobe.com/zh-hant/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} — 非B2B使用案例的手動的ACO Studio金鑰流程
