---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: すべてのアカウントの通知をアカウント マネージャーでクライアントに登録解除します。
ms.openlocfilehash: cc82aa8bc3ba7f550f1f328c12a68802ef34c29c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631238"
---
# <a name="iolkaccountmanagerunadvise"></a>IOlkAccountManager::Unadvise

すべてのアカウントの通知をアカウント マネージャーでクライアントに登録解除します。 
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a>パラメーター

_dwCookie_
  
> [in] [IOlkAccountManager](iolkaccountmanager-advise.md)によって返される Cookie::Advise .
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_INVALIDARG  <br/> |いくつかの引数は無効です。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)

