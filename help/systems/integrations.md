---
title: 整合
description: 瞭解如何設定OAuth憑證和重新導向URL以進行協力廠商整合。
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# 整合

在Commerce管理員中定義整合，會建立OAuth憑證的位置和重新導向URL，用於第三方整合，並識別整合所需的可用API資源。 如需整合註冊程式的詳細資訊，請參閱Commerce開發人員檔案中的[OAuth型驗證](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/)。

![整合](./assets/integrations.png){width="700" zoomable="yes"}

## 入門工作流程

1. **授權整合** — 移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**&#x200B;頁面，尋找相關的整合併授權。
1. **驗證並建立登入** — 出現提示時，接受要求的存取。 如果重新導向至協力廠商，請登入系統或建立帳戶。 成功登入後，您會返回整合頁面。
1. **接收授權整合的確認** — 系統傳送整合已成功授權的通知。 設定整合併接收認證後，就不再需要呼叫存取或請求權杖。

## 新增整合

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**。

   ![新整合](./assets/integration-new.png){width="600" zoomable="yes"}

1. 輸入下列整合資訊：

   - 輸入整合的&#x200B;**[!UICONTROL Name]**&#x200B;和連絡人&#x200B;**[!UICONTROL Email]**&#x200B;位址。

   - 輸入&#x200B;**[!UICONTROL Callback URL]**，在使用OAuth進行權杖交換時，可在其中傳送OAuth認證。 強烈建議使用`https://`。

   - 輸入&#x200B;**[!UICONTROL Identity Link URL]**，使用這些Adobe Commerce或Magento Open Source整合認證將使用者重新導向至協力廠商帳戶。

   >[!NOTE]
   >
   > `Integration not secure`警告標籤會顯示在[!UICONTROL Integrations]格線上的每個整合名稱附近，以作為提醒，直到HTTPS URL儲存到[!UICONTROL Callback URL]和[!UICONTROL Identity Link URL]欄位中為止。

   - 出現提示時，請輸入您的密碼以確認您的身分。

1. 在左側面板中，選擇&#x200B;**[!UICONTROL API]**&#x200B;並執行下列動作：

   - 將&#x200B;**[!UICONTROL Resource Access]**&#x200B;設定為下列其中一項：

      - `All`
      - `Custom`

   - 對於自訂存取，請選取每個所需資源的核取方塊。

     ![整合 — 可用的API](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

## 啟用整合

依預設，已儲存的整合會顯示在狀態為`Inactive`的格線上。 若要啟用此功能，請完成下列步驟：

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**。

1. 尋找新建立的整合，然後按一下&#x200B;**[!UICONTROL Activate]**&#x200B;連結。

1. 按一下右上角的&#x200B;**[!UICONTROL Allow]**。

   此動作會顯示擴充功能的整合權杖。 將此資訊複製到安全的加密位置，以便與您的整合搭配使用。

   延伸功能的![整合權杖](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. 按一下右上角的&#x200B;**[!UICONTROL Done]**。

## 重新授權整合

若要產生新的整合存取權杖和存取權杖密碼，請從管理員重新授權整合：

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**。

1. 尋找與&#x200B;**[!UICONTROL Active]**&#x200B;狀態的整合。

1. 在&#x200B;_[!UICONTROL Activate]_&#x200B;欄中按一下&#x200B;**[!UICONTROL Reauthorize]**。

1. 按一下&#x200B;**[!UICONTROL Reauthorize]**&#x200B;以核准對API資源的存取權。

1. 儲存擴充功能的新整合權杖，然後按一下&#x200B;**[!UICONTROL Done]**。

## 變更API訪客存取安全性設定

依預設，系統不允許匿名訪客存取CMS、目錄和其他存放區資源。 如果您必須變更設定，請執行下列動作：

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Services]**&#x200B;並選擇&#x200B;**[!UICONTROL Magento Web API]**。

1. 展開&#x200B;**[!UICONTROL Web API Security Setting]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![服務組態 — Web API安全性設定](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. 將&#x200B;**[!UICONTROL Allow Anonymous Guest Access]**&#x200B;設為`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

如需詳細資訊，請參閱Commerce開發人員檔案中的[限制匿名網頁API的存取](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/)。

## 刪除整合

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**。

1. 尋找現有的整合，然後按一下&#x200B;**[!UICONTROL Delete]**&#x200B;欄中的圖示（ ![垃圾桶圖示](../assets/icon-delete-trashcan-solid.png) ）。

1. 若要確認您的動作，請按一下&#x200B;**[!UICONTROL OK]**。
