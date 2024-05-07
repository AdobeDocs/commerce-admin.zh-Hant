---
title: Adobe Commerce的HIPAA整備程度
description: 瞭解如何新增Adobe Commerce HIPAA就緒模組，並取得可讓您遵守HIPAA義務的其他功能。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: c21c8b76e37e617885bae3492801b45093a6b5a5
workflow-type: tm+mt
source-wordcount: '1483'
ht-degree: 0%

---

# Adobe Commerce的HIPAA整備程度

>[!IMPORTANT]
>
>**法律宣告**<br/>
>此資訊旨在協助Adobe客戶回答他們有關Adobe HIPAA就緒服務的問題。 這不構成法律建議。 商家應該諮詢自己的法律顧問，瞭解他們在HIPAA下的義務，以及Adobe產品的適當使用和設定。

## 健康保險便利與責任法案(HIPAA)

健康保險便利與責任法案(HIPAA)是美國重要的聯邦醫療保健隱私法，由美國衛生與公眾服務部(HHS)執行。 HIPAA套用至 _涵蓋的實體_ （例如醫療服務提供者、保險公司及結算所）與 _Business Associates_ （例如為適用實體提供服務的實體）。 HIPAA要求是在三個不同的規則中設定：隱私權規則、安全性規則和違規通知規則。 Adobe會作為某些產品的Business Associate，而Adobe會將之分類為「HIPAA就緒服務」。 受HIPAA管制的資料稱為 _受保護的健康資訊_ 或PHI。 PHI為健康資訊的子集，其中(1)由健康資訊提供者、健康計畫或健康資訊中心建立或接收，(2)關於個人過去、現在或未來的身體或精神健康或狀況，關於向個人提供健康資訊或向個人提供健康資訊的過去、現在或未來付款，以及(3)識別個人或有合理依據相信資訊可用於識別個人的相關資訊。 HIPAA隱私和安全規則要求受保實體以商業夥伴協定或BAA的形式從商業夥伴獲得書面保證，要求商業夥伴保護受保實體PHI的隱私和安全。

## Adobe Commerce HIPAA就緒

Adobe Commerce HIPAA-Ready具有附加功能，可讓商家遵守其各自的HIPAA義務。 您可以安裝Adobe Commerce HIPAA就緒(`magento/hipaa-ee`)模組至您的Adobe Commerce on cloud infrastructure。 還有一些功能必須停用以符合HIPAA。

*這些資料僅供參考。 提供此資訊不會賦予收件者任何合約權利或其他權利。 雖然已盡力確保提供之日資訊的正確性，但並未宣告此資訊是準確且完整的，且Adobe不承擔因法律或Adobe產品變更而更新此資訊的義務。 此外，未經Adobe書面同意，不得將此檔案散發給預定收件者以外的任何一方。*

## 系統需求

Adobe Commerce上的HIPAA整備程度具有與Adobe Commerce相同的系統需求，但有下列其他需求：

- Adobe Commerce 2.4.6-p3或更新版本（非測試版）
- 雲端基礎結構上的Adobe Commerce或Managed Services上的Adobe Commerce
- 最新版本的 `magento/hipaa-ee` 副檔名

## 安裝

