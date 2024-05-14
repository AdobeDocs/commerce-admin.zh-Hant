---
title: Adobe Commerce的HIPAA整備程度
description: 瞭解如何新增Adobe Commerce HIPAA就緒模組，並取得可讓您遵守HIPAA義務的其他功能。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 7e132d66523feba579baf0bae14e1de9de4d6591
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 0%

---

# Adobe Commerce的HIPAA整備程度

>[!IMPORTANT]
>
>**法律宣告**<br/>
>此資訊旨在協助Adobe客戶回答他們有關Adobe HIPAA就緒服務的問題。 這不構成法律建議。 商家應該諮詢自己的法律顧問，瞭解他們在HIPAA下的義務，以及Adobe產品的適當使用和設定。

>[!BEGINSHADEBOX]

**健康保險便利與責任法案(HIPAA)**

健康保險便利與責任法案(HIPAA)是美國重要的聯邦醫療保健隱私法，由美國衛生與公眾服務部(HHS)執行。 HIPAA套用至 _涵蓋的實體_ （例如醫療服務提供者、保險公司及結算所）與 _Business Associates_ （例如為適用實體提供服務的實體）。 HIPAA要求是在三個不同的規則中設定：隱私權規則、安全性規則和違規通知規則。 Adobe會作為某些產品的Business Associate，而Adobe會將之分類為「HIPAA就緒服務」。 受HIPAA管制的資料稱為 _受保護的健康資訊_ 或PHI。 PHI為健康資訊的子集，其中(1)由健康資訊提供者、健康計畫或健康資訊中心建立或接收，(2)關於個人過去、現在或未來的身體或精神健康或狀況，關於向個人提供健康資訊或向個人提供健康資訊的過去、現在或未來付款，以及(3)識別個人或有合理依據相信資訊可用於識別個人的相關資訊。 HIPAA隱私和安全規則要求受保實體以商業夥伴協定或BAA的形式從商業夥伴獲得書面保證，要求商業夥伴保護受保實體PHI的隱私和安全。 如需詳細資訊，請參閱 [HIPAA與Adobe產品和服務](https://www.adobe.com/trust/compliance/hipaa-ready.html) 在Adobe信任中心。

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA就緒

Adobe Commerce HIPAA-Ready具有附加功能，可讓商家遵守其各自的HIPAA義務。

Adobe Commerce HIPAA就緒會以Adobe Commerce擴充功能的形式提供， `magento/hipaa-ee` 這可用於Adobe Commerce的雲端基礎結構或AdobeManaged Services專案。 Adobe Commerce HIPAA就緒安裝程式會停用某些原生服務和功能以符合HIPAA要求。 另請參閱 [停用的服務和功能](#disabled-services-and-features).

*這些資料僅供參考。 提供此資訊不會賦予收件者任何合約權利或其他權利。 雖然已努力確保資料在提供之日的準確性，但並未表示資料準確且完整。 根據法律或Adobe的產品變更，Adobe不承擔更新此資訊的義務。 此外，未經Adobe書面同意，不得將此檔案散發給預定收件者以外的任何一方。*

## 系統需求

Adobe Commerce必須部署在雲端基礎結構上的Adobe Commerce上，或部署在2.4.6-p3或更新版本的Adobe Commerce Managed Services （無測試版）上。

## 安裝

安裝最新版Adobe的HIPAA就緒服務擴充功能(`magento/hipaa-ee`)在執行Adobe Commerce 2.4.6-p3或更新版本的執行個體上執行。 此擴充功能會以作曲者中繼資料的形式從 [repo.magento.com](https://repo.magento.com) 存放庫。

>[!BEGINSHADEBOX]

**先決條件**

您必須有權存取 [repo.magento.com](https://repo.magento.com) 以安裝擴充功能。 如需金鑰產生與取得必要許可權的相關資訊，請參閱 [取得您的驗證金鑰](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

1. 在本機工作站上，變更至雲端基礎結構專案上Adobe Commerce的專案目錄。

   >[!NOTE]
   >
   >如需有關在本機管理Commerce專案環境的資訊，請參閱  [使用CLI管理分支](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) 在 _雲端基礎結構上的Adobe Commerce使用手冊_.

1. 簽出環境分支以使用Adobe Commerce Cloud CLI更新。

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. 新增中繼資料 `magento/hipaa-ee` 至使用撰寫器CLI的撰寫器設定。

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. 更新套件相依性。

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. 新增、提交更新後的程式碼並將其推播至雲端環境。

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   推送更新會啟動 [Commerce雲端部署程式](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) 以套用變更。 從檢視部署狀態 [部署記錄](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### 驗證安裝

部署更新後，請確認 `Hipaa*` 已安裝擴充功能

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

   所有首碼為 `Magento_Hipaa` 必須在「啟用的模組」區段中。

## HIPAA整備的增強功能

此 `magento/hipaa-ee` 此套件引進了基礎Commerce產品的一些變更和增強功能。 以下各節提供這些變更的詳細資訊，以及變更基礎產品的方式。

### 動作記錄檔

稽核記錄是HIPAA的要求。 在Adobe Commerce中 [動作記錄檔](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 功能會記錄管理員使用者在您的商店中所做的每項變更。 為了滿足稽核記錄的HIPAA要求，功能已更新，以記錄所有透過管理員UI和API呼叫執行的管理員使用者和客戶動作。

#### 動作記錄報告

此 _動作記錄檔_ 報表格線(**[!UICONTROL System]** >動作記錄>報表)已修改，以容納透過管理員UI和API執行的客戶動作。

1. 新增兩欄：
   - ***來源***：顯示動作的執行位置。
值： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***使用者端型別***：顯示使用者端型別。
值：客戶 | 管理員 | 整合

2. 已重新命名 ***使用者名稱*** 欄至 ***使用者端識別碼***
   - ***使用者端識別碼***：顯示執行動作之使用者的登入ID。
值：
      - 如果「使用者端型別」為「客戶」，則傳送電子郵件
      - 如果「使用者端型別」為「管理員」，則為使用者名稱
      - 如果「使用者端型別」為「整合」，則使用名稱

3. 已重新命名 ***完整動作名稱*** 欄至 ***Target***
   - ***Target***：顯示動作名稱。
值：
      - 如果來源是REST API或SOAP API，則為端點
      - 查詢或變異名稱(若為GraphQL API)
      - 是管理員UI或客戶UI時的動作名稱。

#### 設定管理員記錄動作

此功能無法使用，因為預設必須記錄所有動作。

### 匯入和匯出特徵

匯入和匯出功能的增強功能著重於改善管理體驗並提供使用者動作的更佳可見度。

>[!NOTE]
>
>這些 ***增強功能不會改變匯入和匯出核心邏輯***；它們會擴充功能，提供更完整的記錄並改善資料歸因。 匯入和匯出的基本功能保持不變。 使用者可以繼續使用現有功能和工作流程，不會造成任何中斷。

#### 管理動作記錄

匯入和匯出功能的重要改善之一，是增強了管理動作的記錄功能。 此增強功能引進更深入探究與資料匯入和匯出相關的活動的能力，有助於改善追蹤和稽核能力。 下列動作現在會記錄並反映在 **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**格線：

| 型別 | 動作 |
| ---- | ------- |
| 匯入 | <ul><li>管理員使用者執行匯入<li>管理員使用者下載匯入的檔案<li>管理員使用者下載錯誤檔案<ul/> |
| 匯出 | <ul><li>管理員使用者請求<li>管理員使用者下載匯出的檔案<ul/> |
| 排程的匯入/匯出 | <ul><li>管理員使用者排程匯出<li>管理員使用者編輯已排程的匯出<li>管理員使用者執行排定的匯出<li>管理員使用者會刪除排程的匯出<li>管理員使用者排程匯入<li>管理員使用者編輯已排程的匯入<li>管理員使用者執行排定的匯入<li>管理員使用者會刪除排程的匯入<li>管理員使用者會執行匯入/匯出操作的大量刪除<ul/> |

### 顯示增強功能及改善的篩選和排序

為讓管理員使用者擁有更多資訊網格，HIPAA就緒服務提供數個增強功能，用於顯示、篩選和排序資料。

#### 匯入歷史記錄([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- 啟用所有欄的篩選功能，但 **[!UICONTROL Imported File]**， **[!UICONTROL Error File]**， **[!UICONTROL Execution Time]**、和 **[!UICONTROL Summary]**.

#### 匯出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- 已新增 **[!UICONTROL ID]** 欄。
- 已新增 **[!UICONTROL Requested At]** 欄(_要求匯出的日期與時間_)。
- 已新增 **[!UICONTROL User]** 欄(_提出要求的管理員使用者名稱_)。
- 已移除 **[!UICONTROL Action]** 欄。
- 已移動 **[!UICONTROL Download]** 連結至 **[!UICONTROL File name]** 欄(_如同「匯入歷史記錄」格線_)。
- 已停用負責刪除匯出檔案的動作(_改善追蹤_)。
- 已針對除外的所有欄啟用排序 **[!UICONTROL File name]**.
- 已針對所有欄啟用篩選功能。

#### 已排程的匯入和匯出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- 已新增 **[!UICONTROL ID]** 欄。
- 已新增 **[!UICONTROL Scheduled At]** 欄( _排程匯入或匯出的日期與時間_)。
- 已新增 **[!UICONTROL User]** 欄( _排程匯入或匯出的管理員使用者名稱_)。

## 停用的服務和功能

為符合HIPAA要求，Adobe Commerce支援的部分服務和功能可能不提供或預設為停用。 商家可以選擇重新啟用或使用這些服務和功能，但需自行承擔風險。

### 服務

- **Adobe Commerce服務**—HIPAA整備服務不提供Adobe Commerce服務或擴充性服務。 這些服務包括但不限於：

   - 即時搜尋
   - API網格
   - App Builder
   - 目錄服務

- **[SendGrid服務](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** — 此服務預設為停用，因為應用程式不符合HIPAA標準。 商家可以提交支援要求來啟用Sendgrid，但是他們必須確認他們承擔使用此服務的風險。

### 功能預設為停用

下列功能在HIPAA整備模組中預設為停用。 商家可以自行承擔啟用任何這些功能的風險。

- **[訪客簽出](../stores-purchase/checkout-guest.md)** — 此功能對HIPAA的各個方面帶來潛在風險，包括記錄、存取控制、PHI衛生和譜系等等。

- **[Newsletter功能](../merchandising-promotions/newsletters.md)** — 此功能已停用，以防止在行銷內容中使用PHI。

- **[進階報告服務設定](../getting-started/business-intelligence.md)** — 此組態設定已停用，以防止將PHI用於分析和報告。
