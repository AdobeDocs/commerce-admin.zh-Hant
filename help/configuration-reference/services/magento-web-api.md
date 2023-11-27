---
title: 『[!UICONTROL Services] &gt； [!UICONTROL Magento Web API]『
description: 檢閱上的組態設定 [!UICONTROL Services] &gt； [!UICONTROL Magento Web API] 商務管理員頁面。
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 5%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![SOAP設定](./assets/web-api-soap-settings.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | 存放區檢視 | 決定預設字元集。 如果為空，則使用UTF-8。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL GraphQl Input Limits]

![GraphQl輸入限制](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | 存放區檢視 | 決定是否為GraphQL呼叫啟用輸入限制。 預設值： `No`. |
| [!UICONTROL Maximum Page Size] | 存放區檢視 | 設定GraphQL回應中分頁搜尋結果允許的專案數上限。 此選項在以下情況下無法使用： _啟用輸入限制_ = `No`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Web Api Input Limits]

![Web Api輸入限制](./assets/web-api-input-limits.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | 存放區檢視 | 判斷是否為Web API呼叫啟用輸入限制。 預設值： `No`. |
| 輸入清單限制 | 存放區檢視 | 設定Web API要求中實體陣列屬性允許的專案數上限。 此選項在以下情況下無法使用： _啟用輸入限制_ = `No`. |
| [!UICONTROL Maximum Page Size] | 存放區檢視 | 設定網頁API回應中分頁搜尋結果允許的專案數上限。 此選項在以下情況下無法使用： _啟用輸入限制_ = `No`. |
| [!UICONTROL Default Page Size] | 存放區檢視 | 設定網頁API回應中分頁搜尋結果的預設專案數。 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Web API Security]

![Web API安全性](./assets/web-api-security.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | 全域 | 決定來賓是否可以從SOAP和REST API匿名存取CMS、目錄和存放資源。 依預設，不允許匿名訪客存取。 選項： `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL JWT Authentication]

![JWT驗證](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| 欄位 | [範圍](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | 全域 | 指定用於JWT （JSON Web權杖）加密的JWS或JWE演演算法型別 |
| [!UICONTROL Content encryption algorithm for JWEs] | 全域 | 指定在選取JWE演演算法時，用於JWT加密的內容加密演演算法型別。 JWS演演算法會忽略此選項。 |
| [!UICONTROL Customer JWT Expires In] | 全域 | 設定客戶JWT持有人權杖過期之前的時間長度（以分鐘為單位）。 如果此欄位空白或具有負值，則客戶JWT持有人權杖將在30分鐘後到期。 預設值： `60` |
| [!UICONTROL Admin User JWT Expires In] | 全域 | 設定Admin JWT持有人權杖過期之前的時間長度（以分鐘為單位）。 如果此欄位空白或具有負值，則管理員JWT持有人權杖將在30分鐘後到期。 預設值： `60` |

{:style=&quot;table-layout:auto&quot;}
