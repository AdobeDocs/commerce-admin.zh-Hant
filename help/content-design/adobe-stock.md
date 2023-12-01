---
title: Adobe Stock整合
description: 將Adobe Stock與您的整合 [!DNL Commerce] 例項，可存取無數用於商店的媒體資產。
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 6666073a48741cb494f408a61401f46fc20cedc4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Adobe Stock整合

若要存取無數用於商店的媒體資產，請整合 [Adobe Stock][adobe-stock] 替換為 [!UICONTROL Commerce].

![Adobe Stock搜尋結果](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Adobe Stock服務可讓企業針對其所有創意專案，存取數百萬張高品質、精心策劃、免版稅的像片、向量、插圖、影片、範本和3D資產。 [!DNL Commerce] 使用者能快速尋找、預覽和授權Adobe Stock資產。 使用者也可將其儲存至 [媒體儲存][media-storage]，而無須離開管理員工作區。

## 必要條件

這項整合需要：

- 一個 [Adobe Developer][dev-console] 帳戶
- Adobe Commerce或Magento Open Source，2.3.4或更新版本

授權Adobe Stock影像需要：

- 一個 [Adobe帳戶][adobe-signin]
- 付費 [Adobe Stock][adobe-stock] 與帳戶相關聯的計畫

## 整合 [!DNL Commerce] 和Adobe Stock

為Adobe Commerce設定Adobe Stock整合有兩個步驟：

1. [建立adobe.developer整合](#create-an-adobe-developer-integration) 產生API金鑰
1. [在商務管理員中設定Adobe Stock整合](#configure-the-adobe-stock-integration)

### 建立Adobe Developer整合

1. 導覽至 [Adobe Developer Console][dev-console].

1. 在 _[!UICONTROL Quick Start]_，按一下&#x200B;**[!UICONTROL Create new project]**.

1. 在 _[!UICONTROL Project overview]_封鎖，按一下&#x200B;**[!UICONTROL Add API]**.

1. 選取 **[!UICONTROL Adobe Stock]** 從整合清單中，按一下 **[!UICONTROL Next]**.

1. 選取OAuth 2.0 **[!UICONTROL Web App]**.

1. 指定 **[!UICONTROL redirect URI]**.

   預設的重新導向URI採用格式 `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`，例如 `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`，其中：

   - `${HOST}` 是您的 [!DNL Commerce] 完整網域名稱(例如 `https://store.myshop.com`)。
   - `${ADMIN_URI}` 是您的 [!DNL Commerce] 管理員URI (例如 `admin_hgkq1l`)，可透過執行 `magento info:adminuri`.

1. 指定 **[!UICONTROL Redirect URI pattern]**，與您的重新導向URI相同，有兩個差異：

   - 任何句號(`.`)必須使用兩個反斜線(`\\`)。
   - 新增 `.*` 至圖樣的結尾。

   使用先前預設重新導向URI的範例，可能是 `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. 按一下 **[!UICONTROL Next]**.

1. 檢閱可用的範圍，然後按一下 **[!UICONTROL Save configured API]**.

1. 在接下來的頁面上，複製 **[!UICONTROL Client ID]** （API金鑰）和 **[!UICONTROL Client secret]**.

   此資訊將用於下一節的步驟中。

### 設定Adobe Stock整合

若要設定您的系統組態 [!DNL Commerce] 管理員，使用 _API金鑰_ 和 _使用者端密碼_ 產生於 [上一節][create-integration].

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Advanced]** 並選擇 **[!UICONTROL System]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** 並執行下列動作：

   - 設定 **[!UICONTROL Enabled Adobe Stock]** 至 `Yes`.

   - 輸入您的 **[!UICONTROL API Key (Client ID)]**.

   - 輸入您的 **[!UICONTROL Client Secret]**.

   - 按一下 **[!UICONTROL Test Connection]** 以驗證您的金鑰。

   ![進階設定 — Adobe Stock整合](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   提供驗證幾秒鐘。 如果您的認證有效，您應該會看到綠色 _連線成功！_ 訊息。

1. 完成後，按一下 **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
