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
ms.openlocfilehash: 2e4ae22ace37455c9ccb9d8ff2a7f07a48132234
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801657"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**適用されます**: Outlook 
  
文字列をバッファーにコピーします。
  
> [!CAUTION]
> 使用しないでください。 [StringCchCopy](http://msdn.microsoft.com/en-us/library/ms647527%28VS.85%29.aspx)を代わりに使用してください。 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>Parameters

lpString1
  
> [out]LpString2 パラメーターが指す文字列の内容を受信するバッファーです。
    
lpString2
  
> [in]Null で終わる文字列をコピーします。
    
## <a name="return-value"></a>�߂�l

関数が成功した場合は、バッファーへのポインターを返します。
  
関数が失敗した場合、NULL が戻り値と lpString1 できない場合があります null で終わる。
  
## <a name="remarks"></a>備考

この関数は、 **lstrcpy**関数をラップします。 詳細については、 [lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)を参照してください。
  
## <a name="see-also"></a>関連項目



[lstrcpy](http://msdn.microsoft.com/en-us/library/ms647490%28VS.85%29.aspx)

