---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: 指定された account プロパティの値を設定します。
ms.openlocfilehash: 94134cee7886177ab840a6caff7d70d65bf9d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322254"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

指定された account プロパティの値を設定します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>パラメーター

_dwprop_
  
> 順番設定する account プロパティのプロパティタグ。
    
_pvar_
  
> 順番指定したプロパティの値を指定します。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |メソッドの呼び出しが成功しました。  <br/> |
|E_INVALIDARG  <br/> |無効なプロパティタグが指定されました。  <br/> |
   
## <a name="remarks"></a>解説

[IOlkAccount:: SaveChanges](iolkaccount-savechanges.md)を使用して、アカウントプロパティの値に対する変更を保存します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

