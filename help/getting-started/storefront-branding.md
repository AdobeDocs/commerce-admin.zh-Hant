---
title: 店面品牌
description: 瞭解如何變更定義商店品牌識別的元素。
exl-id: 91630717-9da7-4d2f-a0d8-adb794a30ee1
feature: Storefront
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---

# 店面品牌

您首先要做的其中一件事就是[變更標頭中的標誌](#upload-your-logo)，然後[為瀏覽器](#add-a-favicon)上傳Favicon。 接下來，您應該[新增您的歡迎訊息](#change-the-welcome-message)並[更新頁尾中的版權宣告](#change-the-copyright-notice)。 這些是一些您可以立即處理的簡單設計元素。 當您的商店處於開發狀態時，您可以[開啟商店示範通知](#set-the-store-demo-notice)，然後在準備啟動時移除它。

![店面品牌元素](./assets/storefront-home-page-branding.png){width="600" zoomable="yes"}

## 上傳您的標誌

標頭中標誌的大小和位置由商店主題決定。 您的標誌可以儲存為GIF、PNG或JPG (JPEG)檔案型別，並由商店管理員上傳。

頁首](./assets/storefront-header-logo.png){width="600"}中的![標誌

標誌影像位於伺服器上的下列位置。 任何名稱為`logo.svg`的影像檔案都會做為預設的主題標誌。

完整路徑 — `app/design/frontend/[vendor]/[theme]/web/images/logo.svg`

相對路徑 — `images/logo.svg`

如果您不知道主題中使用的標誌或其他影像大小，請在瀏覽器中開啟頁面，以滑鼠右鍵按一下影像，然後檢查元素。

>[!NOTE]
>
>除了標題中的標誌外，您的標誌也會出現在[電子郵件範本](../systems/email-templates.md#prepare-your-email-logo)和[PDF發票](../stores-purchase/sales-documents.md)及其他銷售檔案上。 用於電子郵件範本和發票的標誌有不同的大小要求，必須單獨上傳。

支援的標誌檔案格式：

| 檔案格式 | 說明 |
|--- |--- |
| PNG | （可攜式網路圖形）這個較新的GIF格式替代方案，最多可支援1600萬色（24位元）。 不失真壓縮格式會產生高品質的點陣圖影像，其中包含清晰的文字，但檔案大小比某些格式大。 PNG格式支援透明圖層，專為線上檢視和串流而設計。 |
| GIF | （圖形交換格式）廣泛支援的較舊點陣圖格式，限製為256色（8位元）。 GIF格式支援簡單動畫和透明圖層。 |
| JPG (JPEG) | (Joint Photographic Expert Group)大多數數位相機使用的壓縮點陣圖格式。 有失真壓縮會產生一些資料遺失，有時在文字中會出現模糊點。 |

{style="table-layout:auto"}

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。

   ![設計設定頁面](./assets/design-configuration.png){width="700"}

1. 尋找您要設定的存放區檢視，然後按一下&#x200B;_[!UICONTROL Action]_欄中的&#x200B;**[!UICONTROL Edit]**。

1. 展開&#x200B;**[!UICONTROL Header]**&#x200B;區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![標頭設定](./assets/configuration-header.png){width="600"}

1. 若要上傳新標誌，請按一下&#x200B;**[!UICONTROL Upload]**，然後從您的系統選擇檔案。

1. 輸入&#x200B;**[!UICONTROL Logo Image Width]**&#x200B;和&#x200B;**[!UICONTROL Logo Image Height]**&#x200B;畫素。

1. 針對&#x200B;**[!UICONTROL Logo Image Alt]**，輸入當有人將滑鼠懸停在影像上時要顯示的文字。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Configuration]**。

## 新增Favicon

_Favicon_&#x200B;是&#x200B;_最愛圖示_&#x200B;的縮寫，並參照每個瀏覽器頁面標籤上的小圖示。 根據瀏覽器的不同，Favicon也會顯示在位址列中，緊接在URL的前面。

Favicon通常是16 x 16畫素或32 x 32畫素大小。 [!DNL Commerce]接受ICO、PNG、APNG、GIF和JPG (JPEG)檔案型別，但並非所有瀏覽器都支援這些格式。 Favicon最廣泛支援的檔案格式為ICO。 您可以使用其他影像檔案型別，但並非所有瀏覽器都支援此格式。 線上有許多可用的免費工具，可用來產生ICO影像或將影像轉換為該格式。

瀏覽器標籤中的![Favicon](./assets/storefront-favicon.png){width="600"}

[!DNL Commerce]支援下列檔案格式做為Favicon：

| 檔案格式 | 說明 |
|--- |--- |
| ICO | 此影像檔案格式是專為小型電腦圖示影像所設計。 ICO格式大多用於Microsoft® Windows作業系統，最多可包含256 x 256畫素和1600萬色（24位元）的影像，以及8位元透明度。 |
| PNG | （可攜式網路圖形）這個較新的GIF格式替代方案，最多可支援1600萬色（24位元）。 不失真壓縮格式會產生高品質的點陣圖影像，其中包含清晰的文字，但檔案大小比某些格式大。 PNG格式支援透明圖層，專為線上檢視和串流而設計。 |
| APNG | （可攜式網路圖形動畫）與PNG類似的檔案格式，可支援簡單動畫。 |
| GIF | （圖形交換格式）廣泛支援的較舊點陣圖格式，限製為256色（8位元）。 GIF格式支援簡單動畫和透明圖層。 |
| JPG (JPEG) | (Joint Photographic Expert Group)大多數數位相機使用的壓縮點陣圖格式。 有失真壓縮會產生一些資料遺失，有時在文字中會出現模糊點。 |

{style="table-layout:auto"}

### 步驟1：建立Favicon

1. 使用您選擇的影像編輯器，建立您標誌的16 x 16或32 x 32圖形影像。

1. （選擇性）使用其中一個可用的線上工具，將檔案轉換成.ico格式，並將檔案儲存到您的電腦。

### 步驟2：將Favicon上傳至您的存放區

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。

1. 在網格中，尋找您要設定的存放區檢視，然後按一下&#x200B;_[!UICONTROL Action]_欄中的&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;_[!UICONTROL Other Settings]_底下，展開&#x200B;**[!UICONTROL HTML Head]**區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![HTML標頭設定](./assets/configuration-html-head.png){width="600"}

1. 如果要移除目前的Favicon，請按一下影像左下角的&#x200B;_刪除_ （![垃圾桶圖示](../assets/icon-delete-trashcan.png)）圖示。

1. 按一下&#x200B;**[!UICONTROL Upload]**&#x200B;並開啟您準備的Favicon檔案。

   ![已上傳Favicon](./assets/favicon-upload.png){width="400"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Configuration]**。

### 步驟3：重新整理快取

1. 當提示重新整理快取時，請按一下工作區頂端訊息中的&#x200B;**[!UICONTROL Cache Management]**&#x200B;連結。

1. 在清單中，選取標示為`Invalidated`的&#x200B;**[!UICONTROL Page Cache]**&#x200B;核取方塊。

1. 將&#x200B;**[!UICONTROL Actions]**&#x200B;設為`Refresh`並按一下&#x200B;**[!UICONTROL Submit]**。

1. 若要檢視新的Favicon，請返回您的店面並重新整理瀏覽器。

## 變更歡迎訊息

標題中的歡迎訊息會展開並包含已登入的客戶名稱。 啟動商店之前，請務必變更每個商店檢視的預設&#x200B;_歡迎_&#x200B;文字。

![歡迎訊息](./assets/storefront-welcome-message.png){width="600"}

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。

1. 在網格中，尋找您要設定的存放區檢視，然後按一下&#x200B;_[!UICONTROL Action]_欄中的&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;_[!UICONTROL Other Settings]_底下，展開&#x200B;**[!UICONTROL Header]**區段的![擴充選擇器](../assets/icon-display-expand.png)。

1. 針對&#x200B;**[!UICONTROL Welcome Text]**，輸入您要在商店標頭中顯示的歡迎訊息文字。

   ![標頭設定](./assets/configuration-header.png){width="600"}

1. 完成時，按一下&#x200B;**[!UICONTROL Save Configuration]**。

1. 當提示更新頁面快取時，請按一下工作區頂端的&#x200B;**[!UICONTROL Cache Management]**&#x200B;連結，然後依照指示重新整理快取。

## 變更版權宣告

您的商店會在每個頁面的頁尾顯示版權宣告。 依據最佳做法的要求，版權宣告應包含當年，並將您的公司識別為網站內容的合法擁有者。

![著作權宣告範例](./assets/storefront-footer-copyright.png){width="600"}

`&copy;`字元代碼用於插入版權符號，如下列範例所示：

- 長格式範例

  `Copyright &copy; 2013-present Luma, Inc. All rights reserved.`

- 簡短格式範例

  `&copy; 2021 Luma, Inc. All rights reserved.`

**_若要更新版權宣告：_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。

1. 在網格中，尋找您要設定的存放區檢視，然後按一下&#x200B;_[!UICONTROL Action]_欄中的&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;_其他設定_&#x200B;下，展開![擴充選擇器](../assets/icon-display-expand.png) **[!UICONTROL Footer]**&#x200B;區段。

   ![頁尾設計設定](./assets/configuration-footer.png){width="600"}

1. 針對&#x200B;**[!UICONTROL Copyright]**，輸入您想要顯示在每個頁面頁尾的版權宣告。

   使用`&copy;`字元代碼插入版權符號。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Configuration]**。

## 設定商店示範通知

如果您的商店線上上，但仍在建置中，您可以在頁面頂端顯示商店示範通知，告知人們該商店尚未營業。 當您準備好&#x200B;_上線_&#x200B;時，只要移除訊息即可。 它類似於將視窗中懸掛的符號從&#x200B;_已關閉_&#x200B;翻轉為&#x200B;_已開啟_。 示範通知的格式由商店的主題決定。

![店面示範通知](./assets/storefront-demo-notice.png){width="600"}

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**。

1. 在網格中，尋找您要設定的存放區檢視，然後按一下&#x200B;_[!UICONTROL Action]_欄中的&#x200B;**[!UICONTROL Edit]**。

1. 在&#x200B;_[!UICONTROL Other Settings]_底下，展開&#x200B;**[!UICONTROL HTML Head]**區段的![擴充選擇器](../assets/icon-display-expand.png)。

   ![HTML標題](./assets/configuration-html-head.png){width="600"}

1. 向下捲動至底部，並將&#x200B;**[!UICONTROL Display Demo Store Notice]**&#x200B;設定為您的偏好設定。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Configuration]**。

1. 如果系統提示您更新快取，請在系統訊息中按一下&#x200B;**[!UICONTROL Cache Management]**，然後依照指示重新整理快取。
