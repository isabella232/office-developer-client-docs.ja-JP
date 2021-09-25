---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: 指定したカテゴリのアカウントの順序を変更します。
ms.openlocfilehash: 5197cc484d0c410367c06d8c28dce9b62c73411d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617098"
---
# <a name="iolkaccountmanagersetorder"></a>IOlkAccountManager::SetOrder

指定したカテゴリのアカウントの順序を変更します。
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT SetOrder(
    const CLSID * pclsidCategory,
    DWORD cAccts,
    DWORD rgAccts[]
);

```

## <a name="parameters"></a>パラメーター

_pclsidCategory_
  
> [in]順序を設定するカテゴリ クラス ID。 この値は、次のいずれかである必要があります。
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
_cAccts_
  
> [in]アカウントの数。
    
_rgAccts_
  
> [in]アカウントの ID の配列。 配列のサイズは  _cAccts です_。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_ACCT_WRONG_SORT_ORDER  <br/> |新しい並べ替え順序のアカウント数は、古い並べ替え順序とは異なります。  <br/> |
|E_INVALIDARG  <br/> |いくつかの引数は無効です。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>注釈

呼び出し元は、配列ポインター  _prgAccts_ および  _prgAccts_ が指す配列のメモリを割り当てる。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

