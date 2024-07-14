---
title: 媒體 — 地圖
description: 瞭解用於將對應從 [!DNL Google Maps] 平台新增至 [!DNL Page Builder] 階段的Map內容型別。
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# 媒體 — 地圖

使用&#x200B;_對應_&#x200B;內容型別將對應從[[!DNL Google Maps] 平台][1]新增到[[!DNL Page Builder] 階段](workspace.md#stage)。 例如，您可以將地圖新增至區塊，然後將區塊新增至[關於我們](../content-design/pages.md#about-us)和[聯絡我們](../getting-started/store-details.md#contact-us-form)頁面。

若要充分利用[!DNL Google Maps] Platform，您可以自訂地圖、強調您的商店位置，並使用Google [Places][2]將您商店的豐富資訊新增到所有[!DNL Google Maps]。

## 內嵌Google地圖的好處

1. 直接在您的網站上為購買者提供您企業的完整資訊（電話號碼、網站、評論、星級評等資訊）。

1. Google地圖通常會醒目提示附近的景點、公園、餐廳等。 此資訊可協助您的客戶決定實際地點並計畫行程。

1. 讓客戶輕鬆找到實體商店的地址，無需開啟新的瀏覽器視窗並離開您的網站。

1. 如果您有一連串實體商店，在網站上新增Google Map有助於透過反白顯示的專案來提高您的品牌知名度和可信度。

![店面範例 — 與位置](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}對應

{{$include /help/_includes/page-builder-save-timeout.md}}

## 地圖工具箱

當您將滑鼠游標停留在地圖容器上時，地圖工具箱就會出現。

| 工具 | 圖示 | 說明 |
|--- |--- |--- |
| 移動 | ![移動圖示](./assets/pb-icon-move.png){width="25"} | 將地圖移至舞台上的另一個位置。 |
| （標籤） | [!UICONTROL Map] | 將目前的內容容器識別為對應。 將滑鼠懸停在地圖容器上可檢視工具箱。 |
| 設定 | ![設定圖示](./assets/pb-icon-settings.png){width="25"} | 開啟「編輯對映」頁面，您可以在此變更對映和容器的屬性。 |
| 隱藏 | ![隱藏圖示](./assets/pb-icon-hide.png){width="25"} | 隱藏目前的對應。 |
| 顯示 | ![顯示圖示](./assets/pb-icon-show.png){width="25"} | 顯示隱藏的地圖。 |
| 複製 | ![圖示重複](./assets/pb-icon-duplicate.png){width="25"} | 製作地圖副本。 |
| 移除 | ![移除圖示](./assets/pb-icon-remove.png){width="25"} | 從舞台刪除地圖。 |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 為您的管理員設定[!DNL Google Maps]

新增地圖之前，您必須先開啟[帳戶][3]以免費試用[!DNL Google Maps]平台。 免費試用期為12個月，包含$300的評分。 如果您用光了信用，Google不會在未經您許可的情況下為帳戶付費。

### 步驟1：取得您的[!DNL Google Maps] API金鑰

根據您是否已有[!DNL Google Maps]金鑰，請使用下列程式之一來取得設定所需的API金鑰。 若要設定[!DNL Google Maps]金鑰，您必須是獲授權為您的帳戶啟用帳單的網站管理員。 如果您尚未準備好設定[!DNL Google Maps]平台帳戶，您可以略過此步驟，暫時使用預留位置對應。

