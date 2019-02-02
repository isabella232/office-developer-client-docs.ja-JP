---
title: IOlkAccountManagerInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e5ffb61-1469-bc91-f237-27d1156179cd
description: 使用のアカウント マネージャーを初期化します。
ms.openlocfilehash: 5a643a4636251afc98750be8acf47cd3bdab3847
ms.sourcegitcommit: b361919ae2d3ac000d9fcaa3030713df7062ecd4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2019
ms.locfileid: "29715341"
---
# <a name="iolkaccountmanagerinit"></a>IOlkAccountManager::Init

使用のアカウント マネージャーを初期化します。
  
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
  
> [in]アカウントのヘルパー機能を提供する[IOlkAccountHelper](iolkaccounthelper.md)インターフェイスです。 
    
_dwFlags_
  
> [in]動作を変更するフラグです。
    
   - **ACCT_INIT_NO_STORES_CHECK** -(IMAP アカウントの場合) などのアカウントが、関連付けられているストアとの同期することを防止します。 
    
   - **ACCT_INIT_NOSYNCH_MAPI_ACCTS** -により、MAPI サービス アカウントと同期します。 
   
   - **ACCT_INIT_NO_NOTIFICATIONS** : アカウント マネージャーが他のアプリケーション向けのブロードキャスト メッセージを受信することを防止します。 
   
   - **OLK_ACCOUNT_NO_FLAGS** -同期の MAPI サービス アカウントです。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_OLK_ALREADY_INITIALIZED  <br/> |**初期化**が既に呼び出されています。  <br/> |
|E_OLK_REGISTRY  <br/> |アカウント管理者に必要なレジストリ設定にアクセスできませんでした。  <br/> |
   
## <a name="remarks"></a>注釈

クライアントは、アカウント マネージャーを使用してアカウントにアクセスしたり、通知を設定する前にアカウントを初期化するために**IOlkAccountManager::Init**マネージャーを呼び出す必要があります。 Outlook は起動時にアカウントを使用して MAPI サービスを自動的に同期をするため、同期するのには特定の原因がない限り、 **ACCT_INIT_NOSYNCH_MAPI_ACCTS**を使用します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)

