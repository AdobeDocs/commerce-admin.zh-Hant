---
title: '[!DNL Google Analytics]'
description: 瞭解如何使用 [!DNL Google Analytics] 為您的Commerce網站收集有用的量度。
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics]可讓您定義額外的自訂維度和量度以進行追蹤，並支援離線和行動應用程式互動，以及存取持續更新。 [!DNL Google Analytics] 4是Google的新一代測量解決方案，正在取代[!DNL Universal Analytics]。 在2023年7月1日，標準Universal Analytics屬性將停止處理新點選。

>[!NOTE]
>
>如果您的企業受到隱私權法規的約束，例如[一般資料保護規範](../getting-started/compliance-gdpr.md)和/或[加州消費者隱私保護法](../getting-started/compliance-ccpa.md)，請參閱[Google隱私權設定](google-tools.md#google-privacy-settings)。

>[!IMPORTANT]
>
>如果您啟用[Cookie限制模式](../getting-started/compliance-cookie-law.md)，[!DNL Google Analytics]將不會收集訪客的相關資料，除非訪客已接受Cookie。

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### 步驟1：設定[!UICONTROL Google Analytics] 4

如果您尚未設定網站的[!DNL Google Analytics] 4，請遵循下列其中一種方法：

- [第一次設定Analytics資料集合](https://support.google.com/analytics/answer/9304153)
- [將Google Analytics4新增至具有 [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)的網站

### 步驟2：完成Commerce設定

1. 登入Commerce商店的管理員。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Google API]**。

1. 展開&#x200B;**[!UICONTROL Google GTag]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Google Analytics4]**&#x200B;子區段，然後執行下列動作：

   - 將&#x200B;**[!UICONTROL Enable]**&#x200B;設為`Yes`。

   - 將&#x200B;**[!UICONTROL Account type]**&#x200B;保留為`Google Analytics4`。

   - 輸入您的&#x200B;**[!UICONTROL Measurement ID]**。 若要深入瞭解，請參閱[Google Analytics說明](https://support.google.com/analytics/answer/9539598)。

   - 如果您想要對內容進行A/B測試和其他效能測試，請將&#x200B;**內容實驗**&#x200B;設定為`Yes`。

   ![銷售組態 — 適用於Google Analytics的Google API 4](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## Google Universal Analytics

>[!IMPORTANT]
>
>2023年7月1日，標準Universal Analytics屬性將不再處理資料。 如果您還是依賴[!DNL Universal Analytics]，建議您[準備使用Google Analytics4](https://support.google.com/analytics/answer/10759417)。

### 步驟1：設定Google Universal Analytics

造訪Google網站，並註冊[Google Universal Analytics][1]帳戶。

### 步驟2：完成Commerce設定

1. 登入Commerce商店的管理員。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Google API]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Google Analytics]**&#x200B;區段，然後執行下列動作：

   - 將&#x200B;**[!UICONTROL Enable]**&#x200B;設為`Yes`。

   - 輸入您的[!DNL Google Analytics] **[!UICONTROL Account Number]**。

   - 如果您想要對內容進行A/B測試和其他效能測試，請將&#x200B;**[!UICONTROL Content Experiments]**&#x200B;設為`Yes`。

   ![銷售組態 — Google API -Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 增強型電子商務

增強型電子商務是[!DNL Google Universal Analytics]的外掛程式，可讓您深入瞭解客戶的購物和購買行為。 您可以使用增強型電子商務產生有關關鍵客戶活動的報表，例如客戶在購物車中新增專案、開始結帳程式或完成購買時。 您也可以識別和分析放棄購物車但不購買的購物者模式。

下列指示顯示如何使用[!DNL Universal Analytics]設定[!DNL Google Tag Manager]以產生增強型電子商務資料和報表。

### 步驟1. 註冊Google帳戶

1. 註冊[Google Tag Manager](google-tag-manager.md)帳戶，並完成Commerce設定。

1. 註冊新的[Google Universal Analytics][1]帳戶。

### 步驟2. 設定增強型電子商務

1. 登入您的Google Universal Analytics帳戶。

1. 使用下列設定來建立Enhanced Ecommerce Analytics的屬性：

   - 狀態：開啟
   - 相關產品：開啟
   - 啟用增強型電子商務報告：開啟
   - 簽出標籤： （不需要）

1. 完成時，按一下&#x200B;**[!UICONTROL Submit]**。

### 步驟3. 建立標籤和觸發器

1. 登入您的[!DNL Google Tag Manager]帳戶並建立下列觸發程式：

   | 名稱 | 事件型別 | 篩選 |
   |--- |--- |--- |
   | `addToCart` | 自訂事件 |  |
   | `checkout` | 自訂事件 |  |
   | `checkout only` | 頁面檢視 | 頁面URL符合RegEx /checkout/。* |
   | `checkoutOption` | 自訂事件 |  |
   | `gtm.dom` | 自訂事件 |  |
   | `productClick` | 自訂事件 |  |
   | `promotionClick` | 自訂事件 |  |
   | `removeFromCart` | 自訂事件 |  |

   >[!NOTE]
   >
   >僅針對內建的Commerce基本付款方法（例如`Check / Money Order`和`Cash On Delivery Payment`）觸發[!UICONTROL Checkout]事件。 `PayPal checkout`和其他外部付款方法不會執行此事件，這些方法使用重新導向以從外部資源結帳。

1. 使用相同的基本設定建立下列Universal Analytics標籤。

   - Universal Analytics標籤

     | 名稱 | 型別 | 正在引發觸發程式 |
     |--- |--- |--- |
     | `Add to cart tracking` | Universal Analytics | addToCart |
     | `Checkout option tracking` | Universal Analytics | checkoutoption |
     | `Checkout tracking` | Universal Analytics | 簽出 |
     | `Pageview tracking` | Universal Analytics | gtm.dom |
     | `Product click tracking` | Universal Analytics | productClick |
     | `Promo click tracking` | Universal Analytics | promotionClick |
     | `Remove from cart tracking` | Universal Analytics | removeFromCart |

   - 基本標籤設定

     | 設定 | 值 |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | Universal Analytics |
     | [!UICONTROL Tracking ID] | UA-XXX （來自您的Universal Analytics帳戶的追蹤ID。） |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | 真 |
     | [!UICONTROL Use data layer] | 真 |
     | [!UICONTROL Use Debug version] | 真 |

1. 完成個別追蹤設定。

   - 輸入下列&#x200B;**[!UICONTROL Add to Cart]**&#x200B;個追蹤設定：

     | 設定 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 電子商務 |
     | [!UICONTROL Action] | 加入購物車 |
     | [!UICONTROL Trigger] | addToCart |

   - 輸入下列&#x200B;**[!UICONTROL Checkout option]**&#x200B;個追蹤設定：

     | 設定 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 電子商務 |
     | [!UICONTROL Action] | 簽出選項 |
     | [!UICONTROL Trigger] | checkoutoption |

   - 輸入下列&#x200B;**[!UICONTROL PageView]**&#x200B;個追蹤設定：

     | 設定 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | PageView |
     | [!UICONTROL Trigger] | gtm.dom |

   - 完成下列&#x200B;**[!UICONTROL Product Click]**&#x200B;追蹤設定：

     | 設定 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 電子商務 |
     | [!UICONTROL Action] | 產品點按 |
     | [!UICONTROL Trigger] | productClick |

   - 完成下列&#x200B;**[!UICONTROL Promotion Click]**&#x200B;追蹤設定：

     | 設定 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 電子商務 |
     | [!UICONTROL Action] | 促銷活動點按 |
     | [!UICONTROL Trigger] | promotionClick |

   - 完成下列&#x200B;**[!UICONTROL Remove from Cart]**&#x200B;追蹤設定：

     | 設定 | 值 |
     |--- |--- |
     | [!UICONTROL Track Type] | 事件 |
     | [!UICONTROL Category] | 電子商務 |
     | [!UICONTROL Action] | 從購物車移除 |
     | [!UICONTROL Trigger] | removeFromCart |

1. 完成後，請按一下「**[!UICONTROL Preview]**」並確認標籤是否正確運作。

1. 驗證設定後，請按一下&#x200B;**[!UICONTROL Publish]**。


[1]: https://support.google.com/analytics/answer/2817075?hl=en
