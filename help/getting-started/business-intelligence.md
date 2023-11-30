---
title: 『[!DNL Commerce Intelligence] 工具
description: 瞭解Adobe Commerce和Magento Open Source商戶如何使用Commerce Intelligence工具來獲得用於做出正確業務決策的見解。
exl-id: 687d04e4-841b-44f7-94ca-bbb20fbe2d8b
feature: Commerce Intelligence, Reporting
source-git-commit: c97d6eb4050bbae7e766f01ce50b5c3be7544c5c
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# [!DNL Commerce Intelligence] 工具

使用Commerce Intelligence工具來獲得用於制定正確業務決策的見解。

## [!DNL Commerce Intelligence] 帳戶

當您啟用 [!DNL Commerce Intelligence] 透過Adobe帳戶，您可以存取五個包含約70個報表的控制面板。 這些報表旨在提供有關您資料的深入分析，並回答諸如「我的訂單每月增長如何？」、「誰是我最忠實的客戶？」及「我的優惠券策略有效嗎？」等問題。 如需關於此工具集的詳細資訊，請參閱 [Commerce Intelligence使用手冊][1].

## [!DNL Advanced Reporting]

[!DNL Advanced Reporting] 包含在Adobe Commerce和Magento Open Source中。 此功能可讓您存取一套以您的產品、訂單和客戶資料為根據的動態報表，並根據您的業務需求量身打造個人化控制面板。 當 [!DNL Advanced Reporting] 使用 [!DNL Commerce Intelligence] 對於Analytics，您不需要有Commerce Intelligence帳戶即可使用 [!DNL Advanced Reporting].

如需技術資訊，請參閱 [[!DNL Advanced Reporting]][2]開發人員檔案中的{：target=&quot;_blank&quot;}主題。

>[!NOTE]
>
>[!DNL Commerce Intelligence] 帳戶使用內建報告，而非 [!DNL Advanced Reporting] 功能。

![進階報告儀表板](./assets/reporting-advanced.png){width="700"}

### 需求

* 網站必須在公用網頁伺服器上執行。

* 網域必須具備有效的安全性(SSL)憑證。

* [!DNL Commerce] 必須已順利安裝或升級，且沒有錯誤。

* 在 [!DNL Commerce] 設定 [商店URL](../stores-purchase/store-urls.md)，則 **[!UICONTROL Base URL (Secure)]** 存放區檢視的設定必須指向安全URL。 例如： `https://yourdomain.com`.

* 在 [!DNL Commerce] 存放區URL的設定， **[!UICONTROL Use Secure URLs on Storefront]** 和 **[!UICONTROL Use Secure URLs in Admin]** 必須設為 `Yes`.

* [[!DNL Commerce] crontab][3] 即會建立，且已安裝伺服器上正在執行cron工作。

>[!NOTE]
>
>[!DNL Advanced Reporting] 只能用於 [!DNL Commerce] 已持續使用單一 [基本貨幣](../stores-purchase/currency-configuration.md).


### 步驟1：啟用 [!DNL Advanced Reporting]

在 [!DNL Commerce] 組態， [[!DNL Advanced Reporting]](../configuration-reference/general/advanced-reporting.md) 預設為啟用，並在cron為時自動啟動 [已設定](../configuration-reference/advanced/system.md) 並執行。 每小時的開頭會在接下來的24小時內起始建立訂閱的嘗試，直到成功為止。 在成功建立訂閱之前，訂閱狀態為「擱置中」。

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側導覽面板中， **[!UICONTROL General]** 展開，請選擇 **[!UICONTROL Advanced Reporting]** 並執行下列動作：

   * 確認 **[!UICONTROL Advanced Reporting Service]** 設為 `Enable` （預設設定）。

   * 設定 **[!UICONTROL Time of day to send data]** 根據24小時時鐘，您希望服務從您的商店接收更新資料的時、分、秒。 預設情況下，資料會在凌晨2:00傳送。

   * 在 **[!UICONTROL Industry Data]**，選擇 **[!UICONTROL Industry]** 最能描述您業務的。

   ![進階報告設定](./assets/advanced-reporting-config.png){width="400"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.

1. 出現提示時，按一下 **[[!UICONTROL Cache Management]](../systems/cache-management.md)** 重新整理任何無效的快取。

1. 等待整夜，或等到下次排程更新的時間。 然後，檢查您的訂閱狀態。 如果狀態仍為 _擱置中_，確定您的安裝符合所有要求。

### 步驟2：存取 [!DNL Advanced Reporting]

1. 執行下列任一項作業：

   * 在 _管理員_ 側欄，選擇 **[!UICONTROL Dashboard]**. 然後，按一下 **[!UICONTROL Go to Advanced Reporting]**.
   * 在 _管理員_ 側欄，前往 **[!UICONTROL Reports]** > _[!UICONTROL Business Intelligence]_>**[!UICONTROL Advanced Reporting]**.

   此 [!DNL Advanced Reporting] 控制面板提供訂單、客戶和產品的快速摘要。 請務必向下捲動以檢視完整的儀表板。

1. 若要更妥善地檢視資料，請設定 **[!UICONTROL Filters]** ，位於您要納入報表中的時段和存放區檢視的右上角。 接著，執行下列動作：

   * 將滑鼠指標暫留在任何資料點上，即可取得詳細資訊。
   * 若要檢視所有儀表板報表，請按一下每個標籤。

   ![資料點](./assets/reporting-advanced-data-point.png){width="600" zoomable="yes"}

## 存取 [!DNL Advanced Reporting] 資料資源

在進階報告控制面板的右上角，按一下 **[!UICONTROL Additional Resources]**.

![進階報告資料資源](./assets/advanced-reporting-your-data-resources.png){width="600" zoomable="yes"}

## 疑難排解

如果您收到404「找不到頁面」訊息，請確認您的商店符合 [!DNL Advanced Reporting]. 然後，按照指示驗證整合是否已安裝。

### 確認整合作用中

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integration]**.

