---
title: IOlkAccountManagerFindAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 31004aec-7bd2-6e12-83eb-1a32da121c54
description: プロパティ値でアカウントを検索します。
ms.openlocfilehash: 2ec221394364ce2c747e7f9aed4ff5d8373c9b96
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564506"
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

_dwProp_
  
> [in]検索するプロパティ。 必ず[、PROP_ACCT_ID](prop_acct_id.md)またはPROP_ACCT_IS_EXCH。 [](prop_acct_is_exch.md)
    
_pVar_
  
> [in]一致する値。
    
_ppAccount_
  
> [out]見つかったアカウント。 このオブジェクトは [、IOlkAccount インターフェイスをサポート](iolkaccount.md) します。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定したアカウントが見つかりません。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
|E_OLK_PARAM_NOT_SUPPORTED  <br/> |1 つ以上のパラメーターが無効です。  <br/> |
   
## <a name="see-also"></a>関連項目

- [ACCT_VARIANT](acct_variant.md)  
- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountHelper](iolkaccounthelper.md)

