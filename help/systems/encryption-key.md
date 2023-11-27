---
title: 加密金鑰
description: 瞭解如何自動產生或新增您自己的加密金鑰；您應定期變更此金鑰以提高安全性。
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# 加密金鑰

Adobe Commerce和Magento Open Source使用加密金鑰來保護密碼和其他敏感資料。 業界標準 [!DNL ChaCha20-Poly1305] 演演算法搭配256位元金鑰使用，以加密所有需要加密的資料。 這包括信用卡資料和整合（付款和運送模組）密碼。 此外，強式安全雜湊演演算法(SHA-256)可用來雜湊所有不需要解密的資料。

初始安裝期間，系統會提示您讓Commerce產生加密金鑰，或輸入您自己的金鑰。 加密金鑰工具可讓您視需要變更金鑰。 應定期變更加密金鑰以提高安全性，並且隨時可能危及原始金鑰。 每當金鑰變更時，所有舊資料都會使用新金鑰重新編碼。

如需技術資訊，請參閱 [進階內部部署安裝](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) 在 _安裝指南_.

## 步驟1：讓檔案可寫入

若要變更加密金鑰，請確定下列檔案是可寫入的： `[your store]/app/etc/env.php`

## 步驟2：變更加密金鑰

1. 在 _管理員_ 側欄，前往 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![系統加密金鑰](./assets/encryption-key.png){width="700" zoomable="yes"}

1. 執行下列任一項作業：

   - 若要產生新金鑰，請設定 **[!UICONTROL Auto-generate Key]** 至 `Yes`.
   - 若要使用不同的金鑰，請設定 **[!UICONTROL Auto-generate Key]** 至 `No`. 然後在 **[!UICONTROL New Key]** 欄位，輸入或貼上您要使用的金鑰。

1. 按一下 **[!UICONTROL Change Encryption Key]**.

1. 將新金鑰的記錄儲存在安全位置。

   如果檔案發生任何問題，則必須將資料解密。
