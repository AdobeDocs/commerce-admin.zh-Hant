---
title: 設定Visual Merchandiser的智慧屬性
description: 瞭解如何設定Visual Merchandiser使用的智慧屬性。
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/-6tbdpZ7L6nS1sIOXdk5Faxpkkt9qzqWhIjqp9MwgiM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 196
ht-degree: 0%

---

# 設定Visual Merchandiser的智慧屬性

{{ee-feature}}

「視覺化銷售器」組態決定了在銷售視窗中可使用的屬性，以及最小庫存臨界值。 此組態也會識別用於顏色的屬性以及顏色值的順序。

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Catalog]**&#x200B;並在下方選擇&#x200B;**[!UICONTROL Visual Merchandiser]**。

1. 展開&#x200B;**[!UICONTROL General Options]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![目錄組態 — 視覺化銷售工具](../configuration-reference/catalog/assets/catalog-visual-merchandiser-general-options.png){width="600" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Attributes for Category Rules]**&#x200B;清單中，選取您想要用於視覺化銷售的每個屬性。

   若要選取多個屬性，請按住Ctrl鍵(PC)或Command鍵(Mac)，然後按一下每個專案。

1. 輸入&#x200B;**[!UICONTROL Minimum Stock Threshold]**&#x200B;讓產品出現在Visual Merchandiser視窗中。

1. 輸入&#x200B;**[!UICONTROL Color Attribute Code]**。

   預設值為`color`。 如果您的目錄使用不同的屬性，請以小寫輸入屬性名稱。

1. 針對&#x200B;**[!UICONTROL Color Order]**，請在個別的列中依序輸入每個色彩值，以決定每個色彩的優先順序。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。
