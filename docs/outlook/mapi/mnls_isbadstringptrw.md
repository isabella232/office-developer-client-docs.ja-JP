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
ms.openlocfilehash: 0e64df38afdb8ecce35eb0151d36dde3da35f0a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356855"
---
# <a name="mnls_isbadstringptrw"></a>MNLS_IsBadStringPtrW

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ワイド文字列へのポインターが有効な値を確認します。
  
```cpp
BOOL MNLS_IsBadStringPtrW(
  LPCWSTR lpsz,
  UINT ucchMax);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]ワイド文字列へのポインター。
    
 _ucchMax_
  
> [in]ターミネーターを含む文字の文字列の最大長。
    
## <a name="return-value"></a>戻り値

文字列が正しい場合は true のブール型 (Boolean) の値を返します。
  
## <a name="remarks"></a>注釈

この関数は [IsBadStringPtr をラップします](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx)。 詳細については [、「IsBadStringPtr」を参照してください](https://msdn.microsoft.com/library/aa366714%28VS.85%29.aspx)。
  

