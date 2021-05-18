---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: 使用するアカウント マネージャーを初期化します。
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322037"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

使用するアカウント マネージャーを初期化します。
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Init (  
    IOlkAccountHelper *pAcctHelper, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>パラメーター

_pAcctHelper_
  
> [in]アカウント [ヘルパー機能を提供する IOlkAccountHelper](iolkaccounthelper.md) インターフェイス。 
    
_dwFlags_
  
> [in]動作を変更するフラグです。
    
   - **ACCT_INIT_NO_STORES_CHECK** —アカウント (IMAP アカウントなど) が関連付けられたストアと同期しなからせない。 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** —MAPI サービスとアカウントの同期を防止します。 
   
   - **ACCT_INIT_NO_NOTIFICATIONS** —アカウント マネージャーが他のアプリケーション用のブロードキャスト メッセージを傍受することを防止します。 
   
   - **OLK_ACCOUNT_NO_FLAGS** —MAPI サービスをアカウントと同期します。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**Init** は既に呼び出されています。  <br/> |
|E_OLK_REGISTRY  <br/> |アカウント マネージャーは、必要なレジストリ設定にアクセスできません。  <br/> |
   
## <a name="remarks"></a>注釈

アカウント マネージャーを使用してアカウントにアクセスするか、通知を設定する前に、クライアントは **IOlkAccountManager::Init** を呼び出してアカウント マネージャーを初期化する必要があります。 MAPI サービスOutlook起動時にアカウントと自動的に同期する場合は、特定の同期 **ACCT_INIT_NOSYNCH_MAPI_ACCTS** を使用します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)

