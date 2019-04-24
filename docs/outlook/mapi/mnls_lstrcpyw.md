---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: '最終更新日: 2012 年6月18日'
ms.openlocfilehash: 1a1cf0a607dd4b57353eda74f9b14965e110c071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341728"
---
# <a name="mnlslstrcpyw"></a>MNLS_lstrcpyW

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
文字列をバッファーにコピーします。
  
> [!CAUTION]
> 使用しないでください。 代わりに、 [stringcchcopy](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx)を使用することを検討してください。 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>パラメーター

lpString1
  
> 読み上げlpString2 パラメーターによって示される文字列の内容を受信するバッファー。
    
lpString2
  
> 順番コピーする null で終わる文字列を指定します。
    
## <a name="return-value"></a>戻り値

関数が正常に終了した場合、戻り値はバッファーへのポインターです。
  
関数が失敗した場合、戻り値は null で、lpString1 を null で終了することはできません。
  
## <a name="remarks"></a>解説

この関数は、 **lstrcpy**関数をラップします。 詳細については、「 [lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)」を参照してください。
  
## <a name="see-also"></a>関連項目



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

