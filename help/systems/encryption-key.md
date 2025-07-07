---
title: 加密金鑰
description: 瞭解如何變更您自己的加密金鑰，這應該定期進行以提高安全性。
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 256517ebbbd6e28eb027f26c7f0a43001f5d7904
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# 加密金鑰

>[!NOTE]
>
>如果您嘗試完成這些步驟但發生問題，請參閱[疑難排解加密金鑰輪換： CVE-2024-34102](https://experienceleague.adobe.com/zh-hant/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102)知識庫文章。

Adobe Commerce和Magento Open Source使用加密金鑰來保護密碼和其他敏感資料。 產業標準[!DNL ChaCha20-Poly1305]演演算法搭配256位元金鑰使用，以加密所有需要加密的資料。 這包括信用卡資料和整合（付款和運送模組）密碼。 此外，強式安全雜湊演演算法(SHA-256)可用來雜湊所有不需要解密的資料。

初始安裝期間，系統會提示您讓Commerce產生加密金鑰，或輸入您自己的金鑰。 加密金鑰工具可讓您視需要變更金鑰。 應定期變更加密金鑰以提高安全性，並且隨時可能危及原始金鑰。

如需技術資訊，請參閱[安裝指南](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html?lang=zh-Hant)中的&#x200B;_進階內部部署_&#x200B;以及[PHP開發人員指南](https://developer.adobe.com/commerce/php/development/security/data-encryption/)中的&#x200B;_資料重新加密_。

>[!IMPORTANT]
>
>- 在依照這些指示變更加密金鑰之前，請確定下列檔案是可寫入的： `[your store]/app/etc/env.php`
>- 管理員設定中的加密金鑰變更功能已過時，並已在2.4.8中移除。升級至2.4.8之後，您必須使用本頁所述的CLI命令來變更加密金鑰。
>- 輪換加密金鑰將會立即讓所有客戶和管理層工作階段（不包括整合使用者）失效，並需要他們再次登入。

**若要變更加密金鑰：**

下列指示需要存取終端機。

1. 啟用[維護模式](https://experienceleague.adobe.com/zh-hant/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode)。

   ```bash
   bin/magento maintenance:enable
   ```

1. 停用cron工作。

   _雲端基礎結構專案：_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _內部部署專案_

   ```bash
   crontab -e
   ```

1. 使用下列其中一種方法變更加密金鑰。

   +++CLI命令

   執行下列CLI命令，並確定它完成時沒有錯誤。 如果您需要重新加密某些系統設定值或付款欄位，請參閱[PHP開發指南](https://developer.adobe.com/commerce/php/development/security/data-encryption/)中有關重新加密&#x200B;_的詳細_&#x200B;指南。

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++管理員設定

   >[!IMPORTANT]
   >
   >此功能已過時，並已在2.4.8版中移除。Adobe建議使用CLI變更加密金鑰。

   1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**。

      ![系統加密金鑰](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. 執行下列任一項作業：

      - 若要產生新金鑰，請將&#x200B;**[!UICONTROL Auto-generate Key]**&#x200B;設為`Yes`。
      - 若要使用其他金鑰，請將&#x200B;**[!UICONTROL Auto-generate Key]**&#x200B;設為`No`。 然後在&#x200B;**[!UICONTROL New Key]**&#x200B;欄位中輸入或貼上您要使用的金鑰。

   1. 按一下&#x200B;**[!UICONTROL Change Encryption Key]**。

      >[!NOTE]
      >
      >將新金鑰的記錄儲存在安全位置。 如果檔案發生任何問題，則必須將資料解密。

   +++

1. 排清快取。

   _雲端基礎結構專案：_

   ```bash
   magento-cloud cc
   ```

   _內部部署專案：_

   ```bash
   bin/magento cache:flush
   ```

1. 啟用cron工作。

   _雲端基礎結構專案：_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _內部部署專案：_

   ```bash
   crontab -e
   ```

1. 停用維護模式。

   ```bash
   bin/magento maintenance:disable
   ```
