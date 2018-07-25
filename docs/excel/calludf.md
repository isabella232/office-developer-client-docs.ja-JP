---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798761"
---
# <a name="calludf"></a>CallUDF

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
高パフォーマンスのコンピューティング環境でユーザー定義関数を呼び出します。
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>パラメーター

_SessionId_
  
> 呼び出しを行うセッションの ID。
    
_XLLName_
  
> ユーザー定義関数が含まれる XLL の名前。
    
_UDFName_
  
> ユーザー定義関数の名前。
    
_CallBackAddr_
  
> ユーザー定義関数が終了するときにコネクタが呼び出す必要がある関数。
    
_pxAsyncHandle_
  
> Excel とコネクタが、保留中のユーザー定義関数の呼び出しを追跡するために使用する非同期ハンドル。コネクタはこれを使用して、呼び出しが完了した時点で、_CallBackAddr_ 引数で渡された関数ポインターを使用して Excel へのコールバックを行います。 
    
_ArgCount_
  
> ユーザー定義関数に渡される引数の数。最大値は 255 です。
    
_Parameter1_
  
> ユーザー定義関数に渡す値。_ArgCount_ で指定されたパラメーターごとに、この引数を繰り返します。
    
## <a name="return-value"></a>戻り値

UDF 呼び出しが正常に開始された場合は **xlHpcRetSuccess** が返されます。_SessionId_ 引数が無効な場合は **xlHpcRetInvalidSessionId**、タイムアウトなどのその他のエラーが発生した場合は **xlHpcRetCallFailed** が返されます。呼び出しがエラー コード (**xlHpcRetSuccess** 以外のすべてのコード) を返すと、Excel は UDF 呼び出しが失敗したとみなし、_pxAsyncHandle_ を無効化します。この場合、Excel はコールバックが行われることを期待しません。
  
## <a name="remarks"></a>注釈

この関数は非同期で実行されます。
  
## <a name="see-also"></a>関連項目

- [Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)

