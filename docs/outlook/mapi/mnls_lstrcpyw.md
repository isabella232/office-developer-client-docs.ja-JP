---
title: MNLS_lstrcpyW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a0f92c2d-b5ba-4558-b8a2-484b2db32bec
description: '最終更新日: 2012 年 6 月 18 日'
ms.openlocfilehash: ad7323d02a8a3f080614f09b610175976cd4c01f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584039"
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

