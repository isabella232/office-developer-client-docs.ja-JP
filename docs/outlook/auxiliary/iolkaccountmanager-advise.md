---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: クライアントをアカウント マネージャーに登録して、すべてのアカウントに関する通知を受け取る。
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427711"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

クライアントをアカウント マネージャーに登録して、すべてのアカウントに関する通知を受け取る。
  
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
  
> [in]アカウント マネージャーがクライアントに通知を送信するために使用する [IOlkAccountNotify](iolkaccountnotify.md) インターフェイス。 
    
_pdwCookie_
  
> [out]アカウントの [登録を削除するときに IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) が使用する Cookie。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_INVALIDARG  <br/> |無効な引数が指定されています。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

