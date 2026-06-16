---
title: '[!UICONTROL Services] > [!UICONTROL OAuth]'
description: 檢閱Commerce管理員的[!UICONTROL Services] &gt； [!UICONTROL OAuth]頁面上的組態設定。
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/gwRxAaSnEul4D-LjjoGIcEiUCLl8ZrKjcSaMTvlGUKY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![存取權杖到期](./assets/oauth-token-expire.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | 全域 | 決定客戶API Token過期前的小時長度。 如果欄位為空，則客戶Token永不過期。 預設值： `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | 全域 | 決定管理API Token過期前的小時長度。 如果欄位為空，則管理Token永不過期。 預設值： `4` |

{style="table-layout:auto"}

>[!NOTE]
>
>持有者客戶和管理員API權杖期限和加密演演算法由[JWT驗證](magento-web-api.md#jwt-authentication)組態設定控制。

## [!UICONTROL Cleanup Settings]

![清理設定](./assets/oauth-cleanup.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | 全域 | 指定啟動清理前的OAuth要求數目。 請勿輸入`0`以停用清除。 |
| [!UICONTROL Enable WSDL Cache] | 全域 | 決定專案清除前的保留時間（分鐘）。 |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![消費者設定](./assets/oauth-consumer-settings.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | 全域 | 指定客戶張貼認證時，系統逾時所需的秒數。 |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | 全域 | 指定與公佈消費者認證相關的重新導向數目上限。 |
| [!UICONTROL Expiration Period] | 全域 | 決定OAuth權杖交換開始後，未使用的金鑰/密碼到期前的秒數。 |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![驗證鎖定](./assets/oauth-locks.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | 全域 | 指定鎖定帳戶的驗證失敗次數上限。 |
| [!UICONTROL Lockout Time (seconds)] | 全域 | 指定帳戶解除鎖定的時段（秒）。 |

{style="table-layout:auto"}
