---
title: Adobe Commerce的HIPAA整備程度
description: 了解如何新增 Adobe Commerce HIPAA-Ready 擴充功能並取得其他特性和功能，讓您可以遵守 HIPAA 義務。
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '2300'
ht-degree: 1%

---

# Adobe Commerce的HIPAA整備程度

>[!IMPORTANT]
>
>**法律免責宣告**<br/>
>此資訊旨在協助Adobe客戶回答他們有關Adobe HIPAA就緒服務的問題。 這不構成法律建議。 商戶應諮詢自己的法律顧問，瞭解其根據HIPAA所負的義務，以及Adobe產品的適當使用和設定。

>[!BEGINSHADEBOX]

**健康保險可攜性及責任法案(HIPAA)**

健康保險便利與責任法案(HIPAA)是美國重要的聯邦醫療保健隱私法，由美國衛生與公眾服務部(HHS)執行。 HIPAA適用於&#x200B;_涵蓋的實體_ （例如醫療服務提供者、保險公司和結算所）和&#x200B;_商業夥伴_ （例如為涵蓋的實體提供服務的實體）。 HIPAA要求是在三個不同的規則中設定：隱私權規則、安全性規則和違規通知規則。 Adobe可作為某些產品的Business Associate，而Adobe會將此類產品分類為「HIPAA就緒服務」。 受HIPAA規範管理的資料稱為&#x200B;_受保護的健康資訊_&#x200B;或PHI。 PHI為健康資訊的子集，其中(1)由健康資訊提供者、健康計畫或健康資訊中心建立或接收，(2)關於個人過去、現在或未來的身體或精神健康或狀況，關於向個人提供健康資訊或向個人提供健康資訊的過去、現在或未來付款，以及(3)識別個人或有合理依據相信資訊可用於識別個人的相關資訊。 HIPAA隱私和安全規則要求受保實體以商業夥伴協定或BAA的形式從商業夥伴獲得書面保證，要求商業夥伴保護受保實體PHI的隱私和安全。 如需詳細資訊，請參閱Adobe信任中心中的[HIPAA與Adobe產品和服務](https://www.adobe.com/trust/compliance/hipaa-ready.html)。

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA就緒

Adobe Commerce HIPAA就緒擴充功能為Adobe Commerce安裝新增了其他功能，讓商家可遵守各自的HIPAA義務。

