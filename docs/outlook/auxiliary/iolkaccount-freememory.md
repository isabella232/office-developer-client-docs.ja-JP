---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: IOlkAccount インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: 5c8c0952c3014e3088e30565fdfed377d943f126
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576559"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

[IOlkAccount](iolkaccount.md)インターフェイスによって割り当てられたメモリを解放します。 
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>パラメーター

_pv_
  
> [in]解放するメモリへのポインター。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

[IOlkAccount::GetProp](iolkaccount-getprop.md)によって割り当てられたメモリを解放するには、このメソッドを使用します (指定したアカウント プロパティの値がバイナリまたは文字列型の場合) と[IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)です。
  
## <a name="see-also"></a>関連項目

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

