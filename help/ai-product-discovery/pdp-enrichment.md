---
title: 產品詳細資料頁面擴充
description: 使用[!DNL Adobe Commerce]產品詳細資料頁面擴充功能來檢閱AI建議的產品復本、建立擴充工作，以及部署LLM和AI探索的已核准更新。
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 0%
---

# 產品詳細資料頁面擴充

產品詳細資料頁面(PDP)擴充功能可讓LLM在每個PDP上（具有結構化產品資料）獲得最大可抓取性，而不會對您的人類可見體驗進行任何變更。 此功能會讀取您的產品目錄，以針對每個PDP建立結構化的資料裝載，讓LLM輕鬆讀取及剖析。

## 運作方式 {#how-it-works}

您的Adobe Commerce目錄包含產品資訊，例如，屬性、系列品種、類別、價格和可用性。 在PDP擴充工作中，您可以選取產品頁面和目錄事實群組，以供AI代理程式使用。 會為代理商整理資訊，而不會變更店面體驗。

透過PDP擴充，您可以：

- 選擇具有即時產品頁面的特定已啟用產品。
- 在儲存或執行工作之前，先檢閱所選頁面和事實的摘要。
- 預覽擴充中包含的產品資訊。

| 方向 | 用途 |
| --- | --- |
| Commerce目錄 — >擴充工作 | Select即時產品頁面和要包含的目錄事實。 |
| 擴充工作 — > AI代理程式 | 以結構化形式提供所選現有產品資訊。 人類可見的店面不會變更。 |

## 存取PDP擴充

開始之前，請先檢閱部署特定的[AI產品探索先決條件](prerequisites.md)。 完成Commerce平台的設定後，在[管理員]中開啟&#x200B;**[!UICONTROL AI Product Discovery]**&#x200B;並選取&#x200B;**[!UICONTROL Product Details Page Enrichment]**。

## PDP擴充的兩條途徑

接收PDP擴充的兩個路徑：

