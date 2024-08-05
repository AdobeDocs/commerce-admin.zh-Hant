---
title: Adobe Commerce的HIPAA整備程度
description: 了解如何新增 Adobe Commerce HIPAA-Ready 擴充功能並取得其他特性和功能，讓您可以遵守 HIPAA 義務。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: bce0e581e89139875e09b671038a21976eccebca
workflow-type: tm+mt
source-wordcount: '1568'
ht-degree: 1%

---

# Adobe Systems商務的 HIPAA 準備就緒

>[!IMPORTANT]
>
>**法律聲明**<br/>
>此資訊旨在説明Adobe Systems客戶回答有關 Adobe Systems 的 HIPAA 就緒服務的問題。 它不構成法律建議。 商家應諮詢自己的法律顧問，以了解他們在 HIPAA 下的義務以及Adobe Systems產品的適當使用和配置。

>[!BEGINSHADEBOX]

**健康保險流通與責任法案 （HIPAA）**

健康保險便利與責任法案(HIPAA)是美國重要的聯邦醫療保健隱私法，由美國衛生與公眾服務部(HHS)執行。 HIPAA適用於&#x200B;_涵蓋的實體_ （例如醫療服務提供者、保險公司和結算所）和&#x200B;_商業夥伴_ （例如為涵蓋的實體提供服務的實體）。 HIPAA要求是在三個不同的規則中設定：隱私權規則、安全性規則和違規通知規則。 Adobe會作為某些產品的Business Associate，而Adobe會將之分類為「HIPAA就緒服務」。 受HIPAA規範管理的資料稱為&#x200B;_受保護的健康資訊_&#x200B;或PHI。 PHI為健康資訊的子集，其中(1)由健康資訊提供者、健康計畫或健康資訊中心建立或接收，(2)關於個人過去、現在或未來的身體或精神健康或狀況，關於向個人提供健康資訊或向個人提供健康資訊的過去、現在或未來付款，以及(3)識別個人或有合理依據相信資訊可用於識別個人的相關資訊。 HIPAA隱私和安全規則要求受保實體以商業夥伴協定或BAA的形式從商業夥伴獲得書面保證，要求商業夥伴保護受保實體PHI的隱私和安全。 如需詳細資訊，請參閱Adobe信任中心中的[HIPAA與Adobe產品及服務](https://www.adobe.com/trust/compliance/hipaa-ready.html)。

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA就緒

Adobe Commerce HIPAA就緒擴充功能為Adobe Commerce安裝新增了其他功能，讓商家可遵守各自的HIPAA義務。