1. 確認 **[!UICONTROL Magento Analytics user]** 整合會顯示在清單中，而且 **[!UICONTROL Status]** 是 `Active`.

1. 若要重新建立使用者，請按一下 **[!UICONTROL Reauthorize]** 並執行下列動作：

   ![重新授權](./assets/advanced-reporting-integration-reauthorize.png){width="600"}

   * 出現提示時，按一下 **[!UICONTROL Reauthorize]** 以核准對API資源的存取權。

     ![重新授權對API資源的存取](./assets/advanced-reporting-integration-api.png){width="600"}

   * 確認擴充功能的整合代號清單是否完整。 然後，按一下 **完成**.

     ![整合Token](./assets/advanced-reporting-integration-tokens-for-extensions.png){width="600"}

1. 尋找指出整合的訊息 `Magento Analytics user` 已重新授權。

1. 請稍候一整夜，或等到下次排程更新的時間。

### 驗證單一基礎貨幣

[!DNL Advanced Reporting] 只能用於 [!DNL Commerce] 僅使用單一專案的安裝 [基本貨幣](../stores-purchase/currency-configuration.md) 從安裝時起。 結果是，在歷史記錄中，所有訂單都使用相同的基本貨幣。 [!DNL Advanced Reporting] 如果您在任何時候變更了基準貨幣，且歷史記錄中有使用不同基準貨幣處理的訂單，則無法運作。

若要確定您的商店是否有多重基本貨幣，您可以查詢 [!DNL Commerce] 資料庫從命令列使用下列MySQL範例。 您可能需要變更表格名稱以符合您的資料結構：

```sql
select distinct base_currency_code from sales_order;
```

### 資料差異

如果您注意到 `Data last updated...` 註解會顯示昨天的日期，而不是今天的日期，進階報告更新中可能會延遲最多一天。 此延遲是由於佇列大小大於預期。

## 控制面板報表

**[!UICONTROL Orders]**

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Revenue] | 顯示商店檢視在定義的時段內收到的所有收入。 |
| [!UICONTROL Orders] | 顯示定義時段內透過商店檢視下單的所有訂單。 |
| [!UICONTROL AOV] | 顯示定義時段內透過商店檢視下方的平均訂單值。 |
| [!UICONTROL Refunds] | 顯示定義期間透過商店檢視處理的所有退款。 |
| [!UICONTROL Tax Collected] | 顯示定義期間內透過商店檢視所收集的所有稅捐。 |
| [!UICONTROL Shipping Collected] | 顯示在定義的時段內，透過商店檢視所收取的所有運費。 |
| [!UICONTROL Orders by Status] | 針對定義時段內的商店檢視，依狀態顯示訂單數。 |
| [!UICONTROL Orders by Status] | 依狀態列出訂單數的摘要。 |
| [!UICONTROL Coupon Usage] | 列出在定義的時段內，透過商店檢視兌換的所有優惠券代碼和每個優惠券的使用者人數。 |
| [!UICONTROL Orders and Revenue by Billing Region] | 列出在定義的時段內，商店檢視的訂單數量與收入（依區域）。 |
| [!UICONTROL Tax Collected by Billing Region] | 列出在定義的時段內，依區域針對商店檢視所徵收的稅捐金額。 |
| [!UICONTROL Shipping Fees Collected by Shipping Region] | 列出在定義的時段內，依區域針對商店檢視所收取的送貨費用。 |

{style="table-layout:auto"}

**[!UICONTROL Customers]**

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Unique Customers] | 顯示在定義的時段內與商店檢視相關聯的不重複客戶帳戶數目。 |
| [!UICONTROL New Registered Accounts] | 顯示在定義的時段內，在存放區檢視中註冊的新客戶帳戶數目。 |
| [!UICONTROL Top Coupon Users] | 依客戶ID列出排名最前的抵用券使用者，以及在定義的時段內，為商店檢視下含抵用券的訂單數。 |
| [!UICONTROL Customer KPI Table] | 列出在定義的時段內，商店檢視的訂單數、收入和平均訂單值（依客戶ID）。 |

{style="table-layout:auto"}

**[!UICONTROL Products]**

| 欄位 | 說明 |
|--- |--- |
| [!UICONTROL Quantity of Products Sold] | 顯示定義時段內透過商店檢視出售的產品數量。 |
| [!UICONTROL Products Added to Wishlists] | 列出在定義的時段內，透過商店檢視新增到願望清單的所有產品。 |
| [!UICONTROL Best Selling Products by Quantity] | 列出在定義的時段內透過商店檢視銷售的最暢銷產品和數量。 |
| [!UICONTROL Best Selling Products by Revenue] | 列出在定義的時段內，透過商店檢視銷售產品所產生的暢銷產品和收入。 |

{style="table-layout:auto"}


[1]: https://experienceleague.adobe.com/docs/commerce-business-intelligence/mbi/guide-overview.html
[2]: https://developer.adobe.com/commerce/php/development/advanced-reporting/
[3]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
