---
title: 『[!UICONTROL Customers] &gt； [!UICONTROL Gift Registry]『
description: 檢閱上的組態設定 [!UICONTROL Customers] &gt； [!UICONTROL Gift Registry] 商務管理員頁面。
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

如需有關使用這些設定為您的商店客戶啟用禮品登錄檔的詳細資訊，請參閱 [設定禮品登記簿](../../merchandising-promotions/gift-registry-configure.md). 如需在店面加入禮品註冊搜尋的相關資訊，請參閱 [新增贈品登入搜尋](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![一般選項](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | 存放區檢視 | 決定是否有禮品登記簿。 選項： <br/>**`Yes`**— 針對選取的商店檢視啟用禮品登記簿。 「贈品登入」標籤會出現在已註冊客戶的帳戶儀表板中。<br/>**`No`**  — 無法檢視商店的禮品登記簿。 |
| [!UICONTROL Maximum Registrants] | 存放區檢視 | 設定客戶可新增至禮品登入的人員數量。 客戶與每位註冊者共用贈品登入。 在店面， _新增註冊者_ 按鈕可供客戶使用，直到達到最大數量為止。 |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![所有者通知](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 存放區檢視 | 決定建立禮品登入時，所傳送之「擁有者通知」電子郵件所使用的範本。 預設範本：禮品登入擁有者通知 |
| [!UICONTROL Email Sender] | 存放區檢視 | 識別 [商店聯絡人](../../getting-started/store-details.md#store-email-addresses) 會顯示為「禮品註冊擁有者通知」電子郵件的寄件者。 預設值： `General Contact` |

{style="table-layout:auto"}

## 贈品登入共用

![贈品登入共用](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 存放區檢視 | 決定建立禮品登入時，用於傳送之「禮品登入共用」電子郵件的範本。 當擁有者按一下 _共用贈品登入_，則會傳送電子郵件給每位收件者。 預設範本： `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | 存放區檢視 | 識別 [商店聯絡人](../../getting-started/store-details.md#store-email-addresses) 會顯示為「贈品註冊共用」電子郵件的寄件者。 預設值： `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | 存放區檢視 | 一次可傳送的贈品註冊共用電子郵件通知訊息數上限。 |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![贈品登入更新](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 存放區檢視 | 決定當從禮品登入購買時，傳送給禮品登入擁有者的禮品登入更新電子郵件所使用的範本。 更新包含採購料號與數量的相關資訊，但不包含下訂單者的姓名。 預設範本： `Gift Registry Update` |
| [!UICONTROL Email Sender] | 存放區檢視 | 識別 [商店聯絡人](../../getting-started/store-details.md#store-email-addresses) 會顯示為「贈品註冊更新」電子郵件的寄件者。 預設值： `General Contact` |

{style="table-layout:auto"}
