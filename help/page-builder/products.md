---
title: 新增內容 — 產品
description: 瞭解產品內容型別，用於新增產品清單至 [!DNL Page Builder] 階段。
exl-id: 8ef38669-a6f6-493b-b963-b0fc4e3bbff4
feature: Page Builder, Page Content, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1913'
ht-degree: 0%

---

# 新增內容 — 產品

使用&#x200B;_Products_&#x200B;內容型別，以格線或轉盤版面配置將產品清單新增至[[!DNL Page Builder] 階段](workspace.md#stage)。 使用[新增內容 — 區塊](block.md)工具將區塊放在[!DNL Page Builder]舞台上，然後將產品清單放在區塊內。 或者，您可以直接在頁面上的列中新增產品清單。

## 使用產品輪播的准則

產品輪播提供強大且吸引人的方式，展示您的產品。 若要充分運用此功能，建議遵循下列准則：

- 將產品輪播直接新增至頁面寬度容器，例如列、索引標籤或一欄式版面。 使用頁面寬度版面配置可確保產品的最佳回應式顯示。 [!DNL Page Builder]會根據頁面寬度而非容器寬度來減少顯示的產品數量。

- 請勿將產品輪播新增至窄欄。 如前所述，[!DNL Page Builder]預設會根據頁面寬度（而非欄寬）決定要顯示的產品數量。

- 如果您希望產品輪播持續自動捲動，請將&#x200B;**[!UICONTROL Autoplay]**&#x200B;和&#x200B;**[!UICONTROL Infinite Loop]**&#x200B;設定為`Yes`。 如果「自動播放」設定為`Yes`，但「無限回圈」設定為`No`，則自動捲動會在產品清單的結尾停止。

- 將&#x200B;**[!UICONTROL Carousel Mode]**&#x200B;設為`Continuous`，以在轉盤中一次反白、置中和捲動一個產品。 其他產品在清單中是可見的，但為反白顯示置中的產品，則為透明。

  ![處於連續輪播模式的產品清單](./assets/pb-products-settings-carousel-continuous.png){width="600"}

- 若要在轉盤中一次顯示和捲動最多五個產品，請將&#x200B;**[!UICONTROL Carousel Mode]**&#x200B;設定為`Default`。

  ![預設轉盤模式下的產品清單](./assets/pb-products-settings-carousel-default.png){width="600"}

下列指示顯示如何將產品清單新增至區塊。 然後您可以使用[Widget](../content-design/widgets.md)，將區塊放置在商店中任何頁面上的特定位置。

{{$include /help/_includes/page-builder-save-timeout.md}}

## 產品工具箱

| 工具 | 圖示 | 說明 |
| --------- | ------------- | ----------------- |
| 移動 | ![移動圖示](./assets/pb-icon-move.png){width="25"} | 將產品容器及其內容移至舞台上的另一個位置。 |
| 設定 | ![設定圖示](./assets/pb-icon-settings.png){width="25"} | 開啟&#x200B;_編輯產品_&#x200B;頁面，您可以在其中選擇產品清單並變更容器的屬性。 |
| 隱藏 | ![隱藏圖示](./assets/pb-icon-hide.png){width="25"} | 隱藏目前的產品容器及其內容。 |
| 顯示 | ![顯示圖示](./assets/pb-icon-show.png){width="25"} | 顯示隱藏的產品容器及其內容。 |
| 複製 | ![圖示重複](./assets/pb-icon-duplicate.png){width="25"} | 製作產品容器及其內容的副本。 |
| 移除 | ![移除圖示](./assets/pb-icon-remove.png){width="25"} | 從階段刪除產品容器及其內容。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 建立產品清單區塊

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**。

1. 按一下&#x200B;**[!UICONTROL Add New Block]**。

1. 輸入&#x200B;**[!UICONTROL Block Title]**&#x200B;和&#x200B;**[!UICONTROL Identifier]**。

1. 選擇要提供區塊的&#x200B;**[!UICONTROL Store View]**。

1. 向下捲動並按一下&#x200B;**[!UICONTROL Edit with Page Builder]**&#x200B;或在內容預覽區域內以開啟[!DNL Page Builder]工作區。

