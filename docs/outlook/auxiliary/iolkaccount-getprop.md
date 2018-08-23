---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: 指定したアカウントのプロパティの値を取得します。
ms.openlocfilehash: 2c0756f416a209d37eff2209a82c298837f85f3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799416"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

指定したアカウントのプロパティの値を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>パラメーター

_dwProp_
  
> [in]取得するアカウントのプロパティのプロパティ タグです。
    
_pVar_
  
> [out]指定したプロパティの値です。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定したアカウントのプロパティが見つかりませんでした。  <br/> |
|E_INVALIDARG  <br/> |プロパティの無効なタグが指定されています。  <br/> |
   
## <a name="remarks"></a>注釈

アカウントのプロパティの値がバイナリまたは文字列型の場合、このメソッドが返されると、 [IOlkAccount::FreeMemory](iolkaccount-freememory.md)を使用して、 *pVar*を解放する必要があります。
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

