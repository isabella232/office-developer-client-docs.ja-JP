---
title: IOlkAccountManagerSetOrder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e219adf6-e591-72e6-b9bd-2fc62eb5142d
description: 指定したカテゴリのアカウントの順序を変更します。
ms.openlocfilehash: 29dfe4fd1bda9e323481297167361650c3b3a173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422860"
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

