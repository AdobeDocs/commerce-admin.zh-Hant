---
title: Google reCAPTCHA Enterprise
description: 瞭解如何設定Google reCAPTCHA Enterprise以保護您的Adobe Commerce as a Cloud Service店面免受機器人和詐騙活動的傷害。
role: Admin
feature: Configuration, Security
source-git-commit: 5181e6dcbffdca87dd6c376c36f7c9d0a3fbc015
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform)使用最適化風險分析和機器學習來區分人類使用者和機器人，為您的Adobe Commerce as a Cloud Service店面提供進階機器人保護。 這有助於防止網站上的詐騙活動、垃圾郵件和濫用。

>[!NOTE]
>
>此功能不為管理員提供reCAPTCHA支援。

如需設定其他Google reCAPTCHA版本的資訊，請參閱[Google reCAPTCHA V3和V2](security-google-recaptcha.md)。

## 功能

Google reCAPTCHA Enterprise包含下列功能：

- **進階機器人偵測**：使用Google Cloud的機器學習模型來進行卓越的機器人偵測
- **風險分數分析**：提供每個互動的詳細風險分數(0.0-1.0)
- **可設定的臨界值**：設定每個租使用者的最低可接受風險分數
- **多租使用者支援**：每個租使用者設定與隔離的Google雲端專案
- **加密的認證**：服務帳戶認證已加密儲存在資料庫中
- **表單保護**：保護所有標準Commerce表單，包括登入、結帳、產品評論等。

## 先決條件

您需要下列資源，才能為Adobe Commerce as a Cloud Service店面設定Google reCAPTCHA Enterprise：

- 已啟用reCAPTCHA Enterprise的作用中Google雲端帳戶。
- 存取Google Cloud Console以建立和管理reCAPTCHA Enterprise金鑰。

在多租使用者Adobe Commerce as a Cloud Service安裝中，每個租使用者都必須有自己的Google Cloud專案和reCAPTCHA Enterprise金鑰。

## 步驟1：設定Google reCAPTCHA Enterprise

請依照這些一般步驟來設定店面的Google reCAPTCHA Enterprise 。 如需詳細指示，請參閱[Google reCAPTCHA Enterprise檔案](https://docs.cloud.google.com/recaptcha/docs/overview)。

1. [為您的reCAPTCHA Enterprise實作建立Google Cloud專案](https://developers.google.com/workspace/guides/create-project)。

1. 啟用[reCAPTCHA Enterprise API](https://docs.cloud.google.com/recaptcha/docs/prepare-environment)。

1. 建立以分數為基礎的reCAPTCHA Enterprise [網站金鑰](https://docs.cloud.google.com/recaptcha/docs/choose-key-type)。

1. 建立具有`roles/recaptchaenterprise.admin` IAM角色的服務帳戶。

1. 下載服務帳戶JSON金鑰檔案，該檔案包含使用Google reCAPTCHA Enterprise驗證Adobe Commerce as a Cloud Service店面所需的認證。

## 步驟2：為店面設定Google reCAPTCHA

1. 在左側面板的&#x200B;_[!UICONTROL Security]_&#x200B;下，選擇&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**。

1. 完成&#x200B;**[!UICONTROL reCAPTCHA Enterprise]**&#x200B;區段，如下所示。

   - 針對&#x200B;**[!UICONTROL Site Key]**，請從Google Cloud Console複製並貼上您的reCAPTCHA Enterprise網站金鑰。

   - 針對&#x200B;**[!UICONTROL Google Cloud Project ID]**，從您的Google Cloud專案複製並貼上專案ID。

   - 針對&#x200B;**[!UICONTROL Service Account JSON]**，複製您在[步驟1：設定Google reCAPTCHA Enterprise](#step-1-set-up-google-recaptcha-enterprise)中下載的服務帳戶JSON金鑰檔案內容。

   - 針對&#x200B;**[!UICONTROL Minimum Score Threshold]**，輸入最低分數(0.0-1.0)，以識別何時將使用者互動標示為潛在風險；其中1.0是典型的使用者互動，而0.0可能是機器人。

   - 針對&#x200B;**[!UICONTROL Badge Position]**，選擇每個頁面上隱藏的reCAPTCHA徽章位置。 選項： `Inline` / `Bottom Right` / `Bottom Left`。

   - 針對&#x200B;**[!UICONTROL Theme]**，請選擇`Light Theme` （預設）或`Dark Theme`以決定Google reCAPTCHA方塊的樣式。

   - 針對&#x200B;**[!UICONTROL Language Code]**，輸入[雙字元代碼](https://developers.google.com/recaptcha/docs/language)，指定用於Google reCAPTCHA文字與訊息的語言。

   - 若為&#x200B;**[!UICONTROL Validation Failure Message]**，可選擇在驗證失敗時變更店面顯示的訊息。


1. 展開&#x200B;**[!UICONTROL Storefront]**&#x200B;區段，並將您要保護的每個店面表單設定為&#x200B;**[!UICONTROL reCAPTCHA Enterprise]**。

   {{recaptcha-forms-list}}

   ![店面選項組態](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 步驟3：儲存設定

1. 組態設定完成後，按一下&#x200B;**[!UICONTROL Save Config]**。

1. 在工作區頂端的訊息中，按一下&#x200B;**[!UICONTROL Cache Management]**&#x200B;並重新整理每個無效的快取。
