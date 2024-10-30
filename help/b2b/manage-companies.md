---
title: 公司管理
description: 簡化具有複雜作業模型的B2B組織的管理與管理。
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# 公司管理

公司管理可簡化具有複雜組織結構的公司的業務營運。 管理員使用者可以將公司指派給指定的母公司，藉此建立公司階層以映象B2B組織。 此指派可讓母公司管理員檢視及管理組織內的公司。

從&#x200B;*[!UICONTROL Companies]*&#x200B;檢視啟動公司管理工作。 從管理員移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

![B2B管理公司網格](./assets/companies-grid-view.png){width="700" zoomable="yes"}

*[!UICONTROL Company Type]*&#x200B;欄指出公司是作為組織的一部分進行管理，還是作為單獨的公司管理。

- `Parent`是擁有一或多個指派公司的企業組織。 母公司不能被指派為其他公司的子公司。

- `Child`是已指派給組織的公司。 公司只能指派給一家母公司。

- `Company`代表單一公司。 單一公司可以成為組織的一部分，方法是將其設為母公司，或將其指派給現有的母公司。

編輯父或子公司時，請展開&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;以檢視組織中的所有公司。 `Current`旗標表示您正在編輯的公司。

![B2B公司階層網格](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## 檢視並設定[!UICONTROL Company Hierarchy]

初次建立公司時，*[!UICONTROL Company Hierarchy]*&#x200B;格線是空的。 如果公司是單一公司，則此區域也是空的。

![B2B公司階層網格](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

如果公司是組織的母公司，且組織中其他公司的公司帳戶已在Adobe Commerce中設定，則具有適當許可權的管理員使用者可以指派公司，並使用&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;網格完成其他公司管理任務：

- 檢視與母公司相關聯的所有公司。
- 從母公司詳細資料頁面，將更多公司指派給組織。
- 使用&#x200B;*[!UICONTROL Unassign from parent]*&#x200B;動作從組織中移除公司。
- 更新&#x200B;*[!UICONTROL Advanced Settings]*&#x200B;設定以將相同的設定套用至多個公司。

如需詳細指示，請參閱[管理公司階層](manage-company-hierarchy.md)。

