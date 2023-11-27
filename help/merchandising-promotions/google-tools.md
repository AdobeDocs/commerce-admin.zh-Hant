---
title: Google網站工具
description: 瞭解可用來最佳化內容、分析流量以及將目錄連結至購物彙總和市場的Google工具整合。
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Google網站工具

您的商店設定與以下Google工具整合，以協助最佳化您的內容、分析您的流量，以及將您的目錄連結至購物彙總和行銷場所。

- [Google Analytics](google-analytics.md)  — 使用 _Google Universal Analytics_ 定義其他自訂維度和量度以進行追蹤，並支援離線和行動應用程式互動，以及存取持續更新。

- [Google內容實驗](google-content-experiments.md)  — 使用Google Analytics內容實驗為產品、類別或內容頁面設定A/B測試。

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (僅限Adobe Commerce)使用Google標籤管理員來管理許多與行銷活動事件相關的標籤。

- [Google AdWords](google-adwords.md)  — 建立Google AdWords行銷活動並追蹤您商店的轉換情形。

{{gtag-api-note}}

## Google隱私權設定

如果您的企業必須遵守隱私權法規，例如 [GDPR](../getting-started/compliance-gdpr.md) 或 [CCPA](../getting-started/compliance-ccpa.md)，變更Google工具的預設設定以符合隱私權要求。 請依照下列步驟操作，以確保您使用客戶資料的方式符合法規。

### 步驟1：更新Google設定

1. [登入][1]{： target=&quot;_blank&quot;}至貴公司的Google Analytics帳戶。

1. 在左側邊欄底部，選擇 **[!UICONTROL Admin]**，然後導覽至您要編輯的帳戶（如果適用）。

1. 在 **[!UICONTROL Account]** 欄，按一下 **[!UICONTROL Account Settings]**.

1. 為符合隱私權法規要求，請關閉資料共用。

   預設Google Analytics設定會將您的公司資料與Google和其他各方共用。若要關閉資料共用，請清除下列設定的選取核取方塊：

   - Google產品和服務
   - 基準測試
   - 技術支援
   - 客戶專家

1. 接受 _資料處理修正_.

   Google Ads資料處理術語說明Google如何處理資料，以及為確保受GDPR規範的業務資料安全性所採取的措施。 您合法實體與聯絡人資訊的記錄也會隨修訂內容一併維護。 至 [瞭解更多][2]{： target=&quot;_blank&quot;}，按一下頁面頂端訊息中的連結。

   - 向下捲動頁面至 **[!UICONTROL Data Processing Amendment]**.
   - 按一下 **[!UICONTROL Review Amendment]** 以閱讀 _Google Ads資料處理辭彙_.
   - 按一下 **[!UICONTROL Accept]**.
   - 按一下 **[!UICONTROL Save]**.

1. 完成 _DPA管理_ 詳細資料。

   - 按一下 **[!UICONTROL Manage DPA Details]** 開啟DPA管理頁面，您可在此編輯連絡人和貴組織的合法實體。

   - 在 **[!UICONTROL Legal Entities]** 區段，按一下 _編輯_ ( ![Google編輯圖示](./assets/google-icon-edit.png) )圖示，並為您的組織新增一或多個已註冊名稱。 完成後，按一下 **[!UICONTROL Save]**.

   - 在 **連絡人** 區段，按一下 _新增_ ( ![Google新增圖示](./assets/google-icon-add.png) )圖示並輸入第一個連絡人的資訊。 接著，選取每個適用角色的核取方塊，然後按一下 **[!UICONTROL Add]**.

      - 主要聯絡人 — （通知電子郵件地址）傳送通知的聯絡人。
      - 資料保護人員 — （若適用）專責促進隱私權法規遵循的人員。
      - 歐洲經濟區(EEA)代表 — （若適用）代表歐盟以外客戶且履行GDPR義務的人員。

     重複以上步驟以新增其他連絡人（如果適用）。

### 步驟2：修改您的Google JS程式庫

Google支援三個JavaScript程式庫來測量網站使用量，視Google產品而定： `gtag.js`， `analytics.js`、和 `ga.js`. 為了滿足隱私權要求，標準程式碼可以修改如下：

#### 將IP位址匿名化

匿名化所使用的IP位址 **_Google Universal Analytics_**，將下列程式碼片段新增至 `analytics.js` Web伺服器上的程式庫：

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

若要進一步瞭解，請參閱 [Analytics.js欄位參考][3]{： target=&quot;_blank&quot;}於Google說明。

如果您使用舊版 `ga.js` 程式庫中，新增下列程式碼片段：

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

匿名化所使用的IP位址 **_Google Tag Manager_**，設定 `anonymize_ip` 引數至 `true` 在 `gtag.js` 程式庫。

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

若要深入瞭解，請參閱 [Analytics中的IP匿名化][4] Google說明中的。

#### 強制SSL

若要強制透過安全通訊端層(SSL)傳輸所有Google資料，請將下列程式碼片段新增至 `analytics.js` 程式庫。

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### 步驟3：更新您的隱私權原則

更新您的 [隱私權原則](../getting-started/privacy-policy.md) 宣告您的公司：

- 使用Google Analytics
- 隱藏IP位址以隱藏個人資訊
- 已關閉Google資料共用
- 不使用其他Google服務搭配Google AnalyticsCookie

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
