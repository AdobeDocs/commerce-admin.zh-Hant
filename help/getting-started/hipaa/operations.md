---
title: 作業
description: 移轉至HIPAA就緒產品並使用次要中繼環境進行疑難排解的准則。
source-git-commit: 999d3126ae368000fc2c58c315473739012f3934
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# 作業

使用這些准則來瞭解如何移轉至Adobe Commerce的HIPAA就緒產品，以及使用`staging_for_support`環境進行疑難排解。

## 移轉

從非HIPAA Commerce產品移轉至HIPAA就緒產品的客戶必須遵循以下准則：

1. **刪除現有的資料空間**：在移轉之前，必須刪除所有現有的資料空間，以防止敏感資料和非敏感資料在Adobe Commerce SaaS層級中混合使用。 建立支援票證以刪除資料空間。
1. **設定新環境**：新HIPAA Commerce執行個體中的[Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas)安裝程式只能在刪除資料空間之後設定。 新的HIPAA SaaS環境只應在刪除舊資料空間後使用。 Commerce服務聯結器的設定會自動觸發新SaaS資料空間的建立。
1. **移轉策略**：刪除SaaS資料空間是無法復原的程式，而且會刪除您的所有目錄資料和相關設定。 如果您想要結轉任何舊資料或設定，則必須制定移轉策略。 此策略是商人的責任。 只有在完成移轉資料備份（如果適用）後，才應建立用於刪除現有資料空間的支援票證。

>[!NOTE]
>若要刪除現有資料空間，客戶必須建立名為「HIPAA移轉：刪除SaaS資料空間」的Adobe Commerce支援票證、提供其`MAGEID`，並提供需要刪除的SaaS專案ID。

## 疑難排解Adobe Commerce支援

Adobe Commerce HIPAA就緒產品隨附其他`staging_for_support`環境，供Adobe Commerce支援團隊用於疑難排解目的。

客戶必須確定`staging_for_support`環境：

- 不包含任何敏感資料，例如但不限於受保護的健康資訊(PHI)。
- 不得用於任何生產活動。
- 不得指定與`staging_for_support`不同的名稱，以避免混淆。
- 在生產環境中使用程式碼和設定保持最新，以確保在儘可能靠近生產的環境中執行疑難排解。

## Commerce服務

- **不符合HIPAA標準的Commerce服務** — 客戶不得使用Adobe Commerce服務，例如即時搜尋、產品Recommendations、付款服務、Sales Channel或Commerce Intelligence，因為這些服務未符合HIPAA標準。 客戶應該只使用[HIPAA就緒的服務](overview.md)。

- **資料連線** — 只有[資料連線](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview)延伸模組中的後台收集器可以使用HIPAA。 客戶不應將PHI傳送至不符合HIPAA要求的資料連線服務，例如店面活動和Audience Activation。 客戶必須確定已停用店面資料收集。

- **目錄服務** — 根據設計，[目錄服務](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/overview)不會處理PHI，所以它不在HIPAA整備稽核與法規遵循的範圍之內。 客戶有責任根據自身對使用案例的評估，並諮詢法律顧問，以確保他們使用此服務。 客戶也不應透過Federated Service使用目錄服務，以避免將PHI傳遞至不符合HIPAA標準的服務的風險。

- **SaaS資料匯出** — 應將[SaaS資料匯出](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview)服務設定為僅針對Adobe Commerce中符合HIPAA標準的元件傳送資料。
