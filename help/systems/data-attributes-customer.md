---
title: 客戶資料屬性參考
description: 當您處理客戶資料匯入和匯出時，請使用此客戶資料屬性參考。
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# 客戶資料屬性參考

下表列出客戶主要檔案和客戶地址典型匯出的屬性。 用來匯出此資料的安裝有兩個網站和多個存放區檢視，且已安裝範例資料。

每個屬性或欄位在CSV檔案中以欄的形式呈現，而客戶記錄則以列呈現。 以底線開頭的欄是包含屬性或複雜資料的服務實體。

## 客戶主檔案

| 屬性 | 說明 |
|--- |--- |
| `email` | 客戶的電子郵件地址。 |
| `_website` |  |
| `_store` |  |
| `confirmation` | 確認旗標。 |
| `created_at` | 建立客戶帳戶的日期。 |
| `created_in` | 建立帳戶的存放區檢視。 |
| `disable_auto_group_change` | 決定是否可在VAT ID驗證期間動態指派客戶群組。 |
| `dob` | 客戶的出生日期。 <br><br>**_重要：_**根據目前的安全性和隱私權最佳實務，檢閱客戶的完整出生日期（月、日、年）的儲存和處理。 與其他個人識別碼（例如_全名&#x200B;_）一起收集時，可能會有法律和安全風險。 我們建議限制客戶完整出生日期的儲存，而建議使用客戶出生年作為替代方法。 |
| `firstname` | 客戶的名字。 |
| `gender` | 客戶性別。 |
| `group_id` | 指派客戶的客戶群組ID。 |
| `lastname` | 客戶的姓氏。 |
| `middlename` | 客戶的中間名或中間首字母。 |
| `password_hash` | 密碼雜湊 |
| `prefix` | 任何與客戶名稱搭配使用的前置詞（例如`Mr.`、`Ms.`、`Mrs.`和`Dr.`）。 |
| `rp_token` | 重設密碼權杖。 |
| `rp_token_created_at` | 重設密碼的日期。 |
| `store_id` | 存放區ID |
| `suffix` | 任何與客戶名稱搭配使用的尾碼（例如`Jr.`、`Sr.`和`Esquire`）。 |
| `taxvat` |  |
| `website_id` | 建立客戶帳戶所在網站的網站ID。 |
| `password` | 客戶密碼。 |

{style="table-layout:auto"}

## 客戶地址

| 屬性 | 說明 |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | 客戶地址所在的城市。 |
| `company` | 適用於此地址的公司名稱。 |
| `country_id` | 客戶地址所在的國家/地區ID。 |
| `fax` | 客戶的傳真號碼（如適用）。 |
| `firstname` | 客戶的名字。 |
| `lastname` | 客戶的姓氏。 |
| `middlename` | 客戶的中間名或中間首字母。 |
| `postcode` | 客戶地址所在的郵遞區號。 |
| `prefix` | 任何與客戶名稱搭配使用的前置詞（例如`Mr.`、`Ms.`、`Mrs.`和`Dr.`）。 |
| `region` | 客戶地址所在的地區。 |
| `region_id` | 地區ID |
| `street` | 客戶的街道地址。 若在設定中指定，街道地址的第二行可以使用。 |
| `suffix` | 若已使用，則為與客戶名稱關聯的尾碼（例如`Jr.`、`Sr.`或`III`）。 |
| `telephone` | 客戶與地址相關聯的電話號碼。 |
| `vat_id` | VAT ID是用於「VAT驗證」時客戶「VAT編號」的內部識別碼。 |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | 識別預設帳單地址。 值`1`表示地址是客戶的預設帳單地址。 值： 1 / 0 |
| `_address_default_shipping_` | 識別預設送貨地址。 值`1`表示該地址是客戶的預設送貨地址。 值： `1` / `0` |

{style="table-layout:auto"}