1. 前往[Google Cloud平台主控台](https://cloud.google.com/console/google/maps-apis/overview)。

1. 按一下專案下拉式清單，然後選取或建立您要新增API金鑰的專案。

1. 若要設定您的API認證，請依照[!DNL Google Maps]檔案中的[指示][4]操作。

1. 將API金鑰複製到剪貼簿。

### 步驟2：在[!DNL Commerce]中設定[!DNL Google Maps]

1. 在&#x200B;_管理員_&#x200B;側邊欄中，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_下，選擇&#x200B;**[!UICONTROL Content Management]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**。

   ![進階內容工具](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   如需有關內容管理進階工具組態選項的詳細資訊，請參閱[組態參考指南](../configuration-reference/general/content-management.md)。

1. 針對&#x200B;**[!UICONTROL Google Maps API Key]**，貼上您在步驟1中複製的金鑰。

1. 按一下&#x200B;**[!UICONTROL Test Key]**。

   如果您的金鑰發生問題，請返回[!DNL Google Maps]平台網站以解決問題。 然後再試一次。

1. 在驗證您的金鑰之後，按一下&#x200B;**[!UICONTROL Save Config]**。

## 將地圖新增至舞台

1. 開啟[!DNL Page Builder]工作區的頁面、區塊或動態區塊。

1. 在[!DNL Page Builder]面板中，展開&#x200B;**[!UICONTROL Media]**&#x200B;並將&#x200B;**[!UICONTROL Map]**&#x200B;預留位置拖曳到舞台。

   ![將地圖拖曳到舞台](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   如果為商店設定[!DNL Google Maps]平台，則會顯示商店位置的地圖。

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   如果尚未為您的存放區設定[!DNL Google Maps]平台，則會改為顯示預留位置對應。

   ![[!DNL Google Maps]預留位置](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## 新增自訂地圖位置

1. 將滑鼠懸停在地圖容器上以顯示工具箱，然後選擇&#x200B;_設定_ （ ![設定圖示](./assets/pb-icon-settings.png){width="20"} ）圖示。

1. 在&#x200B;_[!UICONTROL Edit Map]_頁面的右上角，按一下&#x200B;**[!UICONTROL Add Location]**。

1. 輸入您要在地圖上與pin碼關聯的&#x200B;**[!UICONTROL Location Name]**。

1. 收集您要用於自訂位置的位置座標。

   或者，您可以在&#x200B;**[!UICONTROL Position]**&#x200B;方塊中，拖曳顯示地圖中的圖釘。

   如有必要，請在新的瀏覽器視窗中移至[[!DNL Google Maps]][5]，並使用下列其中一種方法來取得座標：

   ![地圖座標](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **方法1：**&#x200B;從URL複製

   - 在左上角，在&#x200B;**[!UICONTROL Search]**&#x200B;方塊中輸入地址，然後按一下&#x200B;_搜尋_ （![搜尋圖示](../assets/icon-magnify-search.png){width="20"} ）圖示。

   - 複製URL中的座標，並將其貼到記事本中。

   **方法2：**&#x200B;從「這裡有什麼？」複製

   - 以滑鼠右鍵按一下標示地圖上位置的紅色圖釘，然後在功能表中選擇&#x200B;**[!UICONTROL What's here?]**。

   - 在顯示的標籤中，複製文字（包括座標），並將文字貼到記事本中。

1. 在每個&#x200B;**[!UICONTROL Coordinates]**&#x200B;方塊中輸入數字（不含逗號）。

   您也可以輸入要在地圖上可用的其餘資訊。

1. 競爭您要與地圖位置關聯的任何其他資訊：

   | 選項 | 說明 |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | 地點的電話號碼。 |
   | [!UICONTROL Street Address] | 地點的街道地址。 |
   | [!UICONTROL City] | 地點的城市。 |
   | [!UICONTROL Region/State] | 位置的區域或狀態。 |
   | [!UICONTROL Zip/Postal Code] | 地點的郵遞區號。 |
   | [!UICONTROL Country] | 地點的國家/地區。 |
   | [!UICONTROL Comment] | 您要包含的任何註解。 |

   {style="table-layout:auto"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save]**。

   新位置會顯示在地圖中，並出現在&#x200B;_[!UICONTROL Edit Map]_頁面上的地圖位置格線中。

   ![[!DNL Page Builder] — 對應位置格線](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## 設定地圖樣式 {#styling}

使用[!DNL Google Maps]平台樣式精靈套用六個預先定義主題之一或建立自訂主題。 您可以產生含有對應樣式屬性或樣式對映連結的JSON檔案。

### 變更地圖樣式

1. 在&#x200B;_管理員_&#x200B;側邊欄中，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_下，選擇&#x200B;**[!UICONTROL Content Management]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**。

1. 在&#x200B;**[!UICONTROL Google Maps Style]**&#x200B;文字方塊下，按一下[建立對應樣式][6]。

   此動作會在個別的索引標籤中開啟[[!DNL Google Maps] 平台樣式精靈][6]，您可以在此定義[!DNL Google Maps]平台專案的樣式。

1. 按一下「**[!UICONTROL Create a Style]**」，然後依照提供的指示進行。

   完成時，按一下&#x200B;**[!UICONTROL Finish]**。

1. 將完成的樣式匯出為JSON程式碼或URL，以便將其新增至[!DNL Commerce]設定。

   - **JSON**：在產生JSON程式碼的方塊底下，按一下&#x200B;**[!UICONTROL Copy JSON]**。

   - **[!UICONTROL URL]**：在產生之URL的方塊下方，按一下&#x200B;**[!UICONTROL Copy URL]**。

1. 返回您的[管理瀏覽器]索引標籤，並將產生的程式碼或URL貼到&#x200B;**Google地圖樣式**&#x200B;方塊中。

   如果您使用URL，請將`YOUR_API_KEY`預留位置取代為[!DNL Google Maps] API金鑰。 此URL會連結至您設定樣式的Google Map。

1. 按一下右上角的&#x200B;**[!UICONTROL Save Config]**。

### 變更地圖設定

1. 將滑鼠懸停在地圖容器上以顯示工具方塊，然後選擇&#x200B;_設定_ （ ![設定圖示](./assets/pb-icon-settings.png){width="20"} ）圖示。

1. 視需要變更基本設定：

   | 選項 | 說明 |
   | ------ | ----------- |
   | [!UICONTROL Height] | 指定所顯示地圖的高度（畫素）。 |
   | [!UICONTROL Show Controls] | 決定是否顯示標準Google Map控制項。 |

   {style="table-layout:auto"}

1. 視需要修改&#x200B;_[!UICONTROL Advanced]_設定：

   - 若要控制新增至容器的地圖內容的水平位置，請選擇&#x200B;**[!UICONTROL Alignment]**：

     | 選項 | 說明 |
     | ------ | ----------- |
     | `Default` | 套用目前佈景主題樣式表中指定的對齊預設設定。 |
     | `Left` | 將內容沿地圖容器的左邊框對齊，並允許指定的任何邊框間距。 |
     | `Center` | 對齊地圖容器中央的內容，並允許指定的任何邊框間距。 |
     | `Right` | 沿著地圖容器的右邊框對齊內容，並允許指定的任何邊框間距。 |

     {style="table-layout:auto"}

   - 設定套用至地圖容器所有四個側面的&#x200B;**[!UICONTROL Border]**&#x200B;樣式：

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

   - 如果您設定了`None`以外的框線樣式，請完成框線顯示選項：

     ![邊框顏色](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | 選項 | 說明 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 選擇色票、按一下檢色器，或輸入有效的顏色名稱或相等的十六進位值，以指定顏色。 |
     | [!UICONTROL Border Width] | 輸入邊框線條寬度的畫素數。 |
     | [!UICONTROL Border Radius] | 輸入畫素數目，以定義用來將邊框每個角落倒圓角的半徑大小。 |

     {style="table-layout:auto"}

   - （選擇性）從目前的樣式表中指定要套用至對應容器的&#x200B;**[!UICONTROL CSS classes]**&#x200B;名稱。

     以空格分隔多個類別名稱。

   - 輸入&#x200B;**[!UICONTROL Margins and Padding]**&#x200B;的值（以畫素為單位），以指定地圖容器的外部邊界和內邊距。

     在地圖容器圖表中輸入每個對應的值。

     | 容器區域 | 說明 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | 套用至容器所有側邊外部邊緣的空白空間量。 |
     | [!UICONTROL Padding] | 套用至容器所有邊內側邊緣的空白空間量。 |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >邊框間距不適用於「地圖」內容型別。

1. 完成後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;套用設定並返回[!DNL Page Builder]工作區。

### 變更格線大小

格線大小決定與[!DNL Page Builder]階段上[資料行](column.md)相關的地圖大小。 依預設，對應寬度為12欄，最多為16欄。

1. 在&#x200B;_管理員_&#x200B;側邊欄中，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 在左側面板的&#x200B;_[!UICONTROL General]_下，選擇&#x200B;**[!UICONTROL Content Management]**。

1. 展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**。

1. 視需要更新格線選項：

   >[!NOTE]
   >
   >如有需要，請清除&#x200B;**[!UICONTROL Use system value]**&#x200B;核取方塊以修改這些設定。

   - 針對&#x200B;**[!UICONTROL Default Column Grid Size]**，輸入格線預設大小的新值。

   - 針對&#x200B;**[!UICONTROL Maximum Column Grid Size]**，輸入預設格點大小上限的新值。

   ![資料行格線大小設定](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
