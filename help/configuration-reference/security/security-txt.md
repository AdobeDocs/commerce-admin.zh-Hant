---
title: '[!UICONTROL Security] > [!UICONTROL Security.txt]'
description: 檢閱Commerce管理員的[!UICONTROL Security] &gt； [!UICONTROL Security.txt]頁面上的組態設定。
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
TQID: https://experienceleague.adobe.com/fXStEab1k6GKC5Tj7CStSGou3uNB-wJk5rZ-7EiFkcg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 360
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

如需有關變更這些組態設定的詳細資訊，請參閱[安全性問題報告](../../systems/security-issue-reporting.md)。

{{config}}

## [!UICONTROL General]

![一般](./assets/txt-general.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable] | 網站 | 啟用後，會儲存`security.txt`檔案，其中包含安全性研究人員回報您潛在漏洞所需的資訊。 選項：<br />**`Yes`**— 根據&#x200B;_連絡人資訊_與&#x200B;_其他資訊_區段中輸入的資訊，建立`security.txt`檔案。<br />**`No`** - （預設）不建立`security.txt`檔案。 |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![連絡資訊](./assets/txt-contact-info.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Email] | 網站 | 可傳送安全性報告的電子郵件地址。 |
| [!UICONTROL Phone] | 網站 | 可用來回報安全性問題的電話號碼。 |
| [!UICONTROL Contact Page] | 網站 | 網站上列出安全性連絡人的網頁URL，或您的&#x200B;_連絡我們_&#x200B;網頁。 範例： <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![其他資訊](./assets/txt-other-info.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Encryption] | 網站 | URL，指向安全性研究人員可用來傳送加密通訊的加密金鑰位置。 _**請勿在此欄位中輸入加密金鑰。**_ <br/><br/>研究人員有責任確認金鑰來自可靠的來源。 研究人員不得假設金鑰與用來產生數位簽名的金鑰相同。 範例：<br />來自網頁伺服器的OpenPGP金鑰 — `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | 網站 | URL會指向您商店中安全性研究人員獲得認可的頁面，例如`https://mystore.com/hall-of-fame.html`。 為了防止日後的攻擊，請僅包含一般說明，但不顯示有關漏洞問題的特定資訊。 範例：<br />我們要感謝以下研究人員：<br />(yyyy/mm/dd) Justin Thyme - SQL插入 |
| [!UICONTROL Preferred Languages] | 網站 | 指定至少一個偏好的安全性報告語言。 請使用逗號分隔多個雙字元[語言代碼](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)。 所有指定的語言都有相同的優先順序。 例如，若要指定英文、西班牙文和法文，請輸入`en, es, fr`。 |
| [!UICONTROL Hiring] | 網站 | 網站上列出安全性相關職位之頁面的URL。 範例： `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | 網站 | 說明您的安全性原則和弱點報告作法的頁面URL。 範例： `https://mystore.com/security-reporting.html`預設： `https://mystore.com/security` |
| [!UICONTROL Signature] | 網站 | 數位簽名檔案的連結。 數位簽章必須從命令列產生，並儲存在伺服器的`.well-known`資料夾中。 如需詳細資訊，請參閱GitHub上的[Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md)。 範例： `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
