---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: '最終更新日: 2012 年 2 月 21 日'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338466"
---
# <a name="mnls_lstrlenw"></a>MNLS_lstrlenW

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
終端の null 文字を除く、指定した Unicode 文字列の長さを指定します。
  
> [!TIP]
> 代わりに [StringCchLength の使用を](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx) 検討してください。 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]チェックする null 終端 Unicode 文字列。
    
## <a name="return-value"></a>戻り値

この関数は、文字列の長さを持つ整数を返します。 これは、終端の null 文字を除く、文字列内の文字の数です。 _lpsz が_ NULL の場合、関数は 0 を返します。 
  
## <a name="remarks"></a>注釈

この関数は **、lstrlen 関数をラップ** します。 詳細については [、「lstrlen」を参照してください](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)。
  
## <a name="see-also"></a>関連項目



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

