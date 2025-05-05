---
title: 管理Experience Cloud整合
description: 瞭解如何管理Experience Cloud整合及疑難排解問題
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: 15569794c1e66ba5a93e46206244e2951522923e
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# 管理Experience Cloud整合

初始啟用後，請啟用或停用Commerce Admin Unified Experience擴充功能，以管理Experience Cloud整合的狀態。

- 如果已啟用Commerce Admin Unified Experience擴充功能，且管理員帳戶已[正確布建](#manage-admin-user-accounts)，Commerce管理員可以從Adobe Experience Cloud檢視及存取可用的Commerce專案。 管理員仍可使用Commerce專案環境的管理員URL存取個別專案。

- 如果已停用Commerce Admin Unified Experience擴充功能，則會停用透過Experience Cloud存取。 管理員必須使用Commerce專案環境的管理員URL登入個別專案。

>[!WARNING]
>
>如果AdobeIdentity Management服務(IMS)整合已停用，則Experience Cloud整合會自動停用。

## 從管理員管理整合

1. 在Commerce管理員中，從左側導覽功能表選取&#x200B;**[!UICONTROL Stores]**，然後選取&#x200B;**[!UICONTROL Configuration]**，以開啟「商店設定」功能表。

1. 從[設定]功能表選取&#x200B;**[!UICONTROL Advanced > Admin]**，然後展開&#x200B;**[!UICONTROL Unified Experience option]**。

   用於Experience Cloud整合的![管理存放區設定](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. 選取&#x200B;**[!UICONTROL Enable]**&#x200B;值，以啟用或停用整合。

1. 新增或更新&#x200B;**[!UICONTROL Project Name]**&#x200B;值，以變更Commerce專案工作區中顯示的專案名稱。

1. 儲存設定。

1. 清除快取。

## 使用Adobe Commerce CLI管理整合

具有Commerce雲端專案管理員存取權的Commerce系統管理員可以使用Adobe Commerce CLI命令來管理Experience Cloud整合。

1. 從您的本機開發環境，登入雲端專案。

   ```bash
   magento-cloud login
   ```

1. 從雲端專案環境的根目錄，連線至Commerce應用程式伺服器。

   ```bash
   ssh magento-cloud
   ```

1. 檢查Admin Unified Experience擴充功能的狀態：

   ```bash
   bin/magento admin:uex:status
   ```

1. 變更擴充功能的狀態以停用整合

   - **啟用**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **停用**—`bin/magento config:set admin/unified_experience/enabled 0`

## 管理管理員使用者帳戶

所有Commerce管理員使用者都必須同時具有Commerce執行個體上的管理員帳戶和Adobe使用者帳戶(Adobe ID)，才能存取Adobe產品和服務。 兩個帳戶都必須關聯至相同的電子郵件地址。

- **Commerce管理帳戶**—[從Commerce執行個體的管理員管理Commerce管理使用者](../systems/permissions-users-all.md)。 Commerce管理員的使用者帳戶必須獲指派管理員角色。

  Commerce專案的系統管理員可以使用[SSH連線到遠端環境](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=zh-Hant#connect-to-a-remote-environment)，並使用Commerce CLI `admin:user:create`和`admin:user:unlock`命令新增或解除鎖定管理員使用者帳戶。

- **Adobe使用者帳戶** — 與Commerce執行個體相關聯之Adobe組織的管理員必須登入Adobe Admin Console，並將每個Commerce管理員的Adobe ID新增至組織。 接著，他們必須指派產品權益和許可權，才能存取Commerce應用程式。 請參閱[在Adobe Admin Console中設定Adobe Commerce使用者](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console)。

從Adobe Developer Console管理Experience Cloud整合設定的管理員，必須擁有具有系統管理員或開發人員存取權的Adobe使用者帳戶。

>[!NOTE]
>
>Adobe ID是透過Adobe建立的帳戶，是透過Experience Cloud存取產品和服務所需的帳戶。 沒有Adobe ID的Commerce管理員可以使用他們用來登入Commerce管理員的相同電子郵件地址[建立免費帳戶](https://helpx.adobe.com/tw/manage-account/using/create-update-adobe-id.html)。
