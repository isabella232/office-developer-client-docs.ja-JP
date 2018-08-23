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
ms.openlocfilehash: 1135a8e07bf94a200d06db8b692ee39dfdb78272
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588889"
---
# <a name="mnlslstrlenw"></a>MNLS_lstrlenW

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
終端の null 文字を除く、指定した Unicode 文字列の長さを決定します。
  
> [!TIP]
> [StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)を代わりに使用してください。 
  
```cpp
int MNLS_lstrlen(
  LPCWSTR lpsz);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]チェックする null で終わる Unicode 文字列です。
    
## <a name="return-value"></a>戻り値

関数は、文字列の長さの整数を返します。 終端の null 文字を除いた文字列の文字数です。 _Lpsz_が NULL の場合は、関数は 0 を返します。 
  
## <a name="remarks"></a>注釈

この関数は、**ライブラリ**関数をラップします。 詳細については、[ライブラリ](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)を参照してください。
  
## <a name="see-also"></a>関連項目



[ライブラリ](http://msdn.microsoft.com/en-us/library/ms647492%28VS.85%29.aspx)
  
[StringCchLength](http://msdn.microsoft.com/en-us/library/ms647539%28VS.85%29.aspx)

