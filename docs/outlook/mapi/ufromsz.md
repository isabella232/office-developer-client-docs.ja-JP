---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 49f921ddd26fc78cea9b9b1e5ad99e248f4409ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609251"
---
# <a name="ufromsz"></a>UFromSz

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
10 進数の null 終端文字列を符号なし整数に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]変換する null 終端文字列へのポインター。 _lpsz パラメーター_ は、65536 文字を超えることはできません。 
    
## <a name="return-value"></a>戻り値

 **UFromSz は** 符号なし整数を返します。 文字列が 1 桁以上の 10 進数で始まる場合は、ゼロが返されます。 
  
## <a name="remarks"></a>注釈

**UFromSz** 関数は、10 進数ではない文字列の最初の文字に達すると、変換を停止します。 たとえば、文字列 "55" を指定すると **、UFromSz は** 整数値 55 を返します。 文字列 "5a5b" を指定すると、整数値 5 が返されます。 文字列 "a5b5" を指定すると **、UFromSz は** ゼロを返します。 
  
 **UFromSz は** 、区別の違いに敏感です。 Unicode および DBCS 形式の文字列がサポートされています。 _lpsz の長さの制限は_ 文字で、必ずしもバイトではありません。 
  

