---
title: 客戶地址範本
description: 瞭解如何自訂客戶地址範本。
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# 客戶地址範本

{{ee-feature}}

您可以修改樣版，以控制列印的商業發票、出貨與退款以及客戶帳戶之地址簿中顯示的客戶帳單與出貨地址格式。 如果您想要包含其他資訊，您可以建立與客戶帳戶和[位址](address-attributes.md)相關聯的[自訂屬性](attribute-properties.md)，並將其合併到範本中。

## 範例1：短格式

針對[!UICONTROL Text One Line]位址範本：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## 範例2：長格式

針對[!UICONTROL Text]、[!UICONTROL HTML]和[!UICONTROL PDF]位址範本：

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![客戶地址範本](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## 變更位址列位的順序

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Customers]**&#x200B;並選取&#x200B;**[!UICONTROL Customer Configuration]**。

1. 按一下以展開&#x200B;**[!UICONTROL Address Templates]**&#x200B;區段。

   區段針對下列各項包含一組單獨的格式化指示：

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. 視需要編輯每個範本，並使用範例作為參考。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
