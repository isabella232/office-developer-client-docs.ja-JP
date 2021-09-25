---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: 指定したカテゴリのアカウントの順序を取得します。
ms.openlocfilehash: 3a680e7a40197a3edf22e78d4e35ac981802a193
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617112"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

指定したカテゴリのアカウントの順序を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccountManager」を参照してください。](iolkaccountmanager.md)
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>パラメーター

_pclsidCategory_
  
> [in]注文を取得するカテゴリ クラス ID。 値は、次のいずれかする必要があります。
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  [out]アカウントの数。 
    
_prgAccts_
  
> [out]アカウントの配列へのポインター。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました  <br/> |
|E_INVALIDARG  <br/> |いくつかの引数は無効です。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>注釈

このメソッドを呼び出す前に、呼び出し元は配列ポインター  *prgAccts*  のみを割り当て  *、prgAccts*  が指す配列にはメモリを割り当てない。 このメソッドが返された後、呼び出し元は [IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md) を使用して  *prgAccts*  に割り当てられたメモリを解放する必要があります。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

