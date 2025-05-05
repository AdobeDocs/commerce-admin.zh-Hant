---
title: 安全性掃描
description: 瞭解如何執行增強式安全性掃描，並監控每個Adobe Commerce和Magento Open Source網站。
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 1f3173d17cc43227f7d44637f1ef0b62606cd0fd
workflow-type: tm+mt
source-wordcount: '614'
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

安全性掃描工具可從您的[Commerce/Magento帳戶](../getting-started/commerce-account-create.md)的儀表板中免費取得。 如需技術資訊，請參閱&#x200B;_雲端基礎結構上的Commerce指南_&#x200B;中的[設定安全性掃描工具](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool)。

![安全性掃描工具](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## 執行安全性掃描

1. 從Commerce首頁，登入您的[Commerce/Magento帳戶](../getting-started/commerce-account-create.md)。

1. 檢閱並接受使用安全性掃描工具的條款。

   - 在左側面板中選擇&#x200B;**[!UICONTROL Security Scan]**。
   - 按一下&#x200B;**[!UICONTROL Go to Security Scan]**。
   - 讀取&#x200B;**[!UICONTROL Terms and Conditions]**。
   - 按一下&#x200B;**[!UICONTROL Agree]**&#x200B;以繼續。

1. 在&#x200B;_[!UICONTROL Monitored Websites]_&#x200B;頁面上，按一下&#x200B;**[!UICONTROL +Add Site]**。

   如果您有多個網站具有不同的網域，請為每個網域設定個別的掃描。

   ![監視的網站](./assets/monitored-website.png){width="600" zoomable="yes"}

1. 若要透過新增確認代碼來驗證您對網站網域的所有權，請執行下列任一項作業：

   **Commerce店面**：

   - 輸入&#x200B;**[!UICONTROL Site URL]**&#x200B;和&#x200B;**[!UICONTROL Site Name]**。
   - 按一下&#x200B;**[!UICONTROL Generate Confirmation Code]**。
   - 按一下&#x200B;**複製**，將確認代碼複製到剪貼簿。

     ![產生確認代碼](./assets/scan-site1.png){width="400" zoomable="yes"}

   - 以具有完整管理員許可權的使用者身分登入您商店的管理員，並執行下列動作：

      - 在&#x200B;_管理員_&#x200B;側邊欄中，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。
      - 在清單中尋找您的網站，然後按一下&#x200B;**[!UICONTROL Edit]**。
      - 展開&#x200B;**[!UICONTROL HTML Head]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。
      - 向下捲動至&#x200B;**[!UICONTROL Scripts and Style Sheets]**，然後按一下任何現有程式碼結尾的文字方塊，並將確認程式碼貼到文字方塊中。

        ![指令碼和樣式表](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - 完成時，按一下&#x200B;**[!UICONTROL Save Configuration]**。

   **PWA店面**：

   - 輸入&#x200B;**[!UICONTROL Site URL]**&#x200B;和&#x200B;**[!UICONTROL Site Name]**。

   - 針對&#x200B;**[!UICONTROL Confirmation Code]**，請選擇`META Tag`選項，然後按一下&#x200B;**[!UICONTROL Generate Code]**。

   - 按一下&#x200B;**[!UICONTROL Copy]**&#x200B;將產生的確認代碼META標籤複製到剪貼簿。

     ![產生確認代碼](./assets/scan-site2.png){width="400" zoomable="yes"}

   - 前往PWA Studio店面專案目錄，然後執行下列動作：

      - 在PWA Studio專案目錄下，移至`packages > venia-concept > template.html`。
      - 將複製的確認代碼（產生的META標籤）新增到HTML標題並儲存變更。

        ![複製確認代碼](./assets/code-pwa.png){width="600" zoomable="yes"}

      - 返回PWA StudioCLI，使用Wyar安裝專案相依性並執行專案建置命令。

        ```sh
        yarn install &&
        yarn build
        ```

      - *在您的雲端專案*&#x200B;中，建立`pwa`資料夾，並將內容複製到店面專案的`dist`資料夾中。

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

1. 返回Commerce帳戶中的&#x200B;_[!UICONTROL Security Scan]_&#x200B;頁面，然後按一下&#x200B;**[!UICONTROL Verify Confirmation Code]**&#x200B;以建立網域的所有權。

1. 成功確認後，為下列其中一種型別設定&#x200B;**[!UICONTROL Set Automatic Security Scan]**&#x200B;選項：

   **每週掃描（建議）**：

   - 選擇每週要執行掃描的&#x200B;**[!UICONTROL Week Day]**、**[!UICONTROL Time]**&#x200B;和&#x200B;**[!UICONTROL Time Zone]**。
   - 根據預設，掃描會排程每週的星期六午夜(UTC)開始，並持續到星期日凌晨。

     ![每週掃描](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **每日掃描**：

   - 選擇每天要執行掃描的&#x200B;**[!UICONTROL Time]**&#x200B;和&#x200B;**[!UICONTROL Time Zone]**。
   - 根據預設，掃描會排程在每天的午夜UTC開始。

     ![每日掃描](./assets/scan-daily.png){width="500" zoomable="yes"}

1. 輸入您想要接收已完成掃描和安全更新通知的&#x200B;**[!UICONTROL Email Address]**。

   ![電子郵件地址](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Submit]**。

   在驗證網域的所有權後，網站會顯示在您的Commerce帳戶的「受監控網站」清單中。

1. 如果您有多個網站具有不同的網域，請重複此程式，為每個網站設定安全性掃描。