Adobe Commerce HIPAA就緒擴充功能`magento/hipaa-ee`可用於雲端基礎結構上的Adobe Commerce或AdobeManaged Services專案。 Adobe Commerce HIPAA就緒安裝程式會停用某些原生服務和功能以符合HIPAA要求。 請參閱[已停用的服務和功能](#disabled-services-and-features)。

>[!NOTE]
>
>只有購買了 Adobe Systems Commerce 醫療保健附加元件的商家才能訪問 HIPAA 就緒的特性和功能。

*這些材料僅供參考。 提供此資訊並不賦予收件者任何合同或其他權利。 雖然已努力確保資料在提供之日的準確性，但並未表示資料準確且完整。 根據法律或Adobe的產品變更，Adobe不承擔更新此資訊的義務。 此外，未經Adobe書面同意，不得將此檔案分發給預定收件者以外的任何一方。*

## 系統需求

Adobe Commerce必須部署在雲端基礎結構上的Adobe Commerce上，或部署在2.4.6-p3或更新版本的Adobe Commerce Managed Services （無測試版）上。

## 安裝

**先決條件**

>[!BEGINSHADEBOX]

- Adobe Systems已為您Adobe Systems商務帳戶提供存取 HIPAA Ready 擴充功能。
- 存取 [repo.magento.com](https://repo.magento.com) 以安裝擴充功能。 有關金鑰生成和獲取必要許可權的資訊，請參閱 [獲取身份驗證金鑰](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)。

>[!ENDSHADEBOX]

在運行 Commerce 版本 2.4.6-p3 或更高版本的執行個體上安裝最新版本Adobe Systems的 HIPAA 就緒服務擴展 （`magento/hipaa-ee`Adobe Systems。 該擴充功能是以撰寫器元包的形式從 repo.magento.com](https://repo.magento.com) 存放庫提供[。元包包括為Adobe Systems商務執行個體啟用 HIPAA 功能的模組集合。

1. 在本地工作站上，更改為Adobe Systems商務對雲端基礎結構專案的項目目錄。

   >[!NOTE]
   >
   >有關在本地管理 Commerce 專案環境的信息，請參閱[Adobe Systems雲基礎結構上的商務使用手冊&#x200B;_中使用_ CLI](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) 管理分支。

1. 簽出環境 分支以使用 Adobe Commerce Cloud CLI 進行更新。

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. 使用撰寫器 CLI 將元包 `magento/hipaa-ee` 添加到撰寫器配置。

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. 更新包依賴項。

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. 新增、提交更新后的代碼，並將其推送到雲端 環境。

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   推送更新會啟動[Commerce雲端部署程式](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process)以套用變更。 從[部署記錄](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log)檢查部署狀態。

### 驗證安裝

部署更新後，請確認已安裝`Hipaa*`擴充功能

1. 使用SSH登入遠端雲端環境。

   ```shell
   magento-cloud ssh
   ```

1. 從命令列，使用Adobe Commerce CLI來檢查模組狀態。

   ```shell
   bin/magento module:status
   ```

1. 確認HIPAA模組包含在啟用的模組清單中：

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   <truncated for brevity>
   ```

   前綴為前綴 `Magento_Hipaa` 的所有模組都必須位於「啟用的模組」部分中。

## 針對 HIPAA 就緒性的功能增強

此 `magento/hipaa-ee` 擴充功能對 Commerce 基礎產品進行了一些變更和增強功能。 以下各節提供有關這些更改以及它們如何更改基本產品的詳細資訊。

### 動作記錄

審核日誌記錄是 HIPAA 要求。 在 Adobe Systems Commerce 中， [「動作記錄」](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 功能會記錄在您的商店中工作的管理員用戶所做的每項變更。 為了滿足審核日誌的 HIPAA 要求，該功能已更新為記錄通過管理員UI和 API 調用執行的所有管理員用戶和客戶操作。

#### 動作記錄報表

“ _操作日誌_ ”報告網格（**[!UICONTROL System]** >“操作日誌”>報告）已修改，以適應通過管理UI和 API 執行客戶操作。

1. 新增兩欄：
   - ***來源***：顯示執行操作的位置。值： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***使用者端型別***：顯示使用者端型別。
值：客戶 | 管理員 | 整合

2. 將&#x200B;***使用者名稱***&#x200B;欄重新命名為&#x200B;***使用者端識別碼***
   - ***使用者端識別碼***：顯示執行動作之使用者的登入識別碼。
值：
      - 如果「使用者端型別」為「客戶」，則傳送電子郵件
      - 如果「使用者端型別」為「管理員」，則為使用者名稱
      - 如果「使用者端型別」為「整合」，則使用名稱

3. 已將&#x200B;***完整動作名稱***&#x200B;資料行重新命名為&#x200B;***目標***
   - ***目標***：顯示動作名稱。
值：
      - 如果Source是REST API或SOAP API，則為端點
      - 查詢或突變名稱（如果是 GraphQL API）
      - 操作名稱（如果管理員UI或客戶UI。

#### 設定記錄的管理員動作

此功能不可用，因為預設情況下必須記錄所有操作。

### 匯入和導出要素

匯入和匯出功能的增強功能著重於改善管理體驗並提供使用者動作的更佳可見度。

>[!NOTE]
>
>這&#x200B;***項增強功能不會改變匯入和匯出核心邏輯***，而是擴充功能以提供更完整的記錄並改善資料歸因。 匯入和匯出的基本功能保持不變。 使用者可以繼續使用現有功能和工作流程，不會造成任何中斷。

#### 管理動作記錄

匯入和匯出功能的重要改善之一，是增強了管理動作的記錄功能。 此增強功能引入了深入研究與數據導入和導出關聯的活動的功能，有助於改進跟蹤和可審核性。 下列動作現已記錄並反映在「**[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**」格線中：

| 型別 | 動作 |
| ---- | ------- |
| 進口 | <ul><li>由管理員用戶執行匯入<li>管理員用戶下載匯入的檔案<li>管理員使用者下載錯誤檔案<ul/> |
| 匯出 | <ul><li>管理員使用者請求<li>管理員使用者下載匯出的檔案<ul/> |
| 排程的匯入/匯出 | <ul><li>管理員使用者排程匯出<li>管理員用戶編輯計劃的導出<li>管理員用戶執行計劃的導出<li>管理員用戶刪除已排程的匯出<li>管理員用戶排程匯入<li>管理員使用者編輯已排程的匯入<li>管理員用戶執行計劃的匯入<li>管理員使用者會刪除排程的匯入<li>管理員使用者會執行匯入/匯出操作的大量刪除<ul/> |

### 顯示改進和改進的篩選和排序

為了向管理員使用者提供更多資訊的網格，HIPAA-Ready 服務提供了多項增強功能來顯示、篩選和排序數據。

#### 匯入歷史 （[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History]）

- 已針對&#x200B;**[!UICONTROL Imported File]**、**[!UICONTROL Error File]**、**[!UICONTROL Execution Time]**&#x200B;和&#x200B;**[!UICONTROL Summary]**&#x200B;以外的所有資料行啟用篩選。

#### 匯出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- 已新增&#x200B;**[!UICONTROL ID]**&#x200B;欄。
- 已新增&#x200B;**[!UICONTROL Requested At]**&#x200B;欄（_要求匯出的日期和時間_）。
- 新增&#x200B;**[!UICONTROL User]**&#x200B;欄（_執行要求的管理員使用者名稱_）。
- 刪除了一 **[!UICONTROL Action]** 欄。
- 已將 **[!UICONTROL Download]** 連結移至欄 **[!UICONTROL File name]** （_按讚匯入歷史記錄」網格_&#x200B;線）。
- 已停用負責刪除匯出檔案的操作 （_以改善追蹤_）。
- 啟用除 以外的 **[!UICONTROL File name]**&#x200B;所有欄的排序。
- 啟用所有欄的篩選。

#### 預定匯入與匯出 （[!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export]）

- 新增了欄 **[!UICONTROL ID]** 目。
- 新增欄 **[!UICONTROL Scheduled At]** （ _排程_&#x200B;匯入或導出的日期和時間）。
- 新增欄 **[!UICONTROL User]** （排 _程匯入或匯出_&#x200B;的管理員用戶的用戶名稱）。

## 殘疾人服務和功能

為了符合 HIPAA 要求，Adobe Systems Commerce 支援的某些服務和功能在預設情況下不可用或禁用。 商家可以選擇重新啟用或使用這些服務和功能，風險自負。

### 服務

- **Adobe Commerce服務**—HIPAA整備服務不提供Adobe Commerce服務或擴充性服務。 這些服務包括但不限於：

   - 即時搜尋
   - API網格
   - App Builder

- **[SendGrid服務](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** — 此服務預設為停用，因為應用程式不符合HIPAA規範。

### 預設為停用的功能

HIPAA整備模組預設會停用下列功能。 商家可以自行承擔啟用任何這些功能的風險。

- **[訪客簽出](../stores-purchase/checkout-guest.md)** — 此功能對HIPAA的各個方面帶來潛在風險，包括記錄、存取控制、PHI衛生和歷程等等。

- **[電子報功能](../merchandising-promotions/newsletters.md)** — 此功能已停用，以防止行銷內容使用PHI。

- **[進階報告服務設置](../getting-started/business-intelligence.md)**— — 禁用此配置設置以防止 PHI 用於分析和報告。
