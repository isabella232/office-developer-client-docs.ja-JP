---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: IOlkAccountManager インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: e51aa8dd165e9cf1d1498386387b422404c7a5d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561930"
---
# <a name="iolkaccountmanagerfreememory"></a>IOlkAccountManager::FreeMemory

[IOlkAccountManager インターフェイスによって割り当てられたメモリを解放](iolkaccountmanager.md)します。 
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a>パラメーター

_pv_
  
> [in]空きメモリへのポインター。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

[IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)によって割り当てられたメモリを解放するには、このメソッドを使用します。
  
## <a name="see-also"></a>関連項目

- [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)

