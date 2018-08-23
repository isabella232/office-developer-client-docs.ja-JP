---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: プロパティの値によっては、アカウントを検索します。
ms.openlocfilehash: a7d016ab7e265e547b33940c16f96979bd5fa87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799469"
---
# <a name="iolkaccountmanagerfindaccount"></a>IOlkAccountManager::FindAccount

プロパティの値によっては、アカウントを検索します。
  
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

_dwProp_
  
> [in]検索するプロパティです。 [PROP_ACCT_ID](prop_acct_id.md)または[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)である必要があります。
    
_pVar_
  
> [in]一致する値。
    
_ppAccount_
  
> [out]アカウントは見つかりませんでした。 このオブジェクトは、 [IOlkAccount](iolkaccount.md)インターフェイスをサポートします。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定されたアカウントが見つかりませんでした。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [ACCT_VARIANT](acct_variant.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

