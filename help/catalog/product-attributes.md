---
title: 產品屬性概觀
description: 瞭解產品屬性，以及如何使用它們描述產品的特定特性。
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/reh5hq2WF3rmbKEKZiV8U18hfyLxXeUHHfJcUgWDcJ0
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 547
ht-degree: 0%

---

# 產品屬性概觀

屬性是產品目錄的建置組塊，可描述產品的特定特性。 產品屬性可以組織成[屬性集](attribute-sets.md)，然後作為建立產品的範本使用。

屬性決定用於產品選項的輸入控制項型別，並為產品頁面提供其他資訊。 它們也可用來作為搜尋引數，以及階層式導覽、產品比較報表和促銷活動的條件。 您可以視需要建立儘可能多的屬性和屬性集，以說明目錄中的產品。 除了您可以建立的屬性之外，系統屬性（例如價格）也會內建在核心Commerce平台中，且無法變更。

![編輯產品時建立新屬性](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

計畫和建立產品屬性時，請使用以下幾節所述的最佳實務。

## 屬性名稱

建立一致的屬性命名慣例，包括字母大小寫和標點符號。 例如，`Color:Green`和`Color:green`可以被不同的系統視為兩個不同的屬性值。 資料中的這類雜訊會影響商業規則、搜尋結果，以及將產品與規則相符的應用程式的資料篩選器。

## 屬性使用

考慮指派屬性和值時如何使用屬性。 識別用來作為展示標籤的屬性，例如產品名稱、影像、價格和說明，以及用於資料輸入的屬性。 請思考屬性在整個網站的不同頁面上呈現的方式，以及它們在類別頁面、產品詳細資料頁面、類別格線及縮圖滑杆上的顯示方式。

## 顏色

從資料庫操作的角度來看，臨機色彩說明可能會帶來挑戰。 色彩名稱（例如「Azure Skies」或「Robin Egg Blue」）非常吸引人，但在作為搜尋條件使用或銷售需要您指定`Color_Family:Blue`時，可能不會傳回最佳結果。 請思考搜尋結果和分層導覽中色彩的顯示方式，並針對您的業務需求建立一些指導方針。 然後，在整個目錄中指定顏色屬性值時需保持一致。

## 變數管理

使用產品[組態選項](product-configurations.md)和[可組態產品](product-create-configurable.md)來管理產品方案中的變異。 這些功能可讓您更輕鬆地分類產品、建立購物車價格規則和動態類別規則，並提供包含各種文字、選擇和日期輸入型別的選項選擇。

## 加權搜尋

為[目錄搜尋](search.md)啟用的產品屬性可以指派權重，以便在搜尋結果中提供較高的值。 較重量的屬性會先傳回，再傳回較輕量的屬性。 例如，考慮系統中的兩個屬性，搜尋權重為3的&#x200B;_color_&#x200B;和搜尋權重為1的&#x200B;_description_。 搜尋單字&#x200B;_red_&#x200B;會傳回色彩屬性值為`red`的產品清單，但不會傳回描述包含單字&#x200B;_red_&#x200B;的產品。 在此範例中，`color`屬性的定義權重大於`description`屬性。

## 未使用的屬性

移除未使用的產品屬性，以獲得更好的建構和更快的索引。


>[!NOTE]
>
>如需最佳化產品屬性設定效能的詳細資訊，請參閱&#x200B;_實作行動手冊_&#x200B;中的[目錄管理最佳實務](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/planning/catalog-management#product-attributes)。