1. 在[!DNL Page Builder]面板中，展開&#x200B;**[!UICONTROL Add Content]**&#x200B;並將&#x200B;**[!UICONTROL Products]**&#x200B;預留位置拖曳到舞台。

   ![新增產品內容型別](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

## 設定產品清單容器

將滑鼠停留在空的&#x200B;_Products_&#x200B;容器上以顯示工具箱，然後按一下&#x200B;_設定_ （![設定圖示](./assets/pb-icon-settings.png){width="20"} ）圖示。

![產品工具箱](./assets/pb-add-content-products-toolbox.png){width="500" zoomable="yes"}

根據下列章節完成&#x200B;_設定_：

### 外觀

1. 若要決定產品清單在頁面上的顯示方式，請選擇其中一個外觀型別：

   | 型別 | 說明 |
   | ---- | ----------- |
   | 產品格線 | 顯示網格中的產品，每列顯示五個產品（預設值），所需列數即為顯示以&#x200B;**[!UICONTROL Number of Products to Display]**&#x200B;設定輸入之數字所需的列數。 |
   | 產品輪播 | 顯示輪播中的產品（也稱為滑桿）。 每張投影片最多可顯示五個產品。 <br/><br/>**回應性警示**：選取此外觀時，最好直接將「產品」內容型別新增到有回應的列、標籤或一欄版面配置中，在較小的熒幕上每側顯示較少產品。 如果將其新增至寬度小於頁面寬度的內容型別（例如窄欄），則無論熒幕大小，輪播每張投影片顯示的產品都會超過容器允許的數目。 |

   {style="table-layout:auto"}

   ![產品外觀](./assets/pb-products-appearances.png){width="300"}

   如果您選擇產品輪播，您也必須設定[輪播設定](#carousel-settings)。

1. 針對&#x200B;**[!UICONTROL Select Products By]**，選擇產品選擇方法：

   您可以依類別、SKU或條件選取產品。 這些選項互斥。 例如，您無法選取「類別」選項、使用「類別」選取器，然後切換至「條件」選項以新增部分條件。 您的產品只會根據您為這三個選項中的&#x200B;_一個_&#x200B;設定的專案來選取。

   - **[!UICONTROL Category]** — 選擇此選項可顯示使用所選類別的產品。

     ![依類別的產品選擇](./assets/pb-products-settings_category.png){width="500"}

     選取此選項時，會提供&#x200B;**[!UICONTROL Category]**&#x200B;選取器。 按一下箭頭，然後向下展開以選擇要顯示的產品類別。 例如，在[!DNL Commerce]範例資料中，鑽研並選取&#x200B;_女性>上衣> Tes_&#x200B;會顯示該類別的所有產品。

     ![選取目錄類別](./assets/pb-select-products-by-category.png){width="500"}

   - **[!UICONTROL SKU]** — 選擇此選項以顯示使用一或多個SKU的產品

     選取時，此選項會提供&#x200B;**[!UICONTROL Product SKUs]**&#x200B;文字方塊，您必須在此輸入要顯示的SKU清單（以逗號分隔）。

     ![依SKU的產品選擇](./assets/pb-products-settings_sku.png){width="500"}

   - **[!UICONTROL Condition]** — 選擇此選項可根據您定義的一或多個條件顯示產品。

     選取時，會有工具可新增條件至您的產品選擇。 例如，您只能選取「性別」設為Unisex的產品。

     ![依據條件的產品選擇](./assets/pb-products-settings_condition.png){width="500"}

     >[!NOTE]
     >
     >選取類別或SKU選項會提供&#x200B;**[!UICONTROL Sort By]**&#x200B;的`Position`選項。 使用此排序選項，產品會以它們在目錄中出現的相同順序顯示。</br>
     >
     >在「類別」選項中，依位置排序會以產品在目錄中顯示的相同順序顯示產品。 針對SKU選項，依位置排序會依照您在&#x200B;**[!UICONTROL Product SKUs]**&#x200B;文字方塊中輸入產品的順序顯示產品。

1. 針對&#x200B;**[!UICONTROL Sort By]**，選擇清單中產品的排序順序：

   | 選項 | 說明 |
   | ------ | ----------- |
   | `Position` （僅適用於類別和SKU選項） | 當您選取「類別」選項時，「位置」會以產品在目錄中的位置相同順序顯示產品。 當您選取SKU選項時，「位置」會以與「產品SKU」文字方塊中的SKU相同的順序顯示產品。 |
   | `Newest products first` | 依產品加入目錄的日期來排序產品，先顯示具有最近輸入日期的產品。 |
   | `Oldest products first` | 依產品加入目錄的日期來排序產品，先顯示具有最早輸入日期的產品。 |
   | `Name: A - Z` | 依字母順序排序產品。 |
   | `Name: Z - A` | 以反向字母順序排序產品。 |
   | `SKU: ascending` | 依SKU以英數字元順序排序產品。 |
   | `SKU: descending` | 依SKU以反向英數字元順序排序產品。 |
   | `Stock: low stock first` | 將產品從最低庫存排序到最高庫存。 |
   | `Stock: high stock first` | 將產品從最高庫存排序到最低庫存。 |
   | `Price: high to low` | 從最高價到最低價排序產品。 |
   | `Price: low to high` | 從最低價格到最高價格排序產品。 |

   {style="table-layout:auto"}

   ![產品排序選項](./assets/pb-products-sortby.png){width="300"}

1. 在轉盤或格線中輸入&#x200B;**[!UICONTROL Number of Products to Display]**。

   值可以從`1`到`999`。 格線的預設值為`5`，轉盤預設值為`20`。

   >[!NOTE]
   >
   >類別、SKU或條件設定中的某些產品可能不會顯示在產品格線或轉盤中。 例如，停用的產品、標籤為不可見的產品、無庫存的產品以及指派給其他網站的產品不會顯示。

   >[!IMPORTANT]
   >
   >可設定、分組和套件式（動態價格）產品的價格在Admin中未定義。 因此，如果產品是依價格篩選，則不會在&#x200B;**[!UICONTROL Preview]**&#x200B;中顯示這些產品。 如果依價格訂購，則無法在&#x200B;**[!UICONTROL Preview]**&#x200B;中正確訂購這些產品。

### 輪播設定

1. 若要決定產品在轉盤中的顯示方式，請選擇&#x200B;**[!UICONTROL Carousel Mode]**：

   | 選項 | 說明 |
   | ------ | ----------- |
   | `Default` | 依預設，輪播會每張投影片顯示五個產品，並依需求回應式減少產品數量。 |
   | `Continuous` | 依預設，輪播會每張投影片顯示五個產品（一半產品在右側和左側），但一次會以無限回圈的方式中心並捲動一個產品。 置中產品的左右兩側產品會變暗，使置中產品反白。 |

   {style="table-layout:auto"}

   如果您在這兩種模式之間切換，則會保留其他轉盤設定，但&#x200B;**[!UICONTROL Infinite Loop]**&#x200B;設定除外，該設定一律設定為「連續」模式的`Yes`，且欄位已停用。

   ![轉盤設定](./assets/pb-products-carousel-settings.png){width="600" zoomable="yes"}

1. 如有需要，請將&#x200B;**[!UICONTROL Autoplay]**&#x200B;選項設定為`Yes`。

   啟用自動播放時，轉盤會在頁面載入時自動開始捲動。 如果您保留預設設定(`No`)，客戶必須按一下幻燈片導覽（點或箭頭）來依序顯示每張幻燈片。

   如果您啟用此功能，請輸入&#x200B;**[!UICONTROL Autoplay Speed]**&#x200B;以指定每張投影片之間的延遲時間（毫秒）。 預設值為`4000` （4秒）。

1. 如有需要，請將&#x200B;**[!UICONTROL Infinite Loop]**&#x200B;選項設定為`Yes`。

   啟用無限回圈時，幻燈片會在頁面開啟時無限期重播。 如果您保留預設設定(`No`)，幻燈片放映只會播放一次。

   >[!NOTE]
   >
   >如果您將&#x200B;**[!UICONTROL Infinite Loop]**&#x200B;設為`No`，並將&#x200B;**[!UICONTROL Autoplay]**&#x200B;設為`Yes`，則自動播放會在要顯示的產品數目結束時停止。

1. 如有需要，請將&#x200B;**[!UICONTROL Show Arrows]**&#x200B;選項設定為`Yes`。

   啟用此選項時，每張投影片都包含&#x200B;_下一個_&#x200B;和&#x200B;_上一個_&#x200B;左右方向的導覽箭頭。 如果您保留預設設定(`No`)，幻燈片不會顯示導覽箭頭。

1. 如有需要，請將&#x200B;**[!UICONTROL Show Dots]**&#x200B;選項設定為`No`。

   當設定為預設設定(`Yes`)時，導覽點會出現在轉盤滑桿底部。 如果停用此設定，轉盤滑桿就不會顯示導覽點。

### 進階

1. 若要控制產品清單在父容器中的位置，請選擇&#x200B;**[!UICONTROL Alignment]**：

   | 選項 | 說明 |
   | ------ | ----------- |
   | `Default` | 套用目前佈景主題樣式表中指定的對齊預設設定。 |
   | `Left` | 沿著父容器的左邊框對齊清單，並允許指定的任何邊框間距。 |
   | `Center` | 將清單對齊父項容器的中心，並容許任何指定的內距。 |
   | `Right` | 沿著父容器的右邊框對齊清單，並允許指定的任何邊框間距。 |

   {style="table-layout:auto"}

1. 設定套用至「產品」容器所有四個側面的&#x200B;**[!UICONTROL Border]**&#x200B;樣式：

   | 選項 | 說明 |
   | ------ | ----------- |
   | `Default` | 套用關聯樣式表所指定的預設邊框樣式。 |
   | `None` | 未提供任何容器框線的可見指示。 |
   | `Dotted` | 容器邊框會以虛線顯示。 |
   | `Dashed` | 容器邊框會以虛線顯示。 |
   | `Solid` | 容器邊框會以實線顯示。 |
   | `Double` | 容器邊框會以雙線顯示。 |
   | `Groove` | 容器框線會顯示為槽線。 |
   | `Ridge` | 容器框線會顯示為脊線。 |
   | `Inset` | 容器框線會顯示為內嵌線。 |
   | `Outset` | 容器邊框會顯示為外線。 |

   {style="table-layout:auto"}

1. 如果您設定了`None`以外的框線樣式，請完成框線顯示選項：

   | 選項 | 說明 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 選擇色票、按一下檢色器，或輸入有效的顏色名稱或相等的十六進位值，以指定顏色。 |
   | [!UICONTROL Border Width] | 輸入邊框線條寬度的畫素數。 |
   | [!UICONTROL Border Radius] | 輸入畫素數目，以定義用來將邊框每個角落倒圓角的半徑大小。 |

   {style="table-layout:auto"}

1. （選擇性）從目前的樣式表中指定要套用至容器的&#x200B;**[!UICONTROL CSS classes]**&#x200B;名稱。

   以空格分隔多個類別名稱。

1. 輸入&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;的值（以畫素為單位），以決定「產品」容器的外部邊界與內部邊距。

   在圖表中輸入對應的值。

   | 容器區域 | 說明 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | 套用至容器所有側邊外部邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | 套用至容器所有邊內側邊緣的空白空間量。 選項： `Top` / `Right` / `Bottom` / `Left` |


## 在舞台上儲存並預覽

在右上角，按一下&#x200B;**[!UICONTROL Save]**&#x200B;以套用設定並返回[!DNL Page Builder]工作區。

如果您已設定產品輪播，看起來應該類似下列範例：

![在舞台上的產品輪播](./assets/pb-products-admin-carousel.png){width="600"}

您現在可以使用[Widget](../content-design/widgets.md)，將此區塊置於您想要其顯示在市集內的任何位置。 或者，您可以使用[Add Content - Block](block.md)，將區塊新增至現有的頁面、索引標籤或區塊。

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
