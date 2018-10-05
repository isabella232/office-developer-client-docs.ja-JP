---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: '最終更新日: 2012 年 6 月 18 日'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382709"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
文字列をバッファーにコピーします。
  
> [!CAUTION]
> 使用しないでください。 [StringCchCopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx)を代わりに使用してください。 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>パラメーター

lpString1
  
> [out]LpString2 パラメーターが指す文字列の内容を受信するバッファーです。
    
lpString2
  
> [in]Null で終わる文字列をコピーします。
    
## <a name="return-value"></a>戻り値

関数が成功した場合は、バッファーへのポインターを返します。
  
関数が失敗した場合、NULL が戻り値と lpString1 できない場合があります null で終わる。
  
## <a name="remarks"></a>備考

この関数は、 **lstrcpy**関数をラップします。 詳細については、 [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)を参照してください。
  
## <a name="see-also"></a>関連項目



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

