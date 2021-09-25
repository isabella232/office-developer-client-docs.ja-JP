---
title: IOlkAccountGetProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5725eb52-3a78-897d-f9e3-c5a494fb78c0
description: 指定したアカウント プロパティの値を取得します。
ms.openlocfilehash: 2ab86eeaf18374a28159c6f0743e55d1664a1b31
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561951"
---
# <a name="iolkaccountgetprop"></a>IOlkAccount::GetProp

指定したアカウント プロパティの値を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
```cpp
HRESULT IOlkAccount::GetProp(  
DWORD dwProp, 
ACCT_VARIANT *pVar 
);
```

## <a name="parameters"></a>パラメーター

_dwProp_
  
> [in]取得する account プロパティのプロパティ タグ。
    
_pVar_
  
> [out]指定したプロパティの値。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定したアカウントのプロパティが見つかりません。  <br/> |
|E_INVALIDARG  <br/> |無効なプロパティ タグが指定されています。  <br/> |
   
## <a name="remarks"></a>注釈

このメソッドが返された後、account プロパティの値がバイナリ型または文字列型の場合は [、IOlkAccount::FreeMemory](iolkaccount-freememory.md)を使用して *pVar* を解放する必要があります。
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)  
- [IOlkAccount::SetProp](iolkaccount-setprop.md)

