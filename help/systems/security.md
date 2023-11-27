---
title: 安全性
description: 瞭解可用於保護存放區和資料的工具，以及在偵測到危害時安全性行動計畫的准則。
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: 671ec7015c37b24ca0acc615ae3715b8b870a453
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# 安全性

有多種方式可保護您的存放區安全並維護您的資料安全性：

- 設定 [雙因素驗證](security-two-factor-authentication.md)
- 實作 [驗證碼](security-captcha.md) 或 [reCAPTCHA](security-google-recaptcha.md)
- 設定 [安全性掃描](security-scan.md) Adobe Commerce或Magento Open Source安裝中每個網域的資訊。

造訪 [安全中心](https://helpx.adobe.com/security.html){：target=&quot;_blank&quot;}並加入安全性警報登入，取得有關潛在漏洞的最新消息。 如需安全性最佳實務的相關資訊，請參閱 [保護您的Commerce網站和基礎架構](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) 在 _實施行動手冊_.

>[!NOTE]
>
>已啟用的存放區 [!DNL Adobe Identity Management Services] (IMS)驗證已停用原生Adobe Commerce和Magento Open Source 2FA。 使用Adobe憑證登入其Commerce執行個體的管理員使用者不需要重新驗證許多管理員工作。 當管理員使用者登入目前的工作階段時，驗證會由Adobe IMS處理。 另請參閱 [[!DNL Adobe Identity Management Service] (IMS)整合概述](../getting-started/adobe-ims-integration-overview.md).

![安全中心](./assets/product-security-home.png){width="700" zoomable="yes"}

## 安全性行動計畫

如果您懷疑您的Adobe Commerce或Magento Open Source網站受到危害，請立即遵循此行動計畫。

1. **診斷**：執行掃描以建立Commerce商店的安全性狀態。 商務 [安全性掃描](security-scan.md) 是Adobe提供的免費服務，可讓您監視商務網站是否有已知的安全性風險和惡意程式，並接收安全性通知。

1. **清除**：聘用 [合格的顧問](https://solutionpartners.adobe.com/s/directory/?partner_type=1) 或線上服務，清除網站上的所有惡意程式碼。 有些Commerce社群成員建議 [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). 檢查 `/media` 剩餘可執行程式碼的資料夾。 移除所有未知的管理員使用者並重設所有管理員密碼。

1. **Protect**：使用最新版本保持您的Commerce安裝為最新。 如果您使用較舊的版本，請在所有可用的安全性修補程式時套用。 檢閱並關注 [商務安全性最佳實務](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). 訂閱 [Commerce安全性警報](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **報告**：如果您認為已在Commerce中發現特定漏洞， [開啟Adobe的問題](https://hackerone.com/adobe?type=team) 並包含技術細節。

1. **升級**：為了讓您完全安心，全年無休的支援可讓您完全安心，請規劃您的升級至 [雲端架構上的Adobe Commerce](https://business.adobe.com/products/magento/cloud-delivery.html) 立即。
