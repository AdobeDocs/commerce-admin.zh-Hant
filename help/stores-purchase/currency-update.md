---
title: 更新匯率
description: 瞭解如何手動設定匯率，或將其匯入您的商店。
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 更新匯率

匯率可以手動設定，或匯入存放區。 為確保您的商店具有最新的匯率，您可以設定要依排程自動更新的匯率。

在匯入貨幣匯率之前，請先完成[貨幣匯率設定](currency-configuration.md)，以指定您接受的貨幣，並建立匯入連線與排程。

![匯率](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## 手動更新匯率

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**。

1. 按一下您要變更的匯率，然後為支援的每種貨幣輸入新值。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Currency Rates]**。

## 匯入匯率

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**。

1. 將&#x200B;**[!UICONTROL Import Service]**&#x200B;設為貨幣匯率提供者。

   預設提供者為`fixer.io (legacy)`。

   >[!IMPORTANT]
   >
   >從2.4.6版開始，[[!DNL Fixer.io]](https://fixer.io/)服務已過時，並由[[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api)服務取代。 強烈建議您使用APILayer帳戶，而非已棄用的[!DNL Fixer.io]帳戶。

1. 按一下&#x200B;**[!UICONTROL Import]**。

   更新的費率會顯示在&#x200B;_[!UICONTROL Currency Rates]_清單中。 如果匯率自上次更新後已變更，則舊匯率會顯示在下方以供參考。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Currency Rates]**。

1. 當提示更新快取時，請按一下&#x200B;**[!UICONTROL Cache Management]**&#x200B;連結，然後重新整理無效的快取。

   ![系統訊息 — 重新整理無效的快取](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## 依排程匯入匯率

1. 請確定您的商店已啟用[Cron](../systems/cron.md)。

1. 若要指定您接受的貨幣並建立匯入連線與排程，請完成[貨幣匯率設定](currency-configuration.md)。

1. 若要確認費率已依排程匯入，請檢查&#x200B;_[!UICONTROL Currency Rates]_清單。

1. 等候為排程建立的頻率設定的時間週期，然後再次檢查速率。
