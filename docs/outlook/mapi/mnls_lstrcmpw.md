---
title: MNLS_lstrcmpW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d26c59d7-c839-426f-8693-727fc6bef67e
description: '最終更新日: 2012 年6月18日'
ms.openlocfilehash: 03b0eb794b07bc56ec6dce4a567d89294b2c908a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356841"
---
# <a name="mnlslstrcmpw"></a>MNLS_lstrcmpW

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2つの Unicode 文字列を比較します。
  
```cpp
int MNLS_lstrcmpW(
  LPCWSTR lpString1,
  LPCWSTR lpString2);
```

## <a name="parameters"></a>パラメーター

 _lpString1_
  
> 順番比較する最初の Unicode 文字列へのポインター。
    
 _lpString2_
  
> 順番比較する2番目の Unicode 文字列へのポインター。
    
## <a name="return-value"></a>戻り値

CSTR_EQUAL 以外の**MNLS_CompareStringW**への同等の呼び出しについて記述されている値を返します。 
  
## <a name="remarks"></a>解説

 _MNLS_lstrcmpW_は、getuserdefaultlcid のロケールで[MNLS_CompareStringW](mnls_comparestringw.md)を呼び出し、フラグに0、cch1 および cch2 に-1 を呼び出して比較を実行します。 
  
## <a name="see-also"></a>関連項目



[getuserdefaultlcid](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

