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
ms.openlocfilehash: 4d3210c098d0a7c83721798c8c32ffd9f1e5ebb4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575463"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
文字列をバッファーにコピーします。
  
> [!CAUTION]
> 使用しないでください。 [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx)を代わりに使用してください。 
  
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
  
## <a name="remarks"></a>注釈

この関数は、 **lstrcpy**関数をラップします。 詳細については、 [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)を参照してください。
  
## <a name="see-also"></a>関連項目



[lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

