---
title: 編輯受限制的存取金鑰
description: 重複使用的程式，用於編輯受限制的存取金鑰
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%
---
# 編輯受限制的存取金鑰

從目錄檢視指派或取消指派金鑰，而不是從主要[!UICONTROL Restricted Access Keys]格線。 您可以從共用目錄的&#x200B;_[!UICONTROL Catalog Views]_&#x200B;標籤或關聯公司的&#x200B;_[!UICONTROL Catalog Views]_&#x200B;區段進行此變更 — 兩者都會列出相同的目錄檢視和目前的索引鍵指派。

目錄檢視必須至少有一個索引鍵，而且最多可以有三個。 如果您嘗試指派第四個索引鍵，儲存會失敗，並出現一則訊息，通知您先移除一個索引鍵。

1. 使用下列其中一個路徑，開啟您要更新之目錄檢視的&#x200B;_[!UICONTROL Catalog Views]_&#x200B;格線：

   - _從共用目錄_ — 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**。 針對共用目錄，從&#x200B;**[!UICONTROL Action]**&#x200B;欄選取&#x200B;**[!UICONTROL General Settings]**。 然後，在&#x200B;_[!UICONTROL Shared Catalog Information]_&#x200B;面板中選取&#x200B;**[!UICONTROL Catalog Views]**。
   - _來自公司_ — 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Customers]** > **[!UICONTROL Companies]**。 針對公司，從&#x200B;**[!UICONTROL Action]**&#x200B;欄選取&#x200B;**[!UICONTROL Edit]**。 然後展開&#x200B;**[!UICONTROL Catalog Views]**&#x200B;區段。

   兩個網格都會列出為指定給公司的共用目錄所建立的目錄檢視，包括其指定的索引鍵。

1. 針對您要更新的目錄檢視選取&#x200B;**[!UICONTROL Edit Restricted Access Keys]**。

   ![編輯限制存取金鑰選擇器，顯示指派給目錄檢視的金鑰](/help/systems/assets/restricted-access-key-selector.png){width="500" zoomable="yes"}

1. 在&#x200B;**[!UICONTROL Access Keys]**&#x200B;欄位中，依[!UICONTROL Key ID]值選取未指派的索引鍵。

   已指派給不同目錄檢視的索引鍵會相應地加上標籤。

1. 選取&#x200B;**[!UICONTROL Done]**&#x200B;將金鑰指派給目錄檢視。

1. 若要從&#x200B;**[!UICONTROL Access Keys]**&#x200B;欄位中移除金鑰，請在金鑰名稱專案中選取`x`以將其移除。

1. 按一下&#x200B;**[!UICONTROL Save]**。
