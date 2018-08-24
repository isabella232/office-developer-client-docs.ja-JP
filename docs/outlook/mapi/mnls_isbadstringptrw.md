---
title: MNLS_IsBadStringPtrW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 293a0700-b950-4fc2-a2e5-148d6c846384
description: '最終更新日: 2012 年 2 月 20 日'
ms.openlocfilehash: 0052d0bd6b485340a92cca9f22ca65c9e2442df6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589568"
---
# <a name="mnlsisbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ワイド文字列へのポインターが有効であることを確認します。
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]ワイド文字列へのポインター。
    
 _ucchMax_
  
> [in]文字列の終端文字を含む文字の最大長。
    
## <a name="return-value"></a>戻り値

ブール値、文字列が無効な場合は true を返します。
  
## <a name="remarks"></a>注釈

この関数は、 [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx)をラップします。 詳細については、 [IsBadStringPtr](http://msdn.microsoft.com/en-us/library/aa366714%28VS.85%29.aspx)を参照してください。
  

