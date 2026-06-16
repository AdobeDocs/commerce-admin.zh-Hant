---
title: PayPal結算報表
description: 瞭解PayPal結算報表，作為管理PayPal交易的工具。
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="僅限PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"
TQID: https://experienceleague.adobe.com/c7v5oSsVPmD6r6obfGEoxPiGkMI4KMWAmfJAW0-CCJk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 0%

---

# PayPal結算報表

「PayPal結算」報表會針對影響資金結算的每筆交易，為商家提供相關資訊。

>[!NOTE]
>
>在產生結算報表之前，商店管理員必須要求PayPal Merchant Technical Services建立SFTP使用者帳戶、啟用結算報表的產生，以及在其PayPal企業帳戶中啟用SFTP。

在PayPal商家帳戶中設定並啟用結算報表後，Adobe Commerce和Magento Open Source將在下列24小時內開始產生報表。 可用的結算報表清單可由管理員檢視。

**_若要檢視結算報告:_**

1. 在&#x200B;_管理員_&#x200B;側邊欄上，移至&#x200B;**[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**。

   ![PayPal結算報告](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. 如需最新更新，請按一下右上角的&#x200B;**[!UICONTROL Fetch Updates]**。

   系統會連線至PayPal SFTP伺服器以擷取報表。 當程式完成時，會出現一則訊息，其中包含已擷取的報表數量。 此報表包含每個交易的下列資訊：

   | 報表欄 | 說明 |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | 下列其中一個參考代碼：<br/> — 訂單IDT<br/> — 交易ID<br/> — 訂閱ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** — 商家在PayPal交易上輸入的文字。<br/>**[!UICONTROL Transaction Debit or Credit]**— 總金額的貨幣流動方向。<br/>**[!UICONTROL Fee Debit or Credit]**  — 費用的資金流動方向。 |

   {style="table-layout:auto"}
