---
title: 出貨承運商設定
description: 瞭解您商店所提供的商業運送帳戶支援。
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
TQID: https://experienceleague.adobe.com/zKN3BQWHywAOLJ-zaJX1-8b7aAYxtzl8v9J7uJG1rFg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-wordcount: 496
ht-degree: 0%

---

# 出貨承運商設定

如果您有商業帳戶與支援的電信業者，您可以在結帳時方便客戶選擇該電信業者。 費率會自動下載，因此您不需要查詢資訊。

>[!NOTE]
>
>請參閱[Commerce Marketplace](../getting-started/commerce-marketplace.md)，以取得Commerce安裝的其他送貨服務。

您必須先完成下列步驟，才能為客戶提供精選的運送公司：

- 設定[送貨設定](shipping-settings.md)以建立商店的原點。

- 針對您要提供的每個電信業者服務進行設定。

   - [**UPS**](ups.md) - United Parcel Service (UPS)提供國內及國際的陸運及空運服務，服務對象超過220個國家。
   - [**USPS**](usps.md) — 美國郵政服務(USPS)是美國政府的獨立郵遞服務。 USPS提供國內及國際的陸運及空運服務。
   - [**FedEx**](fedex.md) - FedEx提供國內及國際的陸運及空運服務，服務對象超過220個國家。
   - [**DHL**](dhl.md) - DHL提供整合式國際服務，以及客製化且以客戶為中心的解決方案，用於管理及運送信件、貨物及資訊。

## 維度權數

維度重量（有時稱為體積重量）是常見的產業作法，其運輸價格是以重量與包裝體積的組合為基礎。 簡單來說，尺寸權重會根據包裹在承運商的貨物區域中佔用的空間量來決定出貨率。 尺寸重量通常用於封裝與其體積相比相對較輕時。

所有主要承運商都會將維度重量套用至部分出貨。 不過，維度加權訂價套用的方式因承運商而異。 如果貴公司的出貨量很大，即使出貨價格稍有差異，一年內也可能折算成數千美元。

## 設定

每個電信業者的組態選項會有所不同。 但是，所有步驟都需要以下步驟：

1. 開啟與承運商的運送帳戶。

1. 在商店的設定中，輸入您的帳號或使用者ID，以及連線至其系統的閘道URL。

### USPS Web Tools API淘汰

Adobe Commerce版本2.4.6、2.4.7和2.4.8使用舊版網站工具API，與USPS進行現成可用的出貨整合。 USPS推出了USPS API，這是REST型平台，用來取代舊版網頁工具API。

自2026年1月25日起，USPS已淘汰舊版網站工具API。 在此日期之後，所有對Web Tools API的請求都將失敗。

若要避免USPS送貨服務中斷，請升級至最新版本的Adobe Commerce，或採取下列動作：

- 套用[USPS REST API移轉品質修補程式](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210)以新增與USPS REST API整合的支援。

- 更新Commerce USPS設定以使用REST API：

   - [USPS出貨承運商設定](usps.md)

   - [送貨標籤設定](shipping-label-create.md)

