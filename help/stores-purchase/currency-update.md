---
title: 更新匯率
description: 瞭解如何手動設定匯率，或將其匯入您的商店。
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# 更新匯率

匯率可以手動設定，或匯入存放區。 為確保您的商店具有最新的匯率，您可以設定要依排程自動更新的匯率。

匯入匯率之前，請先完成 [貨幣匯率設定](currency-configuration.md) 指定您接受的貨幣，並建立匯入連線與排程。

![匯率](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## 手動更新匯率

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. 按一下您要變更的匯率，然後為支援的每種貨幣輸入新值。

1. 完成後，按一下 **[!UICONTROL Save Currency Rates]**.

## 匯入匯率

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. 設定 **[!UICONTROL Import Service]** 至貨幣匯率提供者。

   預設提供者為 `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >從2.4.6版開始， [[!DNL Fixer.io]](https://fixer.io/) 服務已棄用，並由 [[!DNL Fixer API] （愛彼亞）](https://apilayer.com/marketplace/fixer-api) 服務。 強烈建議您使用APILayer帳戶，而非過時的帳戶 [!DNL Fixer.io] 帳戶。

1. 按一下 **[!UICONTROL Import]**.

   更新的費率會顯示在 _[!UICONTROL Currency Rates]_清單。 如果匯率自上次更新後已變更，則舊匯率會顯示在下方以供參考。

1. 完成後，按一下 **[!UICONTROL Save Currency Rates]**.

1. 提示更新快取時，按一下 **[!UICONTROL Cache Management]** 連結並重新整理無效的快取。

   ![系統訊息 — 重新整理無效的快取](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## 依排程匯入匯率

1. 請確定 [Cron](../systems/cron.md) 已為您的商店啟用。

1. 若要指定您接受的貨幣，並建立匯入連線和排程，請完成 [幣別匯率設定](currency-configuration.md).

1. 若要確認費率是依排程匯入，請檢查 _[!UICONTROL Currency Rates]_清單。

1. 等候為排程建立的頻率設定的時間週期，然後再次檢查速率。
