---
title: '[!DNL Google Content Experiments]'
description: 瞭解如何使用 [!DNL Google Content Experiments] 設定Commerce產品、類別或內容頁面的A/B測試。
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

以下範例說明如何使用Google Analytics內容實驗來設定產品、類別或內容頁面的A/B測試。 我們建議您在完成指示時，保持兩個瀏覽器分頁開啟，因為您需要在Commerce管理員與您的 [!DNL Google Analytics] 帳戶。

>[!NOTE]
>
>[!DNL Google Content Experiments] 已棄用，並計畫由取代 [Google最佳化](https://support.google.com/optimize/answer/7084762?hl=en).

## 步驟1. 啟用內容實驗（商務）

1. 登入您的Commerce安裝的Admin。

1. 依照指示啟用 [Google Analytics](google-analytics.md) 商業設定中的內容實驗。

   ![銷售設定 — Google API -Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## 步驟2. 設定變數（商務）

建立相同產品、類別或頁面的多個變數。

- 每個變數必須具有唯一 [URL索引鍵](../catalog/catalog-urls.md).
- 每個變數必須具有相同的 [存放區檢視](../getting-started/websites-stores-views.md#scope-settings) 已選取。

您可以針對要測試的每個實體建立最多十個變體。 若為產品，請使用 [儲存並複製](../catalog/product-workspace.md) 以節省時間。

## 步驟3. 設定實驗(Google)

>[!NOTE]
>
>您必須擁有Google帳戶的適當許可權，才能建立實驗。

1. 開啟另一個瀏覽器索引標籤，然後登入 [Google Analytics][2] 帳戶。

   如有需要，請導覽至 **[!UICONTROL Account]** 和 **[!UICONTROL Property]**.

1. 在左側的側邊欄中，選擇 **[!UICONTROL Admin]** 並使用下列其中一種方法：

   **方法1：** 選擇現有檢視

   在「 」的標題中 _[!UICONTROL View]_欄，按一下向下箭頭，然後選擇要提供實驗資料的檢視。

   **方法2：** 建立新的報表檢視

   - 在「 」的標題中 _檢視_ 欄，按一下 **[!UICONTROL Create View]** 並執行下列動作：

      - 將實驗位置識別為 `Website` 或 `Mobile app`.

      - 輸入描述性 **[!UICONTROL Reporting View Name]**.

      - 指定 **[!UICONTROL Reporting Time Zone]**.

   - 完成後，按一下 **[!UICONTROL Create View]** 然後按一下「上一步」箭頭，返回上一頁。

1. 在左側面板中的 _[!UICONTROL Reports]_，選擇&#x200B;**[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. 按一下 **[!UICONTROL Create experiment]** 並執行下列動作：

   - 指定要重新導向的流量百分比。

   - 指定 **[!UICONTROL Original Page URL]** 以及每個的URL **[!UICONTROL page variation]** 要測試的物件。

   - 完成其他選項。

1. 設定實驗時，按一下 **[!UICONTROL Manually Insert the Code]** 並復製程式碼片段。

## 步驟4. 貼上程式碼片段(Commerce)

1. 返回Commerce安裝的管理員，並以編輯模式開啟產品、類別或頁面的原始版本。

1. 展開 **[!UICONTROL View Optimization]** 產品、類別或頁面的區段。

1. 將您從Google Analytics複製的程式碼片段貼到 **[!UICONTROL Experiment Code]** 文字方塊。

   >[!NOTE]
   >
   >請勿將程式碼片段貼入任何變數中。

   ![產品檢視最佳化](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save]**.

## 步驟5：檢閱並啟動實驗(Google)

1. 返回您的 [Google Analytics][2] 帳戶。

1. 檢閱實驗設定。

1. 如果準備開始，請按一下 **[!UICONTROL Start Experiment]**.

   否則，按一下 **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