雲端基礎結構或Adobe Commerce Managed Services專案上的Adobe Commerce可使用Adobe HIPAA就緒擴充功能`magento/hipaa-ee`。 Adobe Commerce HIPAA就緒安裝程式會停用某些原生服務和功能以符合HIPAA要求。 請參閱[已停用的服務和功能](#disabled-services-and-features)。

>[!NOTE]
>
>只有已購買Adobe Commerce的醫療保健附加元件的商家才能使用HIPAA就緒的功能。

*這些資料僅供參考。 提供此資訊不會賦予收件者任何合約權利或其他權利。 雖然已努力確保資料在提供之日的準確性，但並未表示資料準確且完整。 法律或Adobe的產品有所變更，Adobe不承擔更新此資訊的義務。 此外，未經Adobe書面同意，不得將此檔案散發給預定收件者以外的任何一方。*

## 系統需求

Adobe Commerce必須部署在雲端基礎結構上的Adobe Commerce上，或使用2.4.6-p3 - 2.4.6-p8版本的Adobe Commerce Managed Services （無Beta版本）。

## 安裝

**先決條件**

>[!BEGINSHADEBOX]

- Adobe已布建您的Adobe Commerce帳戶以存取HIPAA Ready擴充功能。
- 存取[repo.magento.com](https://repo.magento.com)以安裝擴充功能。 如需金鑰產生與取得必要許可權，請參閱[取得您的驗證金鑰](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)。

>[!ENDSHADEBOX]

在執行Adobe 2.4.6-p3 - 2.4.6-p8版的執行個體上安裝最新版本的Adobe Commerce HIPAA-Ready Services擴充功能(`magento/hipaa-ee`)。 擴充功能會從[repo.magento.com](https://repo.magento.com)存放庫以撰寫器中繼資料的形式傳送。 中繼套件包括啟用Adobe Commerce執行個體的HIPAA功能的模組集合。

>[!NOTE]
>
>若要確保傳送至Experience Platform的後台事件資料可使用HIPAA，請參閱[資料連線延伸指南](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension)。

1. 在本機工作站上，變更至雲端基礎結構專案上Adobe Commerce的專案目錄。

   >[!NOTE]
   >
   >如需有關在本機管理Commerce專案環境的資訊，請參閱《雲端基礎結構使用手冊》中&#x200B;_Adobe Commerce的[使用CLI管理分支](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches)_。

1. 簽出環境分支以使用Adobe Commerce Cloud CLI更新。

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. 使用撰寫器CLI將中繼套件`magento/hipaa-ee`新增至撰寫器設定。

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
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   所有首碼為`Magento_Hipaa`的模組都必須位於啟用的模組區段中。

## HIPAA整備的增強功能

`magento/hipaa-ee`擴充功能引進了基礎Commerce產品的一些變更和增強功能。 以下各節提供這些變更的詳細資訊，以及變更基礎產品的方式。

### 動作記錄檔

稽核記錄是HIPAA的要求。 在Adobe Commerce中，[動作記錄檔](../../systems/action-log.md)功能會記錄您商店中工作的管理員使用者所做的每次變更。 為了滿足稽核記錄的HIPAA要求，功能已更新，以記錄所有透過管理員UI和API呼叫執行的管理員使用者和客戶動作。

動作記錄也會在Adobe服務存取您的存放區資料時擷取事件。 您可以篩選「動作記錄」報表中的「外部傳送的資料」動作，以識別這些事件。

#### 動作記錄報告

已修改&#x200B;_動作記錄_&#x200B;報表格線（**[!UICONTROL System]** >動作記錄>報表），以容納透過Admin UI和API執行的客戶動作。

1. 新增兩欄：
   - ***Source***：顯示執行動作的位置。
值： `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
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
      - 查詢或變異名稱(若為GraphQL API)
      - 是管理員UI或客戶UI時的動作名稱。

#### 設定管理員記錄動作

此功能無法使用，因為預設必須記錄所有動作。

### hipaa客戶搜尋結果限制

Adobe Commerce中的HIPAA客戶搜尋結果限制功能會限制對受保護健康資訊(PHI)和個人識別資訊(PII)的存取，以確保符合HIPAA法規。 此功能限制根據使用者角色搜尋和檢視客戶記錄的能力，確保只有授權使用者才能存取此資訊。

#### 主要功能

- **搜尋限制**：沒有必要角色的使用者無法搜尋或檢視客戶記錄。
- **存取權的強制搜尋**：不同於預設的Adobe Commerce行為，如果不執行搜尋，就不可能看到客戶資訊。 這可確保使用者必須瞭解客戶的特定詳細資料，才能找到其資訊。
- **有限的搜尋結果**：符合條件的搜尋結果限製為10筆記錄，確保一次只顯示可管理的記錄數。
- **最小篩選數目**：使用者必須套用最少三個篩選（例如電子郵件、姓氏和狀態）才能執行搜尋，確保搜尋是特定且有針對性的。
- **篩選通知**：啟用搜尋限制時，會通知使用者套用篩選條件以縮小搜尋結果。

#### 設定

限制搜尋結果中客戶數量的設定位於&#x200B;**[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**&#x200B;下的管理面板中。 安裝`hipaa-ee`擴充功能時，此設定預設為啟用。

- **限制格線中的客戶數目**：此設定可讓您啟用或停用格線搜尋結果中顯示的客戶數目限制。
- **客戶格線搜尋結果限制**：此設定會指定格線搜尋結果中可顯示的客戶記錄數目上限。

#### 受影響的功能區域

「管理員建立訂單」頁面(**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]**)和「客戶」頁面(**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**)上的客戶網格會受搜尋結果限制功能的影響。

- 篩選器預設為開啟。
- 使用者必須至少套用三個篩選器才能執行搜尋。
- 依預設，搜尋結果限製為10筆記錄。
- 如果有更多記錄符合搜尋條件，通知會通知使用者結果限制以及需要縮小其搜尋範圍。
- 無法使用格點分頁。
- 導覽離開頁面時，未儲存先前套用的搜尋結果和篩選器。

搜尋結果限制功能也適用於客戶搜尋的REST API (`/V1/customers/search`)。

- 若未套用篩選器或篩選器不足，API會傳回錯誤訊息，指出執行搜尋所需的篩選器數。
- 授權使用者套用足夠的篩選器時，API會傳回指定限制內的結果。
- 結果有限時，會新增訊息至回應，指出找到的記錄總數和目前套用的限制。

### 匯入和匯出特徵

匯入和匯出功能的增強功能著重於改善管理體驗並提供使用者動作的更佳可見度。

>[!NOTE]
>
>這&#x200B;***項增強功能不會改變匯入和匯出核心邏輯***，而是擴充功能以提供更完整的記錄並改善資料歸因。 匯入和匯出的基本功能保持不變。 使用者可以繼續使用現有功能和工作流程，不會造成任何中斷。

#### 管理動作記錄

匯入和匯出功能的重要改善之一，是增強了管理動作的記錄功能。 此增強功能引進更深入探究與資料匯入和匯出相關的活動的能力，有助於改善追蹤和稽核能力。 下列動作現已記錄並反映在「**[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**」格線中：

| 型別 | 動作 |
| ---- | ------- |
| 匯入 | <ul><li>管理員使用者執行匯入<li>管理員使用者下載匯入的檔案<li>管理員使用者下載錯誤檔案<ul/> |
| 匯出 | <ul><li>管理員使用者請求<li>管理員使用者下載匯出的檔案<ul/> |
| 排程的匯入/匯出 | <ul><li>管理員使用者排程匯出<li>管理員使用者編輯已排程的匯出<li>管理員使用者執行排定的匯出<li>管理員使用者會刪除排程的匯出<li>管理員使用者排程匯入<li>管理員使用者編輯已排程的匯入<li>管理員使用者執行排定的匯入<li>管理員使用者會刪除排程的匯入<li>管理員使用者會執行匯入/匯出操作的大量刪除<ul/> |

### 顯示增強功能及改善的篩選和排序

為讓管理員使用者擁有更多資訊網格，HIPAA就緒服務提供數個增強功能，用於顯示、篩選和排序資料。

#### 匯入歷程記錄([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- 已針對&#x200B;**[!UICONTROL Imported File]**、**[!UICONTROL Error File]**、**[!UICONTROL Execution Time]**&#x200B;和&#x200B;**[!UICONTROL Summary]**&#x200B;以外的所有資料行啟用篩選。

#### 匯出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- 已新增&#x200B;**[!UICONTROL ID]**&#x200B;欄。
- 已新增&#x200B;**[!UICONTROL Requested At]**&#x200B;欄（_要求匯出的日期和時間_）。
- 新增&#x200B;**[!UICONTROL User]**&#x200B;欄（_執行要求的管理員使用者名稱_）。
- 已移除&#x200B;**[!UICONTROL Action]**&#x200B;欄。
- 已將&#x200B;**[!UICONTROL Download]**&#x200B;連結移動到&#x200B;**[!UICONTROL File name]**&#x200B;欄（_類似匯入歷程記錄格線_）。
- 已停用負責刪除匯出檔案的動作（_以改進追蹤_）。
- 已針對&#x200B;**[!UICONTROL File name]**&#x200B;以外的所有欄啟用排序。
- 已針對所有欄啟用篩選功能。

#### 已排程的匯入和匯出([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- 已新增&#x200B;**[!UICONTROL ID]**&#x200B;欄。
- 已新增&#x200B;**[!UICONTROL Scheduled At]**&#x200B;欄（排定匯入或匯出的&#x200B;_日期和時間_）。
- 新增&#x200B;**[!UICONTROL User]**&#x200B;欄（排程匯入或匯出的管理員使用者名稱&#x200B;__）。

## 符合HIPAA要求的服務與工具

本節說明可與Adobe Commerce的HIPAA產品搭配使用的符合HIPAA的Adobe服務。 本檔案還介紹可用來協助監視商店關鍵安全性和合規性控制的工具。

| 服務 | 生產 | 分段 | staging_for_support | 開發 |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce與Healthcare附加元件 | 是 | 是 | 是 | 否 |
| 傳送格線 | 否 | 否 | 否 | 否 |
| AWS Simple電子郵件服務 | 是 | 是 | 是 | 否 |

### Adobe Commerce服務

下表列出適用於HIPAA整備產品的Adobe Commerce服務。 這些服務包括但不限於：

| 服務 | 非生產 | 生產 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/overview/) | 是 | 是 |
| 適用於Adobe Developer App Builder的[API Mesh](https://developer.adobe.com/graphql-mesh-gateway/) | 是 | 是 |
| [SaaS資料匯出](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) | 是 | 是 |
| [即時搜尋](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) | 否 | 否 |
| [產品建議](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/overview) | 否 | 否 |
| [付款服務](https://experienceleague.adobe.com/en/docs/commerce/payment-services/guide-overview) | 否 | 否 |
| [資料連線後台事件](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice) | 是 | 是 |
| [資料連線店面活動](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#storefront-events) | 否 | 否 |
| [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) | 否 | 否 |

### 工具

適用於Adobe Commerce的[安全性掃描工具](../../systems/security-scan.md)可協助您監視存放區，以確保所有必要的安全性控制項皆已啟用並可運作。 除了標準安全性檢查外，Adobe已增強此工具，為使用Adobe Commerce HIPAA產品的客戶顯示HIPAA特定檢查。 安全掃描工具中的HIPAA檢查旨在確保：

- 未停用稽核模組
- 未停用雙因素驗證(2FA)
- 行銷功能已停用
- 所有安裝的擴充功能都與預先定義的允許清單相符
- 未安裝不支援的Adobe服務

您可以[設定工具](../../systems/security-scan.md#run-a-security-scan)以傳送電子郵件通知給您，其中包含排程掃描或[手動檢視報告](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/launch/overview#to-review-the-report)的詳細資料。

## 停用的功能

為了符合HIPAA要求，Adobe Commerce支援的部分功能可能不提供或預設為停用。 商家可以選擇重新啟用或使用這些功能，但需自行承擔相關風險。

HIPAA整備模組預設會停用下列功能。 商家可以自行承擔啟用任何這些功能的風險。

- **[異動電子郵件](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)** — 預設會停用SendGrid，因為服務未符合HIPAA要求。 Adobe Commerce提供可搭配您自己的[AWS Simple Email Service](https://docs.aws.amazon.com/ses/)帳戶使用的整合選項。 如需設定詳細資訊，請聯絡客戶技術客戶經理或Adobe Commerce支援。

- **[訪客簽出](../../stores-purchase/checkout-guest.md)** — 此功能對HIPAA的各個方面帶來潛在風險，包括記錄、存取控制、PHI衛生和歷程等等。

- **[電子報功能](../../merchandising-promotions/newsletters.md)** — 此功能已停用，以防止行銷內容使用PHI。

- **[進階報告服務設定](../../getting-started/business-intelligence.md)** — 此設定已停用，以防止將PHI用於分析和報告。
