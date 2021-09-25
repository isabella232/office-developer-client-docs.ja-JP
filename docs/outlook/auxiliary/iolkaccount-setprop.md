---
title: IOlkAccountSetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 883b1c5d-47dd-a006-b5f1-130691bdd019
description: 指定したアカウント プロパティの値を設定します。
ms.openlocfilehash: 8fd8eb0acc51d457911799e751451e7600202d5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617147"
---
# <a name="iolkaccountsetprop"></a>IOlkAccount::SetProp

指定したアカウント プロパティの値を設定します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
```cpp
HRESULT IOlkAccount::SetProp(  
    DWORD dwProp, 
    ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>パラメーター

_dwProp_
  
> [in]設定する account プロパティのプロパティ タグ。
    
_pVar_
  
> [in]指定したプロパティの値。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |メソッドの呼び出しが成功しました。  <br/> |
|E_INVALIDARG  <br/> |無効なプロパティ タグが指定されました。  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::SaveChanges](iolkaccount-savechanges.md)を使用して、アカウント プロパティの値に対する変更を保存します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

