---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315366"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
null で終わる16進数値の文字列を、符号なしの長整数型 (long) の値に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> 順番変換する null で終わる文字列へのポインター。 _lpsz_パラメーターは、65536文字以下にする必要があります。 
    
## <a name="return-value"></a>戻り値

 **ulfromszhex**は、符号なし長整数型 (long) の値を返します。 文字列の先頭に少なくとも1つの16進数が指定されていない場合は、0が返されます。 
  
## <a name="remarks"></a>解説

**ulfromszhex**関数は、16進数ではない文字列の最初の文字に達したときに変換を停止します。 たとえば、文字列 "5a" が指定されている場合、 **ulfromszhex**は整数値90を返します。 文字列 "5g5h" が指定されている場合、この関数は整数値5を返します。 文字列 "g5h5" が指定されている場合、 **ulfromszhex**は0を返します。 
  
 **ulfromszhex**は、発音区別の違いに注意していますが、' a ' ~ ' f ' の両方と ' a ' ~ ' a ' を16進数の数字に対して使用することができます。 Unicode および DBCS 形式の文字列がサポートされています。 _lpsz_の長さの制限は、文字である必要があり、必ずしもバイトではありません。 
  

