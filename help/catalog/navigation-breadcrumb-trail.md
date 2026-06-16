---
title: 階層連結追蹤
description: 瞭解不同的階層連結軌跡模式，以及如何設定這些模式，使其顯示在內容和目錄頁面上。
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
TQID: https://experienceleague.adobe.com/v1hA4y0MmxxTtH3WbspqosZM1JMk4PMyhK1xeLxALOE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 0%

---

# 階層連結追蹤

_階層連結路徑_&#x200B;是一組連結，可顯示客戶與商店中其他頁面的關聯位置。 他們可以按一下階層連結追蹤中的任何連結，以返回上一頁。

階層連結追蹤可設定為出現在內容頁面和目錄頁面上。 階層連結軌跡的格式和位置會依主題而有所不同，但通常位於標題的正下方。 依預設，階層連結軌跡會顯示在CMS頁面上。

店面中顯示的![階層連結路徑](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## 麵包屑的一般型別

階層連結可分為三種主要型別，其用途有所差異。 以下說明每種麵包屑實作的本質和主要原則。

### 階層式階層連結

此型別的階層連結是根據網站上設定的類別階層。 顯示的鏈結會告訴使用者它們在結構中的位置。 在此情況下，每個文字連結都適用於比上一個連結高一個層級的頁面。

範例： `Men > Tops > Hoodies & Sweatshirts`

這種型別的優點在於，使用者可以輕鬆檢視他們所在的類別層級，並輕鬆存取目錄頁面之間的導覽。

### 歷史記錄型階層連結

以歷程記錄（或路徑）為基礎的導覽類似於瀏覽器中的上一頁按鈕。 此型別的導覽可讓使用者快速返回先前造訪的頁面，而不會有任何變更。

此型別的好處是，當客戶在類別頁面上選取多個篩選器後，想要返回上一頁時，此型別最有幫助。

範例： `Home > What's New > Gear > Bags`

### 以屬性為基礎的階層連結

此型別的階層連結會顯示類別頁面上選取的屬性。 與其他型別的主要差異在於，以屬性為基礎的階層連結代表客戶為特定產品在導覽層中選擇的篩選器和選項（例如價格、品質和顏色）。

範例： `Home > Suits > All Suits > Refined by > Slim Fit`

## 從CMS頁面新增/移除階層連結

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_下，選擇&#x200B;**[!UICONTROL Web]**。

   ![顯示CMS頁面的階層連結](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. 展開&#x200B;_[!UICONTROL Default Pages]_區段。

1. 取消選取&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊。

1. 將&#x200B;**[!UICONTROL Show Breadcrumbs for CMS Pages]**&#x200B;設為`No`或`Yes`。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

>[!NOTE]
>
>當父類別具有`Browsing Category`= `Deny` [類別許可權](category-permissions.md)設定時，父類別不會顯示在子類別頁面的階層連結軌跡上。
