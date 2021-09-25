---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7d545e93d9ebd746d50c1e5d4db55f2114551ca1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623993"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
16 進数の null 終端文字列を符号なし長整数に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]変換する null 終端文字列へのポインター。 _lpsz パラメーター_ は、65536 文字を超えることはできません。 
    
## <a name="return-value"></a>戻り値

 **UlFromSzHex は** 、符号なし長整数を返します。 文字列が 1 桁以上の 16 進数で始まる場合は、ゼロが返されます。 
  
## <a name="remarks"></a>注釈

**UlFromSzHex** 関数は、16 進数ではない文字列の最初の文字に達すると、変換を停止します。 たとえば、文字列 "5a" を指定すると **、UlFromSzHex** は整数値 90 を返します。 文字列 "5g5h" を指定すると、整数値 5 が返されます。 文字列 "g5h5" を指定すると **、UlFromSzHex は** ゼロを返します。 
  
 **UlFromSzHex** は、二次的な違いには敏感ですが、16 進数の場合は 'a' から 'f' と 'A' から 'F' の両方を使用できます。 Unicode および DBCS 形式の文字列がサポートされています。 _lpsz の長さの制限は_ 文字で、必ずしもバイトではありません。 
  

