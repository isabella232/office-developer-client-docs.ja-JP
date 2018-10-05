---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: '最終更新日: 2012 年 6 月 18 日'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386349"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2 つの Unicode 文字列を比較します。
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>パラメーター

 _lpString1_
  
> [in]比較する最初の Unicode 文字列へのポインター。
    
 _lpString2_
  
> [in]比較する 2 番目の Unicode 文字列へのポインター。
    
## <a name="return-value"></a>戻り値

CSTR_EQUAL を除く**MNLS_CompareStringW**に同等の呼び出しの値を返します。 
  
## <a name="remarks"></a>備考

 _MNLS_lstrcmpW_ GetUserDefaultLCID、フラグ、0 のロケールで[MNLS_CompareStringW](mnls_comparestringw.md)を呼び出すことによって比較を実行して cch1 と cch2 の場合は-1 です。 
  
## <a name="see-also"></a>関連項目



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

