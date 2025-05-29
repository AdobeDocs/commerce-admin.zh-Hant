---
title: 安全性問題報告
description: 瞭解如何設定連絡資訊和安全性相關連結，讓安全性研究人員能夠報告您網站的安全性疑慮。
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案(Adobe管理的PaaS基礎結構)和內部部署專案的Adobe Commerce 。"
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# 安全性問題報告

`security.txt`檔案包含連絡資訊和安全性相關連結，安全性研究人員可使用這些連結來報告您網站的安全性顧慮。 如果您的安全性資訊會隨著時間而變更，請確定`security.txt`檔案中的資訊是最新的。

**_設定security.txt：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL Security]_&#x200B;下，按一下&#x200B;**[!UICONTROL Security.txt]**。

1. 在&#x200B;_[!UICONTROL General]_&#x200B;區段中，將&#x200B;**[!UICONTROL Enable]**&#x200B;設為`Yes`。

   ![一般安全性組態](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Contact Information]_&#x200B;下，輸入下列內容：

   - 處理您商店安全性問題的人員的電子郵件地址和電話號碼。

   - 您商店的&#x200B;**[!UICONTROL Contact Page]** URL。 此頁面可能是商店安全性連絡人的清單，或是您的&#x200B;_連絡我們_&#x200B;頁面。

   ![連絡資訊組態](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. 在&#x200B;_[!UICONTROL Other Information]_&#x200B;下，輸入下列內容：

   - 您的公開&#x200B;**[!UICONTROL Encryption]**&#x200B;金鑰的URL。 例如： `https://example.com/pgp-key.txt`

   - **[!UICONTROL Acknowledgments]**&#x200B;頁面的URL，在此頁面可識別安全性研究人員代表您商店所作出的努力。

   - 您用於安全性相關通訊的&#x200B;**[!UICONTROL Preferred Languages]**。 輸入每個支援語言的標準雙字元[語言代碼](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)，以逗號分隔。 例如，若要指定英文、西班牙文和法文，請輸入`en, es, fr`。 所有指定的語言都有相同的優先順序，無論其外觀順序為何。

   - **[!UICONTROL Hiring]**&#x200B;頁面的URL，此頁面列出您商店中與安全性相關的就業機會。

   - 您的安全性&#x200B;**[!UICONTROL Policy]**&#x200B;頁面的URL。

   - 儲存在伺服器上的數位&#x200B;**[!UICONTROL Signature]**&#x200B;檔案的URL。 例如： `https://mystore.com/.well-known/security.txt.sig`

   數位簽章必須從伺服器的CLI （命令列介面）設定。 若要深入瞭解，請參閱GitHub上的[Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md)。

   ![其他資訊](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
