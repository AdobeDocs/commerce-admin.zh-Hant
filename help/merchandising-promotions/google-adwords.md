---
title: Google AdWords
description: 瞭解如何設定您的Commerce商店以進行Google AdWords轉換追蹤，以測量導致銷售或其他寶貴動作的廣告點選次數。
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Google AdWords

[Google AdWords][1]是一項服務，您可以在Google搜尋結果和Google顯示網路的公司頁面上放置廣告。 AdWords儀表板包含管理行銷活動、追蹤回應和測量結果的工具。

轉換追蹤會顯示導致銷售或其他重要動作的廣告點選次數。 提交訂單後顯示給客戶的&#x200B;_Success_&#x200B;頁面會用於追蹤轉換，因為它只會在銷售後顯示。 完成商店的Google AdWords設定後，不需要將轉換追蹤指令碼複製到成功頁面，因為Commerce已具備必要資訊。 若要進一步瞭解，請參閱[Google AdWords說明][2]。

在Google搜尋結果中![Adobe廣告](./assets/google-adwords-adobe-ad.png){width="500"}

## 步驟1. 建立Google AdWords行銷活動

1. 造訪[Google AdWords][3]，並註冊帳戶。

1. 依照指示建立行銷活動。

1. 若要設定行銷活動的轉換追蹤，請執行以下操作：

   - 在AdWords儀表板的&#x200B;**[!UICONTROL Tools]**&#x200B;標籤上，選擇&#x200B;**[!UICONTROL Conversions]**&#x200B;並按一下&#x200B;**[!UICONTROL Conversion]**。

   - 提示輸入轉換來源時，請選擇&#x200B;**[!UICONTROL Website]**。

   - 輸入您要追蹤的轉換動作名稱，然後按一下&#x200B;**[!UICONTROL Done]**。

   - 按一下「**[!UICONTROL Value]**」，並指派值給轉換（如果適用）。 例如：

      - 如果您在每次銷售上賺取$5，請選擇`Each time it happens`並指派值`$5`。
      - 如果每次銷售的值不盡相同，則將此值留空。

     若要完成，請按一下&#x200B;**[!UICONTROL Done]**。

   - 按一下&#x200B;**[!UICONTROL Conversion windows]**&#x200B;並完成設定，以決定要追蹤轉換的時間、報表類別和歸因模型。

1. 完成時，按一下&#x200B;**[!UICONTROL Save and Continue]**。

## 步驟2. 取得您的轉換標籤

1. 在&#x200B;**[!UICONTROL Install your tag]**&#x200B;底下，選擇計算&#x200B;**[!UICONTROL Page load]**&#x200B;的轉換。

1. 您可以將&#x200B;**[!UICONTROL Google Site Stats]**&#x200B;通知新增至轉換頁面作為選項。

   通知會顯示在下角，並附上Google安全性標準和Cookie使用方式的連結。

1. 若要選擇管理AdWords標籤的方式，請執行下列任一項作業：

   - 如果您打算自行將指令碼新增至儲存區，請選擇&#x200B;**[!UICONTROL Save instructions and tag]**。
   - 如果您打算讓其他人將指令碼新增至您的存放區，請選擇&#x200B;**[!UICONTROL Email instructions and tag]**。

1. 完成時，按一下&#x200B;**[!UICONTROL Done]**。

## 步驟3. 設定您的商店

{{gtag-api-note}}

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**。

1. 如果針對特定商店檢視設定Google AdWords，請執行以下操作：

   - 在左上角，選擇要設定的&#x200B;**[!UICONTROL Store View]**。

   - 提示確認範圍切換時，請按一下&#x200B;**[!UICONTROL OK]**。

1. 在左側面板中，展開&#x200B;**[!UICONTROL Sales]**&#x200B;並選擇&#x200B;**[!UICONTROL Google API]**。

1. 展開![展開選取器](../assets/icon-display-expand.png) **[!UICONTROL Google AdWords]**&#x200B;區段，然後執行下列動作：

   - 將&#x200B;**[!UICONTROL Enable]**&#x200B;設為`Yes`。

   - 從您的Google AdWords指令碼輸入&#x200B;**[!UICONTROL Conversion ID]**。

   ![銷售設定 — Google Ads API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. 若要設定Google Sites統計通知的格式，請執行下列動作：

   - 將&#x200B;**[!UICONTROL Conversion Language]**&#x200B;設定為在Google AdWords指令碼中識別的語言。

   - 輸入要在轉換頁面上用於Google Sites統計通知的&#x200B;**[!UICONTROL Conversion Format]**。

      - `1` — 顯示單行通知，內含連結，可連結至Google追蹤的詳細資訊。
      - `2` — 顯示兩行通知，其中包含有關Google追蹤詳細資訊的連結。
      - `3` — 不顯示客戶通知。

   - 為您要用於Google網站統計通知標籤的&#x200B;**[!UICONTROL Conversion Color]**&#x200B;輸入[十六進位代碼][4]{：target=&quot;_blank&quot;}。

   - 輸入顯示在Google Sites Stat通知上的&#x200B;**[!UICONTROL Conversion Label]**&#x200B;的加密文字。

     例如： `MlEYCOKBnGoQz6CZoAM`

     **範例Google AdWords標籤代碼**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. 將&#x200B;**[!UICONTROL Conversion Value Type]**&#x200B;設定為下列其中一項：

   - `Dynamic` — 根據動態訂單金額值判斷已發生轉換。
   - `Constant` — 根據輸入的特定值判斷轉換已經發生。

   針對&#x200B;_常數_&#x200B;轉換值型別，輸入&#x200B;_[!UICONTROL Order Amount]_的特定&#x200B;**[!UICONTROL Value]**以符合轉換資格。

1. 完成時，按一下&#x200B;**[!UICONTROL Save Config]**。

## 步驟4. 驗證設定

在數小時內，Google AdWords儀表板中的追蹤狀態從`Unverified`變更為`No recent conversions`或`Recording conversions`。 當有人按一下您的廣告並作出購買時，轉換會出現在您的控制面板和促銷活動報表的「轉換動作」頁面上。

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
