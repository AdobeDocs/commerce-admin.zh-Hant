---
title: Cron （排程工作）
description: 瞭解如何從管理員控制Commerce cron作業的執行和排程。
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Cron （排程工作）

Adobe Commerce和Magento Open Source會定期執行指令碼，依排程執行一些操作。 您可以從管理員控制Commerce cron作業的執行和排程。 根據Cron排程執行的存放區作業包含但不限於：

- [電子郵件](email-communications.md)
- [目錄價格規則](../merchandising-promotions/price-rules-catalog.md)
- [電子報](../merchandising-promotions/newsletters.md)
- [XML Sitemap產生](../merchandising-promotions/sitemap-xml.md)
- [貨幣匯率更新](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>Commerce服務必須安裝在crontab中，以確保核心元件和部分協力廠商擴充功能可如預期般運作。 請參閱 [中的指示 _安裝指南_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html) 有關將服務安裝到crontab的詳細資訊。

此外，您可以將下列設定為根據cron排程執行：

- 訂購系統格線更新與重新索引
- 待處理付款期限

確定 [基本URL](../stores-purchase/store-urls.md) 的設定正確，以便在cron作業期間產生的URL正確無誤。 如需雲端基礎結構上的Adobe Commerce，請參閱 [設定cron工作](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html) 在 _雲端基礎結構上的Commerce指南_. 若為內部部署，請參閱 [設定並執行con](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html) 在 _設定指南_.

## 設定cron

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL System]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Cron]** 區段。

   ![進階設定 — cron工作](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. 完成下列設定 **[!UICONTROL Index]** 和 **[!UICONTROL Default]** 群組。

   每個區段中的設定都相同。

   - **[!UICONTROL Generate Schedules Every]**  — 定義產生排程的頻率（分鐘）。 排程儲存在資料庫中。
   - **[!UICONTROL Schedule Ahead for]**  — 定義預先排程cron工作的時間（以分鐘為單位）。 例如，如果此設定設為 `10` 而且cron會執行，cron作業會排定在未來10分鐘執行。
   - **[!UICONTROL Missed if not Run Within]**  — 定義用於判斷錯過工作的時間（以分鐘為單位）。 如果cron工作未在其排定的時間執行，且經過指定的時間，則無法執行且其狀態設定為 `Missed`.
   - **[!UICONTROL History Cleanup Every]**  — 定義從資料庫中清除已結束工作歷史記錄的時間（以分鐘為單位）。
   - **[!UICONTROL Success History Lifetime]**  — 定義具有的cron作業歷史記錄的時間長度（以分鐘為單位） `Successful` 狀態會保留在資料庫中。
   - **[!UICONTROL Failure History Lifetime]**  — 定義具有下列專案之cron作業歷史記錄的時間長度（以分鐘為單位）： `Error` 狀態會保留在資料庫中。
   - **[!UICONTROL Use Separate Process]**  — 定義群組中所有cron工作是否都在個別的系統處理序中執行。 選項： `Yes` / `No`

   ![進階設定 — cron群組索引](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.
