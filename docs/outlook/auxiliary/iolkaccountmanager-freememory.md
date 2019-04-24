---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: IOlkAccountManager インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322058"
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
  
> 順番解放するメモリへのポインター。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解説

[IOlkAccountManager:: getorder](iolkaccountmanager-getorder.md)によって割り当てられたメモリを解放するには、このメソッドを使用します。
  
## <a name="see-also"></a>関連項目

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

