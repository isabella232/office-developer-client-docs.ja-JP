---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: IOlkAccount インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: ce3046db29cb2cac7d7ee72a3e4e9125346a4ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799408"
---
# <a name="iolkaccountfreememory"></a>IOlkAccount::FreeMemory

[IOlkAccount](iolkaccount.md)インターフェイスによって割り当てられたメモリを解放します。 
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a>Parameters

_pv_
  
> [in]解放するメモリへのポインター。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

[IOlkAccount::GetProp](iolkaccount-getprop.md) (指定されたアカウントのプロパティの値がバイナリまたは文字列型の場合) および[IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)によって割り当てられたメモリを解放は、このメソッドを使用します。
  
## <a name="see-also"></a>関連項目

- [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)  
- [IOlkAccount::GetProp](iolkaccount-getprop.md)

