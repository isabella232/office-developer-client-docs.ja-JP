---
title: MNLS_lstrlenW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d342a956-1164-4c9c-b0bb-7a0b72dc97fc
description: '最終更新日: 2012 年2月21日'
ms.openlocfilehash: 31f699d1193e55a88e57a0f491658e0d537ef75d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338466"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定した Unicode 文字列の長さ (終端の null 文字を除く) を指定します。
  
> [!TIP]
> 代わりに、 [stringcchlength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)の使用を検討してください。 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> 順番チェックする null で終了する Unicode 文字列。
    
## <a name="return-value"></a>戻り値

関数は、文字列の長さの整数を返します。 文字列の文字数で、終端の null 文字は含みません。 _lpsz_が NULL の場合、この関数は0を返します。 
  
## <a name="remarks"></a>解説

この関数は、 **lstrlen**関数をラップします。 詳細については、「 [lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)」を参照してください。
  
## <a name="see-also"></a>関連項目



[lstrlen](https://msdn.microsoft.com/library/ms647492%28VS.85%29.aspx)
  
[stringcchlength](https://msdn.microsoft.com/library/ms647539%28VS.85%29.aspx)