- **代理流量** — 此型別的擴充會在您設定Commerce執行個體後24到48小時自動開始，並在&#x200B;**最佳化**&#x200B;索引標籤上顯示結果。
- **擴充管理員** — 這些擴充功能是由商家按一下「**[!UICONTROL Create enrichment]**」按鈕並手動選取要擴充的SKU時設定。 深入瞭解[擴充管理員](#create-an-enrichment-job)。

## 檢閱PDP擴充活動

PDP擴充頁面會開啟至&#x200B;**[!UICONTROL Optimizations]**&#x200B;標籤。 使用儀表板來複查擴充涵蓋範圍、工作活動以及需要注意的工作。 使用&#x200B;**[!UICONTROL Settings]**&#x200B;索引標籤將[連結至](settings.md)您的Commerce執行個體以進行AI產品探索。

### 尋找需要注意的工作

**[!UICONTROL Needs your attention]**&#x200B;區段會醒目顯示需要動作的工作。 卡片可顯示工作名稱、選取產品的方式、產品頁數、工作狀態和進度。 使用卡片上的可用動作以繼續工作。

### 搜尋所有工作

使用表格來搜尋及追蹤工作。 依工作詳細資料搜尋或依狀態篩選，包括&#x200B;**[!UICONTROL Generating]**、**[!UICONTROL Ready to review]**、**[!UICONTROL Deployed]**、**[!UICONTROL Queued]**&#x200B;或&#x200B;**[!UICONTROL Failed]**。 此表格會列出每個工作的ID、名稱、來源、產品頁數、開始日期、狀態以及可用的動作。

## 建立擴充工作

在本節中，您將瞭解如何建立產品詳細資料頁面擴充。

![建立PDP擴充](./assets/create-cat-enrich.png)

1. 在&#x200B;**[!UICONTROL Optimizations]**&#x200B;中，按一下&#x200B;**[!UICONTROL Create enrichment]**。
1. 輸入&#x200B;**擴充名稱**，例如「2026年黑色星期五」。
1. Select **類別**，例如「咖啡」。
1. Select **屬性集**，例如「配件」。
1. Select **產品型別**，例如「簡單產品」。
1. Select **價格範圍**。
1. 按一下&#x200B;**[!UICONTROL Apply filters]**。

   您可以預覽符合擴充條件的產品，然後按一下[自訂]，以進一步限定您要擴充的產品。****

1. 按一下&#x200B;**[!DNL Next]**&#x200B;以確認您要擴充的特定產品。
1. 按一下&#x200B;**[!DNL Run enrichment]**。

   擴充工作會在&#x200B;**最佳化**&#x200B;表格上執行及顯示。 當它完成執行時，您可以[檢閱並部署](#review-and-deploy-an-enrichment-job)最佳化。

### 檢閱擴充工作 {#review-and-deploy-an-enrichment-job}

開啟擴充工作。

![PDP擴充URL清單](./assets/pdp-enrich-urls.png)

含有建議的&#x200B;**URL**&#x200B;表格列出所有具有擴充機會的產品。 對於每個產品，您可以：

- **展開列**&#x200B;以檢視AI分析和建議的擴充。
- **在套用之前先編輯**&#x200B;建議的產品名稱或描述，以符合您的品牌語調和銷售准則。
- **針對您要擴充的產品部署最佳化**，並將其直接發佈至您的Adobe Commerce店面。
- 在稽核並套用擴充後，**標示為固定**。
- **忽略與您目錄策略無關的**&#x200B;建議。

建議分為三個檢視： **目前的建議**、**已修正的建議**&#x200B;和&#x200B;**忽略的建議**。 套用擴充後，它會移至&#x200B;**固定建議**，狀態為&#x200B;**已套用**。 套用的擴充功能可隨時回覆。

### 部署最佳化

檢閱建議並選取要最佳化的產品頁面後，按一下&#x200B;**部署最佳化**，以使用Edge的「最佳化」發佈擴充。 **部署至Edge**&#x200B;確認對話方塊會顯示選取的產品URL、最佳化型別和正在套用的擴充。 部署後，確認畫面會確認哪些產品頁面已成功最佳化。

最佳化是透過[在Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)最佳化，專門傳遞給AI使用者代理程式。 人類訪客會繼續看見您現有的店面體驗，就像之前一樣，不會變更PDP設計、頁面效能或品牌體驗。

## 限制和考量事項 {#limits}

- 只能選取已啟用的產品以及已上線的產品頁面。
- 擴充會組織目錄中已經存在的事實；不會新增產品資訊。
- PDP擴充工作流程不會變更店面。
- PDP擴充作業和目錄擴充作業具有不同的用途和工作流程。
- PDP最佳化使用[在Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)最佳化。

## 最佳實務 {#best-practices}

- 使用可識別產品群組或行銷活動的清晰工作名稱。
- 預覽工作中所包含的事實，並確認它們正確且適用於AI代理程式。
- 在決定略過或覆寫產品之前，請檢查產品是否已擴充。
- 與負責這些記錄的團隊協調目錄同步和產品事實的所有權。

## 範例：使用變體和規格擴充產品

產品頁面包含的目錄資訊通常多於AI代理程式可讀取的資訊量。 例如，商家銷售防水健行靴。 大小、寬度和顏色選項位於隨JavaScript載入的變體選擇器中。 材料、防水及護理指示位於摺疊的「細節」標籤中，而符合的指引會在快顯視窗中開啟。 購物者可以開啟所有這些內容，但在頁面首次載入時讀取頁面的AI爬蟲可能只能看到產品名稱、價格和簡短說明。

當擴充工作在此產品上執行時，會擷取產品的所有目錄資料，包括其屬性和每個變體，並以AI代理程式可讀取的結構化格式封裝。 AI助理可以回答以下問題：「此開機是否適合大小為11英吋的寬熒幕？」 或「完全防水嗎？」 來自商家自己的目錄資料。

擴充工作只會使用目錄中已存在的資訊。 它不會建立新的產品事實，也不會改變購物者看到的產品頁面。
