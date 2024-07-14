---
title: 隱藏類別
description: 瞭解如何將隱藏的類別用於內部用途，或連結至未包含在導覽功能表中的類別。
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# 隱藏類別

有許多方式可使用隱藏的類別。 您可能會想要針對自己的內部目的建立額外的類別層級，但只對客戶顯示較高層級的類別。 或者，您可能會想要連結至未包含在導覽功能表中的類別。

## 建立隱藏類別

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Categories]**。

1. 在類別樹狀結構中，選取要隱藏的類別，然後執行下列動作：

   - 將&#x200B;**[!UICONTROL Is Active]**&#x200B;設為`Yes`。
   - 將&#x200B;**[!UICONTROL Include in Menu]**&#x200B;設為`No`。

1. 在&#x200B;**[!UICONTROL Display Settings]**&#x200B;區段中，將&#x200B;**[!UICONTROL Anchor]**&#x200B;設為`No`。

   ![隱藏的類別](./assets/hidden-categories.png){width="600" zoomable="yes"}

   隱藏的類別處於作用中狀態，但不會顯示在頂端功能表或圖層導覽中。

1. 為每個隱藏的子類別完成以下設定以建立子類別：

   >[!NOTE]
   >
   >雖然類別已隱藏，但您可以在其下方建立子類別，並將其設為使用中。

   - 將&#x200B;**[!UICONTROL Enable Category]**&#x200B;設為`Yes`。
   - 在&#x200B;**[!UICONTROL Display Settings]**&#x200B;區段中，將&#x200B;**[!UICONTROL Anchor]**&#x200B;設為`Yes`。

   身為作用中類別，您現在可以從商店的其他位置連結至這些類別，但它們不會出現在功能表中。

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。
