---
title: 安全性掃描
description: 瞭解如何執行增強式安全性掃描，並監控每個Adobe Commerce和Magento Open Source網站。
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# 安全性掃描

增強式安全性掃描可讓您監視每個Adobe Commerce和Magento Open Source網站(包括PWA)，以瞭解已知的安全性風險和惡意程式，並接收修補程式更新和安全通知。

- 深入瞭解商店的即時安全性狀態。
- 根據最佳實務接收建議，以協助解決問題。
- 將安全性掃描排程為每週、每日或依需求執行。
- 執行超過21,000項安全性測試，協助識別潛在的惡意軟體。
- 存取追蹤及監控網站進度的歷史安全性報告。
- 存取顯示成功和失敗檢查的掃描報告，並附上任何建議的動作。

您可以從您的控制面板免費使用安全性掃描工具， [Commerce帳戶](../getting-started/commerce-account-create.md). 如需技術資訊，請參閱 [設定安全性掃描工具](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) 在 _雲端基礎結構上的Commerce指南_.

![安全性掃描工具](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## 執行安全性掃描

1. 前往Commerce首頁，然後登入您的 [Commerce帳戶](../getting-started/commerce-account-create.md) 並執行下列動作：

   - 在左側面板中，選擇 **[!UICONTROL Security Scan]**.
   - 按一下 **[!UICONTROL Go to Security Scan]**.
   - 閱讀 **[!UICONTROL Terms and Conditions]**.
   - 按一下 **[!UICONTROL Agree]** 以繼續。

1. 在 _[!UICONTROL Monitored Websites]_頁面，按一下&#x200B;**[!UICONTROL +Add Site]**.

   如果您有多個網站具有不同的網域，則必須為每個網域設定個別的掃描。

   ![受監視的網站](./assets/monitored-website.png){width="600" zoomable="yes"}

1. 若要透過新增確認代碼來驗證您對網站網域的所有權，請執行下列任一項作業：

   **Commerce店面**：

   - 輸入 **[!UICONTROL Site URL]** 和 **[!UICONTROL Site Name]**.
   - 按一下 **[!UICONTROL Generate Confirmation Code]**.
   - 按一下 **複製** 將確認代碼複製到剪貼簿。

     ![產生確認代碼](./assets/scan-site1.png){width="400" zoomable="yes"}

   - 以具有完整管理員許可權的使用者身分登入您商店的管理員，並執行下列動作：

      - 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - 在清單中找到您的網站，然後按一下 **[!UICONTROL Edit]**.
      - 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL HTML Head]** 區段。
      - 向下捲動至 **[!UICONTROL Scripts and Style Sheets]** 並按一下任何現有程式碼結尾的文字方塊，然後將確認程式碼貼入文字方塊。

        ![指令碼和樣式表](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - 完成後，按一下 **[!UICONTROL Save Configuration]**.

   **PWA店面**：

   - 輸入 **[!UICONTROL Site URL]** 和 **[!UICONTROL Site Name]**.

   - 的 **[!UICONTROL Confirmation Code]**，選擇 `META Tag` 選項，然後按一下 **[!UICONTROL Generate Code]**.

   - 按一下 **[!UICONTROL Copy]** 將產生的確認代碼META標籤複製到剪貼簿。

     ![產生確認代碼](./assets/scan-site2.png){width="400" zoomable="yes"}

   - 前往PWA Studio店面專案目錄，然後執行下列動作：

      - 在PWA Studio專案目錄下，前往 `packages > venia-concept > template.html`.
      - 將複製的確認代碼（產生的META標籤）新增到HTML標題並儲存變更。

        ![複製確認代碼](./assets/code-pwa.png){width="600" zoomable="yes"}

      - 返回PWA StudioCLI，使用Wyar安裝專案相依性並執行專案建置命令。

        ```sh
        yarn install &&
        yarn build
        ```

      - *在您的雲端專案中*，建立 `pwa` 資料夾並複製店面專案內的內容 `dist` 資料夾。

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - 使用Git CLI工具來暫存、提交這些變更，並將其推播至您的雲端專案。

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        建置流程完成後，變更將會部署至您的PWA存放區前端。

1. 返回 _[!UICONTROL Security Scan]_頁面，然後按一下&#x200B;**[!UICONTROL Verify Confirmation Code]**以建立您對網域的所有權。

1. 成功確認後，請設定 **[!UICONTROL Set Automatic Security Scan]** 下列其中一種型別的選項：

   **每週掃描（建議）**：

   - 選擇 **[!UICONTROL Week Day]**， **[!UICONTROL Time]**、和 **[!UICONTROL Time Zone]** 每週都會進行掃描。
   - 根據預設，掃描會排程每週的星期六午夜(UTC)開始，並持續到星期日凌晨。

     ![每週掃描](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **每日掃描**：

   - 選擇 **[!UICONTROL Time]**、和 **[!UICONTROL Time Zone]** 將會每天進行掃描。
   - 根據預設，掃描會排程在每天的午夜UTC開始。

     ![每日掃描](./assets/scan-daily.png){width="500" zoomable="yes"}

1. 輸入 **[!UICONTROL Email Address]** 您想要接收已完成掃描和安全更新通知的位置。

   ![電子郵件地址](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Submit]**.

   在驗證網域的所有權後，網站會顯示在您的Commerce帳戶的「受監控網站」清單中。

1. 如果您有多個網站具有不同的網域，請重複此程式，為每個網站設定安全性掃描。
