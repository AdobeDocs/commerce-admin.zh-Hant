---
title: 安全性問題報告
description: 瞭解如何設定連絡資訊和安全性相關連結，讓安全性研究人員能夠報告您網站的安全性疑慮。
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# 安全性問題報告

此 `security.txt` 檔案包含連絡資訊和安全性相關連結，安全性研究人員可使用這些連結來報告您網站的安全性顧慮。 如果您的安全性資訊會隨著時間而改變，請確定 `security.txt` 檔案是最新的。

**_若要設定security.txt：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中的 _[!UICONTROL Security]_，按一下&#x200B;**[!UICONTROL Security.txt]**.

1. 在 _[!UICONTROL General]_部分，設定&#x200B;**[!UICONTROL Enable]**至 `Yes`.

   ![一般安全性設定](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Contact Information]_，輸入下列內容：

   - 處理您商店安全性問題的人員的電子郵件地址和電話號碼。

   - 您商店的 **[!UICONTROL Contact Page]**. 此頁面可能是商店安全性連絡人的清單，或是 _聯絡我們_ 頁面。

   ![聯絡資訊設定](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. 在 _[!UICONTROL Other Information]_，輸入下列內容：

   - 您公用的URL **[!UICONTROL Encryption]** 機碼。 例如： `https://example.com/pgp-key.txt`

   - 的URL **[!UICONTROL Acknowledgments]** 此頁面可辨識安全研究人員為商店所做出的努力。

   - 您的 **[!UICONTROL Preferred Languages]** 安全性相關通訊。 輸入標準的兩個字元 [語言代碼](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) ，以逗號分隔。 例如，若要指定英文、西班牙文和法文，請輸入 `en, es, fr`. 所有指定的語言都有相同的優先順序，無論其外觀順序為何。

   - 的URL **[!UICONTROL Hiring]** 列出您商店中與安全性相關的就業機會的頁面。

   - 您安全性的URL **[!UICONTROL Policy]** 頁面。

   - 數位的URL **[!UICONTROL Signature]** 儲存在伺服器上的檔案。 例如： `https://mystore.com/.well-known/security.txt.sig`

   數位簽章必須從伺服器的CLI （命令列介面）設定。 若要深入瞭解，請參閱 [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) 在GitHub上。

   ![其他資訊](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.
