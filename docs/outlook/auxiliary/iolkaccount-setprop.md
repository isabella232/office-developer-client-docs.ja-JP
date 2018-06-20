---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: 指定したアカウントのプロパティの値を設定します。
ms.openlocfilehash: 2bb8a323f5f3399b9eac1cfdf9ac18faddfdb259
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799433"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

指定したアカウントのプロパティの値を設定します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>Parameters

_dwProp_
  
> [in]設定するアカウントのプロパティのプロパティ タグです。
    
_pVar_
  
> [in]指定したプロパティの値です。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |メソッドの呼び出しに成功しました。  <br/> |
|E_INVALIDARG  <br/> |プロパティの無効なタグが指定されました。  <br/> |
   
## <a name="remarks"></a>備考

[IOlkAccount::SaveChanges](iolkaccount-savechanges.md)を使用して、アカウントのプロパティの値に変更を保存します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

