---
title: '[!UICONTROL Services] &amp；gt； [!UICONTROL Magento Web API]'
description: 檢閱Commerce管理員的[!UICONTROL Services] &amp；gt； [!UICONTROL Magento Web API]頁面上的組態設定。
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![SOAP設定](./assets/web-api-soap-settings.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | 存放區檢視 | 決定預設字元集。 如果為空，則使用UTF-8。 |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![GraphQl輸入限制](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | 存放區檢視 | 決定是否為GraphQL呼叫啟用輸入限制。 預設值： `No`。 |
| [!UICONTROL Maximum Page Size] | 存放區檢視 | 設定GraphQL回應中分頁搜尋結果允許的專案數上限。 當&#x200B;_啟用輸入限制_ = `No`時，此選項無法使用。 |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Web Api輸入限制](./assets/web-api-input-limits.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | 存放區檢視 | 判斷是否為Web API呼叫啟用輸入限制。 預設值： `No`。 |
| 輸入清單限制 | 存放區檢視 | 設定Web API要求中實體陣列屬性允許的專案數上限。 當&#x200B;_啟用輸入限制_ = `No`時，此選項無法使用。 |
| [!UICONTROL Maximum Page Size] | 存放區檢視 | 設定網頁API回應中分頁搜尋結果允許的專案數上限。 當&#x200B;_啟用輸入限制_ = `No`時，此選項無法使用。 |
| [!UICONTROL Default Page Size] | 存放區檢視 | 設定網頁API回應中分頁搜尋結果的預設專案數。 |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Web API安全性](./assets/web-api-security.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | 全域 | 決定來賓是否可以從SOAP和REST API匿名存取CMS、目錄和存放區資源。 依預設，不允許匿名訪客存取。 選項： `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![JWT驗證](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| 欄位 | [領域](../../getting-started/websites-stores-views.md#scope-settings) | 說明 |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | 全域 | 指定用於JWT （JSON Web權杖）加密的JWS或JWE演演算法型別 |
| [!UICONTROL Content encryption algorithm for JWEs] | 全域 | 指定在選取JWE演演算法時，用於JWT加密的內容加密演演算法型別。 JWS演演算法會忽略此選項。 |
| [!UICONTROL Customer JWT Expires In] | 全域 | 設定客戶JWT持有人權杖過期之前的時間長度（以分鐘為單位）。 如果此欄位空白或具有負值，則客戶JWT持有人權杖將在30分鐘後到期。 預設值： `60` |
| [!UICONTROL Admin User JWT Expires In] | 全域 | 設定Admin JWT持有人權杖過期之前的時間長度（以分鐘為單位）。 如果此欄位空白或具有負值，則管理員JWT持有人權杖將在30分鐘後到期。 預設值： `60` |

{style="table-layout:auto"}
