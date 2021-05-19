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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356841"
---
# <a name="mnls_lstrcmpw"></a>MNLS_lstrcmpW

 
  
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

呼び出しと同等の呼び出しに対して説明されている値を **返MNLS_CompareStringWを** 除CSTR_EQUAL。 
  
## <a name="remarks"></a>注釈

 _MNLS_lstrcmpW_ は、getUserDefaultLCID [の](mnls_comparestringw.md) ロケールで MNLS_CompareStringW を呼び出し、フラグに 0、cch1 と cch2 の場合は -1 を呼び出して比較を実行します。 
  
## <a name="see-also"></a>関連項目



[GetUserDefaultLCID](https://msdn.microsoft.com/library/dd318135%28VS.85%29.aspx)

