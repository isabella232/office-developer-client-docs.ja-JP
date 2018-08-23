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
ms.openlocfilehash: d5ba7e7bc52ba041e9fe6c9a01b35dc91d3b947b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804163"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**適用対象**: Outlook 
  
16 進数の null で終わる文字列を符号なし長整数に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]変換される null で終わる文字列へのポインター。 _Lpsz_パラメーターは、65536 文字を超えない必要があります。 
    
## <a name="return-value"></a>戻り値

 **UlFromSzHex**では、符号なし長整数を返します。 文字列は、16 進数を少なくとも 1 つで開始されていない、0 が返されます。 
  
## <a name="remarks"></a>注釈

**UlFromSzHex**関数は、16 進数ではない文字列の最初の文字に達したときの変換を停止します。 **UlFromSzHex**は、"5 a"の文字列を指定するには、90 の整数値を返します。 文字列"5g5h"を指定するには、この関数は、整数値 5 を返します。 文字列"g5h5"を指定するには、 **UlFromSzHex**は 0 を返します。 
  
 **UlFromSzHex**アクセントの違いに左右されるがの ' a' から 'f' と '、' 'F' までの 16 進数にします。 Unicode と DBCS の形式で文字列がサポートされています。 _Lpsz_の長さの制限は、文字数、バイト数ではありませんが。 
  

