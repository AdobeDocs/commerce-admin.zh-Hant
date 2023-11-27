---
title: 授權Adobe Stock影像
description: 為確保您擁有合法存取權並消除Adobe Stock浮水印，請授權您的Adobe Stock影像。
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# 授權Adobe Stock影像

您想要用於生產Adobe Commerce和Magento Open Source商店的Adobe Stock資產應該獲得授權。 此授權確保您擁有影像的合法存取權，並消除了存在於所有人的Adobe Stock浮水印 [影像預覽][save-preview]. 若要授權影像或儲存已授權的影像，您必須登入您的Adobe帳戶。

新的 [[!DNL Media Gallery]](media-gallery.md) 提供與Adobe Stock的直接整合，讓您直接從gallery頁面輕鬆授權影像。

## 必要條件

此功能需要 [Adobe Stock整合][adobe-stock-integration] 模組和設定。 授權 [Adobe Stock][adobe-stock] 影像需要付費Adobe Stock計畫和 [Adobe帳戶][adobe-signin].

## 從新授權影像 [!DNL Media Gallery]

1. 在 _管理員_ 側欄，前往 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 請依照以下步驟操作： [使用Adobe Stock影像][using-adobe-stock] 以登入並將預覽影像儲存至 [媒體儲存][media-storage].

   ![已儲存的預覽影像](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. 按一下影像下方的三個點(![資產功能表圖示](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"})，然後按一下 **[!UICONTROL License]**.

   ![Adobe Stock影像動作](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >如果您未登入，則會顯示登入表單。 如需登入的詳細資訊，請參閱 [使用Adobe Stock影像][using-adobe-stock].

1. 在授權確認對話方塊中，按一下 **[!UICONTROL Confirm]** 以授權影像。

   ![授權確認](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >您必須有可用的 [Adobe Stock積分][stock-credits] 在您的帳戶中授權該影像。

## 從標準媒體儲存空間授權影像

1. [存取Adobe Stock搜尋格線][access-search].

1. 至 [檢視影像詳細資料][view-details]，依序按一下搜尋格線中的影像。

1. 請根據影像目前的授權狀態，執行下列任一項作業：

   - 如果影像已獲得授權，請按一下 **[!UICONTROL Save]**.

   - 如果影像為 _非_ 已授權，按一下 **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >您必須有可用的 [Adobe Stock積分][stock-credits] 在您的帳戶中授權該影像。

   這個動作會顯示提示，讓您指定用來將影像儲存到 [媒體儲存][media-storage]. 預設檔案名稱已提供，但您可以根據您的偏好自訂名稱。

   ![儲存Adobe Stock授權的影像](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. 按一下 **[!UICONTROL Confirm]**.

   頁面會重新導向至媒體儲存空間，並顯示您儲存的預覽。

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
