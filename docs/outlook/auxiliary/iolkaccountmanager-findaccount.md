---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: プロパティ値でアカウントを検索します。
ms.openlocfilehash: d09bce88413f85ee3ccc332c3cb88bb545a0ccaf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322079"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

プロパティ値でアカウントを検索します。
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FindAccount (  
    DWORD dwProp, 
    ACCT_VARIANT *pVar, 
    IOlkAccount **ppAccount 
);
```

## <a name="parameters"></a>パラメーター

_dwprop_
  
> 順番検索するプロパティ。 [PROP_ACCT_ID](prop_acct_id.md)または[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)である必要があります。
    
_pvar_
  
> 順番一致する値を指定します。
    
_ppaccount_
  
> 読み上げアカウントが見つかりました。 このオブジェクトは、 [IOlkAccount](iolkaccount.md)インターフェイスをサポートします。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定されたアカウントが見つかりません。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [ACCT_VARIANT](acct_variant.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

