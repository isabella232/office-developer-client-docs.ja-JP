---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: IOlkAccountManager インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: 85ba4d0d47eb5c879fa562e3147860533ef59f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799464"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

[IOlkAccountManager](iolkaccountmanager.md)インターフェイスによって割り当てられたメモリを解放します。 
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>パラメーター

_pv_
  
> [in]解放するメモリへのポインター。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

[IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)によって割り当てられたメモリを解放するのにには、このメソッドを使用します。
  
## <a name="see-also"></a>関連項目

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

