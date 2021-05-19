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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341728"
---
# <a name="mnls_lstrcpyw"></a>MNLS_lstrcpyW

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
文字列をバッファーにコピーします。
  
> [!CAUTION]
> 使用しないでください。 代わりに [StringCchCopy の使用](https://msdn.microsoft.com/library/ms647527%28VS.85%29.aspx) を検討してください。 
  
```cpp
LPWSTR MNLS_lstrcpyW(
 LPWSTR lpString1,
LPCWSTR lpString2);
```

## <a name="parameters"></a>パラメーター

lpString1
  
> [out]lpString2 パラメーターが指す文字列の内容を受け取るバッファー。
    
lpString2
  
> [in]コピーする null 終端文字列。
    
## <a name="return-value"></a>戻り値

関数が成功した場合、戻り値はバッファーへのポインターです。
  
関数が失敗した場合、戻り値は NULL で、lpString1 は null 終了しない可能性があります。
  
## <a name="remarks"></a>注釈

この関数は **、lstrcpy 関数をラップ** します。 詳細については [、「lstrcpy」を参照してください](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)。
  
## <a name="see-also"></a>関連項目



[lstrcpy](https://msdn.microsoft.com/library/ms647490%28VS.85%29.aspx)

