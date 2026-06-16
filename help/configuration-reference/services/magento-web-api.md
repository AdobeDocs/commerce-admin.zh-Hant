---
title: '[!UICONTROL Services] > [!UICONTROL Magento Web API]'
description: 檢閱Commerce管理員的[!UICONTROL Services] &gt； [!UICONTROL Magento Web API]頁面上的組態設定。
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
TQID: https://experienceleague.adobe.com/62cy3cPVxGeI-W1LElSg1TEBEb0cZN30vGZQ74UNhm8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
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
