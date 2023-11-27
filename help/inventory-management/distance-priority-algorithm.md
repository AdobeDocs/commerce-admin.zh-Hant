---
title: 設定距離優先順序演演算法
description: 設定組態以比較出貨目的地地址的地點與來源地點，以決定最接近完成出貨的來源。
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# 設定距離優先順序演演算法

「距離優先順序演演算法」會比較出貨目的地地址的地點與來源地點，以決定最接近完成出貨的來源。 這個距離可能是由實際距離或從一個位置到另一個位置旅行的時間所決定，使用資料庫資料或駕駛、步行或騎腳踏車的方向。 使用此 [來源選擇演演算法](selection-reservations.md) 建議與出貨目的地地址最接近的來源。

>[!NOTE]
>
>如果您使用「距離優先順序演演算法」，請輸入您的完整街道位址和GPS座標 [來源](sources-add.md) 建議使用。

您有兩個選項可以計算距離和時間，以找出最接近出貨履行情況的來源：

- **GOOGLE MAP**  — 使用 [Google Maps平台][1] 服務，用於計算送貨目的地地址與來源地點之間的距離與時間。 此選項會使用來源的經緯度（GPS座標），而且可能會根據計算模式使用街道地址。 Google API金鑰為必填，與 [地理編碼API][2] 和 [距離矩陣API][3] 已啟用，您可能會透過Google產生費用。

- **離線計算**  — 使用下載和匯入的地理碼資料，利用郵遞區號和GPS座標，計算距離，以判斷最接近出貨目的地地址的來源。 若要設定此選項，您可能需要開發人員協助，才能使用命令列指示先下載及匯入地理代碼。

>[!NOTE]
>
>若為具有多個國家/地區的多商店網站，請設定 [預設稅捐目的地](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"} 適用於每個國家/地區。

## 使用Google地圖

您不需要Google帳戶即可開始使用。 此程式包括視需要建立Google帳戶和專案。 此選項需要新增計費帳戶和付款方法至您的Google帳戶，以完成設定並使用演演算法。
不過，我們建議使用Google MAP距離型演演算法，此演演算法較離線計算更進階且更精確。

### 步驟1：建立Google API金鑰

索引鍵是來自 [Google Maps平台][1] 而且應該有 [地理編碼API][2] 和 [距離矩陣API][3] 已啟用。 如需詳細資訊，請參閱 [設定距離優先順序演演算法](distance-priority-algorithm.md).

1. 造訪 [Google Maps平台][1] 並按一下 **[!UICONTROL Get Started]**.

1. 若要啟用平台，請選取 **[!UICONTROL Maps, Routes, and Places]** 並按一下 **[!UICONTROL Continue]**.

   ![您金鑰的Google Maps平台](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. 使用Google帳戶登入或建立帳戶。

1. 設定專案：

   - 選取專案或輸入新專案名稱。

   - 若要接受條款，請選取 `Yes`.

   - 按一下 **[!UICONTROL Next]**.

1. 輸入帳單帳戶或建立帳單帳戶。 您可以略過並在稍後新增帳單帳戶。

   必須有付費帳戶才能使用此服務。

1. 若要開啟並設定您的Google Cloud平台選項，請按一下 **[!UICONTROL Console]**.

   - 開啟您的專案。

   - 展開功能表並按一下 **[!UICONTROL APIs & Services]** > **[!UICONTROL Library]**.

     ![Google API服務](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - 搜尋 [地理編碼API][2] 和 [距離矩陣API][3]. 選取並啟用每個服務。

1. 展開功能表，按一下 **[!UICONTROL APIs & Services]** > **[!UICONTROL Credentials]**，並複製Google API金鑰。

   ![Google API金鑰副本](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### 步驟2：設定Google MAP提供者

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Inventory]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Distance Provider for Distance Based SSA]_部分與集合&#x200B;**[!UICONTROL Provider]**至 `Google MAP`.

   ![距離型SSA提供者](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Google Distance Provider]_並設定設定：

   - 的 **[!UICONTROL Google API Key]**，輸入從您的Google帳戶複製的金鑰。

   - 的 **[!UICONTROL Computation mode]**，選取設定。

     >[!NOTE]
     >
     >使用此演演算法出貨時，如果針對出貨選取的「計算」模式（駕駛、騎腳踏車或行走）未傳迴路線與資料，則SSA會預設為使用「來源優先順序」。 設定 [每庫存來源的優先順序](stocks-prioritize-sources.md) 建議使用。

     | 選項 | 說明 |
     | ----- | ----- |
     | `Driving` | （預設）使用道路網路來要求標準行車路線。 |
     | `Walking` | 使用人行道和人行道（如果可用）來要求步行路線。 |
     | `Bicycling` | 使用腳踏車道和偏好的街道（如果有的話），要求腳踏車騎行路線。 此 [距離矩陣服務][4] 僅於美國和部分加拿大城市提供。 |

   - 的 **[!UICONTROL Value]**，選取值型別：

     | 選項 | 說明 |
     | ----- | ----- |
     | `Distance` | （預設）傳回以公制（公里與公尺）或英制（英里與英尺）為單位的點之間的距離。 |
     | `Time to Destination` | 傳回從來源地點前往運送地址所需的時間（小時與分鐘）。 |

   ![Google距離提供者](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.

## 使用離線計算

離線計算會使用國家/地區代碼來決定出貨目的地與來源地址之間的距離。 可能需要開發人員協助才能設定此選項。 使用 [!DNL Inventory Management] 下載和匯入資料的CLI命令 [geonames.org][5].

>[!NOTE]
>
>已從匯入地理代碼 [geonames.org][5] 在部分國家/地區有限制，例如加拿大和愛爾蘭。 請參閱 [地名郵遞區號檔案][6] 以取得詳細資訊。

### 步驟1：下載和匯入地理代碼

完整的命令列設定，可下載並匯入地理代碼國家/地區以送貨至並擁有來源位置。 此步驟可能需要開發人員協助以取得命令列工作的說明。 請參閱 [匯入地理代碼](cli.md#import-geocodes).

您隨時想要新增更多地理代碼時都可完成這些指令。

### 步驟2：設定計算

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 在左側面板中，展開 **[!UICONTROL Catalog]** 並選擇 **[!UICONTROL Inventory]**.

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 _[!UICONTROL Distance Provider for Distance Based SSA]_區段。

1. 取消選取 **[!UICONTROL Use system value]** 核取方塊並設定 **[!UICONTROL Provider]** 至 `Offline Calculation`.

   ![距離型SSA的距離提供者](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. 完成後，按一下 **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start
[4]: https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes
[5]: https://www.geonames.org/
[6]: https://download.geonames.org/export/zip/readme.txt
