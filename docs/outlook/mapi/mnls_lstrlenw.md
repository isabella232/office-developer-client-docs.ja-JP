---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: '最終更新日: 2012 年 2 月 21 日'
ms.openlocfilehash: 32d9dfef7a03c16998b007a1bddca49ed04118c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575408"
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