Adobe的HIPAA就緒服務在技術上是撰寫器中繼套件 `magento/hipaa-ee` 其中包含特殊模組的連結。 此中繼資料位於存放庫中 [repo.magento.com](https://repo.magento.com).

1. 安裝 `magento/hipaa-ee` 中繼封裝，您必須擁有存取權。 如需金鑰產生與取得必要權利的相關資訊，請參閱 [取得您的驗證金鑰](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html?lang=en).

1. 檢查您要安裝套裝軟體的環境，並確定其符合一般需求 [系統需求](#system-requirements).

1. 新增中繼資料 `magento/hipaa-ee` 至撰寫器設定。

   最簡單的方法是使用撰寫器CLI。 例如：

   ```shell
   composer require magento/hipaa-ee
   ```

1. 如果尚未安裝Adobe Commerce，您可以開始安裝(請遵循 [安裝指示](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html?lang=en))。

   如果已安裝Adobe Commerce，則下載模組後，請執行 `bin/magento setup:upgrade` 指令，然後遵循建議。

   ```shell
   bin/magento setup:upgrade
   ```

   執行此命令時，會啟用新下載的模組，並啟動安裝這些模組的指令碼。 若要進一步瞭解模組管理，請參閱 [啟用或停用模組](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html?lang=en).

1. 安裝或更新程式完成後，您應檢查 `Hipaa*` 也包含相關模組。

   執行命令：

   ```shell
   bin/magento module:status
   ```

   如果HIPAA撰寫器套件已正確新增，您會在命令輸出中看到HIPAA模組。 例如：

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

稽核記錄是HIPAA的要求。 在Adobe Commerce中 [動作記錄檔](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 功能會記錄管理員使用者在您的商店中所做的每項變更。 為符合HIPAA對稽核記錄的要求，功能有所變更，可記錄所有透過管理員UI和API呼叫執行的管理員使用者和客戶動作。

#### 動作記錄報告

此 _動作記錄檔_ 報表格線(**[!UICONTROL System]** >動作記錄>報表)已修改，以容納透過管理員UI和API執行的客戶動作。

1. 兩個額外的欄：
   - ***來源***：顯示動作的執行位置。\
     值： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***使用者端型別***：顯示使用者端型別。\
     值：客戶 | 管理員 | 整合


2. 重新命名 ***使用者名稱*** 至 ***使用者端識別碼***
   - ***使用者端識別碼***：顯示執行動作之使用者的登入ID\
     值：
      - 如果「使用者端型別」為「客戶」，則傳送電子郵件
      - 如果「使用者端型別」為「管理員」，則為使用者名稱
      - 如果「使用者端型別」為「整合」，則使用名稱

3. 重新命名 ***完整動作名稱*** 至 ***Target***
   - ***Target***：顯示動作名稱\
     值：
      - 如果來源是REST API或SOAP API，則為端點
      - 查詢/變異名稱(若GraphQL API)
      - 管理員UI或客戶UI的動作名稱。

#### 設定管理員記錄動作

此功能無法使用，因為預設必須記錄所有動作。

### 匯入/匯出功能

匯入/匯出功能的增強功能著重於改善管理體驗，以及提升使用者動作的可見度。

>[!NOTE]
>
>這些 ***增強功能不會改變匯入/匯出核心邏輯***；它們會擴充功能，提供更完整的記錄並改善資料歸因。 匯入/匯出的基本功能保持不變。 使用者可以繼續使用現有功能和工作流程，不會造成任何中斷。

#### 管理動作記錄

匯入/匯出功能的一項重要改善是強化管理動作的記錄。 此功能可讓您更深入地探索與資料匯入/匯出相關的活動，有助於改善追蹤和稽核能力。 下列動作現在會記錄並反映在 **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**格線：

| 型別 | 動作 |
| ---- | ------- |
| 匯入 | <ul><li>管理員使用者執行匯入<li>管理員使用者下載匯入的檔案<li>管理員使用者下載錯誤檔案<ul/> |
| 匯出 | <ul><li>管理員使用者請求<li>管理員使用者下載匯出的檔案<ul/> |
| 排程的匯入/匯出 | <ul><li>管理員使用者排程匯出<li>管理員使用者編輯已排程的匯出<li>管理員使用者執行排定的匯出<li>管理員使用者會刪除排程的匯出<li>管理員使用者排程匯入<li>管理員使用者編輯已排程的匯入<li>管理員使用者執行排定的匯入<li>管理員使用者會刪除排程的匯入<li>管理員使用者會執行匯入/匯出操作的大量刪除<ul/> |

### 顯示增強功能和改善的篩選/排序

為了讓管理員使用者擁有更多資訊網格，有幾項增強資料顯示以及篩選和排序功能：

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

#### 排定的匯入/匯出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- 已新增 **[!UICONTROL ID]** 欄。
- 已新增 **[!UICONTROL Scheduled At]** 欄(_排程匯入或匯出的日期與時間_)。
- 已新增 **[!UICONTROL User]** 欄(_排程匯入/匯出的管理員使用者名稱_)。

## 停用HIPAA整備功能

### SaaS服務

Adobe Commerce的SaaS服務均不提供HIPAA整備服務。 這包含但不限於：

- 即時搜尋
- API網格
- App Builder
- 目錄服務

### 預設為停用來賓簽出

- 訪客結帳會對HIPAA的各個層面帶來潛在風險，包括記錄、存取控制、PHI衛生和譜系等等。
- HIPAA整備模組中預設會停用訪客簽出，但商家可能會自行承擔啟用風險。

### 預設為停用Newsletter功能

- 電子報功能預設為停用，以防止在行銷內容中使用PHI，但商家可以自行承擔啟用風險。

### 預設為停用進階報表服務設定

進階報告服務設定預設為停用，以防止將PHI用於分析和報告，但商家可以自行承擔啟用風險。

### 預設為停用Sendgrid服務

Sendgrid服務預設為停用，因為應用程式不符合HIPAA標準。 商家可以提交支援要求來啟用Sendgrid，但是他們必須確認將會承擔使用此服務的風險。
