---
title: 登入憑證和URL
description: 瞭解用於存取您的管理員和店面的Commerce URL和帳戶認證。
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
TQID: https://experienceleague.adobe.com/8IGacP581jwpVtFnCFXRrG5vuIwCJaAUnbliitMHuf8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: d41d3a54-9721-475c-abd6-295bebfba9e4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 373
ht-degree: 0%

---

# 登入憑證和URL

繼續進行設定之前，請確定您具備存取存放區管理員和Commerce帳戶所需的資訊。

## 店面URL

您的[店面](storefront.md)位址通常是指派給您IP位址的網域。 有些存放區會安裝在根目錄或最上方的目錄。 其他則是安裝在根目錄下方的目錄中。 存放區可能位在與主要網域相關聯的子網域中。 存放區的URL看起來可能像下列其中一項：

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

如果您還沒有網域，您的商店URL會包含一系列四個數字，每個數字以&#x200B;_點狀四_&#x200B;標籤法以句點分隔。

## 管理員URL

您的商店[Admin](admin.md)的位址是在安裝期間設定的。 預設位址與您的商店相同，但結尾是`/admin`。 雖然本指南中的範例使用預設目錄，但最佳實務是從商店專屬的位置執行管理員。

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce]帳戶

您的[Commerce帳戶](commerce-account-create.md)可讓您存取產品與服務、帳戶設定、帳單歷史記錄及支援資源的相關資訊。 若要存取您的帳戶，請前往主要Commerce網站，然後按一下右上角的&#x200B;**[!UICONTROL My Account]**。

## 客戶帳戶

當您在商店中學習時，請務必設定測試[客戶帳戶](../customers/account-dashboard.md)，以便從客戶的角度體驗商店和結帳過程。

## 範例資料

僅[!BADGE 個PaaS]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/commerce/user-guides/product-solutions" tooltip="僅適用於雲端專案（Adobe管理的PaaS基礎結構）和內部部署專案的Adobe Commerce 。"}

Adobe提供範例資料集，其中包含超過250項產品（其中約200項為可設定產品）、類別、促銷價格規則、CMS頁面、橫幅等的範例商店。 範例資料使用店面上的&#x200B;_Luma_&#x200B;主題。 [安裝此範例資料](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html?lang=zh-Hant)是選擇性的，但有助於測試和開發電子商務業務的自訂專案。
