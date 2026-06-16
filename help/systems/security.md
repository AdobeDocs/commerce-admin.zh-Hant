---
title: 安全性
description: 瞭解可用於保護存放區和資料的工具，以及在偵測到危害時安全性行動計畫的准則。
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
TQID: https://experienceleague.adobe.com/9aJ-ZVqwaIr2IJTY6e2hp3eoZe2v6sxz6WdqP2FiPTc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
subfeature_v2: id: f8ddfd3b-6194-46e8-a176-0e918039be56
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 412
ht-degree: 0%

---

# 安全性

有多種方式可保護您的存放區安全並維護您的資料安全性：

- 設定[雙因素驗證](security-two-factor-authentication.md)
- 實作[CAPTCHA](security-captcha.md)或[reCAPTCHA](security-google-recaptcha.md)
- 為Adobe Commerce或Magento Open Source安裝中的每個網域設定[安全性掃描](security-scan.md)。

>[!NOTE]
>
>已啟用[!DNL Adobe Identity Management Services] (IMS)驗證的存放區已停用原生Adobe Commerce和Magento Open Source 2FA。 使用其Adobe憑證登入其Commerce執行個體的管理員使用者，不需要重新驗證許多管理員工作。 當管理員使用者登入目前的工作階段時，驗證會由Adobe IMS處理。 請參閱[[!DNL Adobe Identity Management Service] (IMS)整合概述](../getting-started/adobe-ims-integration-overview.md)。

請造訪[安全中心](https://helpx.adobe.com/security.html){:target="_blank"}，取得有關潛在漏洞的最新消息、註冊Adobe安全通知，以及存取Adobe信任中心。

![安全中心](./assets/product-security-home.png){width="700" zoomable="yes"}

如需安全性最佳實務的相關資訊，請參閱&#x200B;_實作行動手冊_&#x200B;中的[保護您的Commerce網站和基礎結構](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)。

## 安全性行動計畫

如果您懷疑您的Adobe Commerce或Magento Open Source網站受到危害，請立即遵循此行動計畫。

1. **診斷**：執行掃描以建立Commerce存放區的安全性狀態。 Commerce [安全性掃描](security-scan.md)是Adobe提供的免費服務，可讓您監視Commerce網站是否有已知的安全性風險和惡意程式，以及接收安全性通知。

1. **清除**：請聘請[合格的顧問](https://solutionpartners.adobe.com/s/directory/?partner_type=1)或線上服務，清除網站上的所有惡意程式碼。 有些Commerce社群成員建議[[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal)。 檢查`/media`資料夾中是否有剩餘的可執行程式碼。 移除所有未知的管理員使用者並重設所有管理員密碼。

1. **保護**：使用最新版本保持您的Commerce安裝最新狀態。 如果您使用較舊的版本，請在所有可用的安全性修補程式時套用。 檢閱並遵循[Commerce安全性最佳實務](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf)。 訂閱[Commerce安全性警示](https://www.adobe.com/subscription/adbeSecurityNotifications.html)。

1. **報告**：如果您認為已在Commerce中發現特定漏洞，[請開啟Adobe的問題](https://hackerone.com/adobe?type=team)並包含技術詳細資料。

1. **升級**：為了24小時全年無休的支援讓您完全安心，請立即規劃在我們的雲端架構](https://business.adobe.com/products/magento/cloud-delivery.html)上升級至[Adobe Commerce。
