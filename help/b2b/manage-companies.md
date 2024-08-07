---
title: 公司管理
description: 簡化具有複雜作業模型的B2B組織的管理與管理。
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 公司管理

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="僅適用於Beta計畫參與者"}

公司管理可簡化具有複雜組織結構的公司的業務營運。 管理員使用者可以將公司指派給指定的母公司，藉此建立公司階層以映象B2B組織。 此指派可讓母公司管理員檢視及管理組織內的公司。

從&#x200B;*[!UICONTROL Companies]*&#x200B;檢視啟動公司管理工作。 從管理員移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。

![B2B管理公司網格](./assets/companies-grid-view.png){width="700" zoomable="yes"}

在&#x200B;*[!UICONTROL Companies grid]*&#x200B;中，*[!UICONTROL Company Type]*&#x200B;欄指出公司是作為組織的一部分進行管理，還是作為單獨的公司管理。

- `Parent`是擁有一或多個指派公司的企業組織。 母公司不能被指派為其他公司的子公司。

- `Child`是已指派給組織的公司。 公司只能指派給一家母公司。

- `Company`代表單一公司。 單一公司可以成為組織的一部分，方法是將其設為母公司，或將其指派給現有的母公司。

編輯父或子公司時，請展開&#x200B;*[!UICONTROL Company Hierarchy]*&#x200B;以檢視組織中的所有公司。 `Current`旗標表示您正在編輯的公司。

![B2B公司階層網格](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## 檢視並設定[!UICONTROL Company Hierarchy]

初次建立公司時，[!UICONTROL Company Hierarchy]格線是空的。 如果公司是單一公司，則此區域也是空的。

![B2B公司階層網格](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

對於母公司，具有適當許可權的Admin使用者可以完成以下工作：

- 藉由建立新的上階組織或更新現有的組織來建立公司階層。
- 管理現有組織以新增或移除公司。

如需詳細資訊，請參閱[管理公司階層](assign-companies.md)。
