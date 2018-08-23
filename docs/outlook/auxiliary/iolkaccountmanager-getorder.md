---
title: IOlkAccountManagerGetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bd22026c-e4f7-2f25-0ef2-5d9539fd7eee
description: アカウントの指定したカテゴリの順序を取得します。
ms.openlocfilehash: d05e354e25d49a51b3d3f8f053c2b39dc37b333f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799476"
---
# <a name="iolkaccountmanagergetorder"></a>IOlkAccountManager::GetOrder

アカウントの指定したカテゴリの順序を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccountManager](iolkaccountmanager.md)を参照してください。
  
```cpp
HRESULT IOlkAccountManager::GetOrder (  
    const CLSID *pclsidCategory, 
    DWORD *pcAccts, 
    DWORD *prgAccts[] 
); 
```

## <a name="parameters"></a>パラメーター

_pclsidCategory_
  
> [in]順序を取得する対象のカテゴリのクラス ID です。 値は、次のいずれかする必要があります。
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_pcAccts_
  
>  [out]アカウントの数です。 
    
_prgAccts_
  
> [out]アカウントの配列へのポインター。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しに成功しました  <br/> |
|E_INVALIDARG  <br/> |いくつかの引数は無効です。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>注釈

このメソッドを呼び出す前に呼び出し元はである*prgAccts*ポイントの配列ののみ、配列のポインター *prgAccts*がないメモリを割り当てます。 このメソッドから制御が戻った後、呼び出し元は、 *prgAccts*に割り当てられたメモリを解放するのには[IOlkAccountManager::FreeMemory](iolkaccountmanager-freememory.md)を使用する必要があります。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager::SetOrder](iolkaccountmanager-setorder.md)

