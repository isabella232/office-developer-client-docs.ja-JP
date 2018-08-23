---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: クライアントをすべてのアカウントに関する通知のアカウント マネージャーに登録します。
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799462"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

クライアントをすべてのアカウントに関する通知のアカウント マネージャーに登録します。
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a>パラメーター

_pNotify_
  
> [in]クライアントに通知を送信するのには、アカウント マネージャーを使用する[IOlkAccountNotify](iolkaccountnotify.md)インターフェイスです。 
    
_pdwCookie_
  
> [out][IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)は、アカウントの登録を削除するときに使用する cookie です。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_INVALIDARG  <br/> |無効な引数が用意されています。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

