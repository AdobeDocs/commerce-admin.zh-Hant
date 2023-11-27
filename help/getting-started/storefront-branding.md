---
title: 店面品牌
description: 瞭解如何變更定義商店品牌識別的元素。
exl-id: 91630717-9da7-4d2f-a0d8-adb794a30ee1
feature: Storefront
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1285'
ht-degree: 0%

---

# 店面品牌

您首先要做的其中一件事就是 [變更標誌](#upload-your-logo) 在標題和 [上傳favicon](#add-a-favicon) 適用於瀏覽器。 接下來，您應該 [新增您的歡迎訊息](#change-the-welcome-message) 和 [更新版權宣告](#change-the-copyright-notice) 在頁尾中。 這些是一些您可以立即處理的簡單設計元素。 當您的商店處於開發狀態時，您可以 [開啟商店示範通知](#set-the-store-demo-notice)，然後在您準備好啟動時將其移除。

![店面品牌元素](./assets/storefront-home-page-branding.png){width="600" zoomable="yes"}

## 上傳您的標誌

標頭中標誌的大小和位置由商店主題決定。 您的標誌可以儲存為GIF、PNG或JPG(JPEG)檔案型別，並由商店管理員上傳。

![頁首中的標誌](./assets/storefront-header-logo.png){width="600"}

標誌影像位於伺服器上的下列位置。 任何名為的影像檔案 `logo.svg` 會作為預設佈景主題標誌使用。

完整路徑 —  `app/design/frontend/[vendor]/[theme]/web/images/logo.svg`

相對路徑 —   `images/logo.svg`

如果您不知道主題中使用的標誌或其他影像大小，請在瀏覽器中開啟頁面，以滑鼠右鍵按一下影像，然後檢查元素。

>[!NOTE]
>
>除了標題中的標誌外，您的標誌也會出現在 [電子郵件範本](../systems/email-templates.md#prepare-your-email-logo) 及於 [PDF發票](../stores-purchase/sales-documents.md) 和其他銷售檔案。 用於電子郵件範本和發票的標誌有不同的大小要求，必須單獨上傳。

支援的標誌檔案格式：

| 檔案格式 | 說明 |
|--- |--- |
| PNG | （可攜式網路圖形）這個較新的GIF格式替代方案，最多可支援1600萬色（24位元）。 不失真壓縮格式會產生高品質的點陣圖影像，其中包含清晰的文字，但檔案大小比某些格式大。 PNG格式支援透明圖層，專為線上檢視和串流而設計。 |
| GIF | （圖形交換格式）廣泛支援的較舊點陣圖格式，限製為256色（8位元）。 GIF格式支援簡單動畫和透明圖層。 |
| JPG(JPEG) | (Joint Photographic Expert Group)大多數數位相機使用的壓縮點陣圖格式。 有失真壓縮會產生一些資料遺失，有時在文字中會出現模糊點。 |

{style="table-layout:auto"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   ![設計組態頁面](./assets/design-configuration.png){width="700"}

1. 尋找要設定的存放區檢視，然後按一下 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 展開 ![展開選擇器](../assets/icon-display-expand.png) 此 **[!UICONTROL Header]** 區段。

   ![標題設定](./assets/configuration-header.png){width="600"}

1. 若要上傳新標誌，請按一下 **[!UICONTROL Upload]** 並從系統選擇檔案。

1. 輸入 **[!UICONTROL Logo Image Width]** 和 **[!UICONTROL Logo Image Height]** 以畫素為單位。

1. 的 **[!UICONTROL Logo Image Alt]**，輸入當有人將滑鼠懸停在影像上時要顯示的文字。

1. 完成後，按一下 **[!UICONTROL Save Configuration]**.

## 新增Favicon

_法維孔_ 是縮寫 _我的最愛圖示_ 和會參照每個瀏覽器頁面標籤上的小圖示。 根據瀏覽器的不同，Favicon也會顯示在位址列中，緊接在URL的前面。

Favicon通常是16 x 16畫素或32 x 32畫素大小。 [!DNL Commerce] 接受ICO、PNG、APNG、GIF和JPG(JPEG)檔案型別，但並非所有瀏覽器都支援這些格式。 Favicon最廣泛支援的檔案格式為ICO。 您可以使用其他影像檔案型別，但並非所有瀏覽器都支援此格式。 線上有許多可用的免費工具，可用來產生ICO影像或將影像轉換為該格式。

![瀏覽器標籤中的Favicon](./assets/storefront-favicon.png){width="600"}

[!DNL Commerce] 支援下列檔案格式做為Favicon：

| 檔案格式 | 說明 |
|--- |--- |
| ICO | 此影像檔案格式是專為小型電腦圖示影像所設計。 ICO格式大多用於Microsoft® Windows作業系統，最多可包含256 x 256畫素和1600萬色（24位元）的影像，以及8位元透明度。 |
| PNG | （可攜式網路圖形）這個較新的GIF格式替代方案，最多可支援1600萬色（24位元）。 不失真壓縮格式會產生高品質的點陣圖影像，其中包含清晰的文字，但檔案大小比某些格式大。 PNG格式支援透明圖層，專為線上檢視和串流而設計。 |
| APNG | （可攜式網路圖形動畫）與PNG類似的檔案格式，可支援簡單動畫。 |
| GIF | （圖形交換格式）廣泛支援的較舊點陣圖格式，限製為256色（8位元）。 GIF格式支援簡單動畫和透明圖層。 |
| JPG(JPEG) | (Joint Photographic Expert Group)大多數數位相機使用的壓縮點陣圖格式。 有失真壓縮會產生一些資料遺失，有時在文字中會出現模糊點。 |

{style="table-layout:auto"}

### 步驟1：建立Favicon

1. 使用您選擇的影像編輯器，建立您標誌的16 x 16或32 x 32圖形影像。

1. （選擇性）使用其中一個可用的線上工具，將檔案轉換成.ico格式，並將檔案儲存到您的電腦。

### 步驟2：將Favicon上傳至您的存放區

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 在格線中，尋找要設定的存放區檢視，然後按一下 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 在 _[!UICONTROL Other Settings]_，展開 ![展開選擇器](../assets/icon-display-expand.png) 此&#x200B;**[!UICONTROL HTML Head]**區段。

   ![HTML標頭設定](./assets/configuration-html-head.png){width="600"}

1. 如果要移除目前的Favicon，請按一下 _刪除_ (![垃圾桶圖示](../assets/icon-delete-trashcan.png))圖示中依視覺效果標示。

1. 按一下 **[!UICONTROL Upload]** 並開啟您準備的favicon檔案。

   ![已上傳Favicon](./assets/favicon-upload.png){width="400"}

1. 完成後，按一下 **[!UICONTROL Save Configuration]**.

### 步驟3：重新整理快取

1. 當提示重新整理快取時，按一下 **[!UICONTROL Cache Management]** 工作區頂端訊息中的連結。

1. 在清單中，選取 **[!UICONTROL Page Cache]** 已標示的核取方塊 `Invalidated`.

1. 設定 **[!UICONTROL Actions]** 至 `Refresh` 並按一下 **[!UICONTROL Submit]**.

1. 若要檢視新的Favicon，請返回您的店面並重新整理瀏覽器。

## 變更歡迎訊息

標題中的歡迎訊息會展開並包含已登入的客戶名稱。 啟動商店之前，請務必變更預設值 _歡迎_ 每個商店檢視的文字。

![歡迎訊息](./assets/storefront-welcome-message.png){width="600"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 在格線中，尋找要設定的存放區檢視，然後按一下 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 在 _[!UICONTROL Other Settings]_，展開 ![展開選擇器](../assets/icon-display-expand.png) 此&#x200B;**[!UICONTROL Header]**區段。

1. 的 **[!UICONTROL Welcome Text]**，輸入您要在商店標頭中顯示的歡迎訊息文字。

   ![標題設定](./assets/configuration-header.png){width="600"}

1. 完成後，按一下 **[!UICONTROL Save Configuration]**.

1. 當提示您更新頁面快取時，請按一下 **[!UICONTROL Cache Management]** 工作區頂端的連結，並依照指示重新整理快取。

## 變更版權宣告

您的商店會在每個頁面的頁尾顯示版權宣告。 依據最佳做法的要求，版權宣告應包含當年，並將您的公司識別為網站內容的合法擁有者。

![版權宣告範例](./assets/storefront-footer-copyright.png){width="600"}

此 `&copy;` 字元代碼用於插入版權符號，如下列範例所示：

- 長格式範例

  `Copyright &copy; 2013-present Luma, Inc. All rights reserved.`

- 簡短格式範例

  `&copy; 2021 Luma, Inc. All rights reserved.`

**_更新版權宣告：_**

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 在格線中，尋找要設定的存放區檢視，然後按一下 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 在 _其他設定_，展開 ![展開選擇器](../assets/icon-display-expand.png)此 **[!UICONTROL Footer]** 區段。

   ![頁尾設計設定](./assets/configuration-footer.png){width="600"}

1. 的 **[!UICONTROL Copyright]**，請輸入您想要顯示在每個頁面頁尾的版權宣告。

   使用 `&copy;` 字元代碼以插入版權符號。

1. 完成後，按一下 **[!UICONTROL Save Configuration]**.

## 設定商店示範通知

如果您的商店線上上，但仍在建置中，您可以在頁面頂端顯示商店示範通知，告知人們該商店尚未營業。 當您準備好時 _上線_，直接移除訊息即可。 這類似於翻轉掛在視窗上的符號 _已關閉_ 至 _開啟_. 示範通知的格式由商店的主題決定。

![店面示範通知](./assets/storefront-demo-notice.png){width="600"}

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 在格線中，尋找要設定的存放區檢視，然後按一下 **[!UICONTROL Edit]** 在 _[!UICONTROL Action]_欄。

1. 在 _[!UICONTROL Other Settings]_，展開 ![展開選擇器](../assets/icon-display-expand.png) 此&#x200B;**[!UICONTROL HTML Head]**區段。

   ![HTML標題](./assets/configuration-html-head.png){width="600"}

1. 向下捲動至底部並設定 **[!UICONTROL Display Demo Store Notice]** 依您的偏好設定。

1. 完成後，按一下 **[!UICONTROL Save Configuration]**.

1. 如果系統提示您更新快取，請按一下 **[!UICONTROL Cache Management]** 並依照指示重新整理快取。
