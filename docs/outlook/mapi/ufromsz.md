---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439010"
---
# <a name="ufromsz"></a>UFromSz

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
10進数値の null で終わる文字列を符号なし整数に変換します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> 順番変換する null で終わる文字列へのポインター。 _lpsz_パラメーターは、65536文字以下にする必要があります。 
    
## <a name="return-value"></a>戻り値

 **ufromsz**は、符号なし整数を返します。 文字列が少なくとも1つの10進数字で始まらない場合は、0が返されます。 
  
## <a name="remarks"></a>注釈

**ufromsz**関数は、10進数ではない文字列の最初の文字に達したときに変換を停止します。 たとえば、文字列 "55" が指定されている場合、 **ufromsz**は整数値55を返します。 文字列 "5a5b" が指定されている場合、関数は整数値5を返します。 文字列 "a5b5" が指定されている場合、 **ufromsz**は0を返します。 
  
 **ufromsz**は、分音の違いに敏感です。 Unicode および DBCS 形式の文字列がサポートされています。 _lpsz_の長さの制限は、文字である必要があり、必ずしもバイトではありません。 
  

