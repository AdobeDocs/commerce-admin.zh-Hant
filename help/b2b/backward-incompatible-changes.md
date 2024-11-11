---
title: Adobe Commerce B2B與回溯不相容的變更
description: 瞭解Adobe Commerce B2B發行版本中的變更，這些變更可能需要您更新自訂程式碼。
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Adobe Commerce B2B與回溯不相容的變更

檢閱Adobe Commerce發行版本B2B中所有回溯不相容變更的高階參考資訊。 請參閱醒目提示一節，瞭解具有重大影響的不相容變更，以及需要詳細說明和特殊指示的變更。

## 反白顯示

### 1.4.2至1.5.0

加入多公司指派後，公司使用者帳戶現在可以有多個`company_id`值。 已更新`Magento\Company\Api\Data\CompanyCustomerInterface`以設定使用者的預設`company_id`。 預設值設為指派給公司使用者帳戶的第一個公司。

如果您要從舊版升級，Adobe建議您在使用`Magento\Company\Api\Data\CompanyCustomerInterface`的類別中實作下列方法。

- Magento\Company\Api\Data\CompanyCustomerInterface：：getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface：：setIsDefault

## 參考

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
