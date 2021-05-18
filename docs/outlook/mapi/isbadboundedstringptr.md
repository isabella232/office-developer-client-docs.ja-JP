---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278835"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し元のプロセスが、指定されたメモリ範囲への読み取りアクセス権を持っているのを確認します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiwin.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー。  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]NULL 終端 ASCII 文字列へのポインター。
    
 _cchMax_
  
> [in]文字列の最大サイズ (CHARs)。 この関数は、文字列の終端の null 文字までのすべての文字、またはこのパラメーターで指定された文字数までの読み取りアクセスをチェックします。これより小さい方を指定します。 このパラメーターが 0 の場合、戻り値は 0 です。
    
## <a name="return-value"></a>戻り値

呼び出し元のプロセスが文字列の終端の null 文字までのすべての文字に対する読み取りアクセス権を持つ場合、または  _cchMax_ で指定された文字数までの読み取りアクセス権を持つ場合、戻り値は 0 です。
  
呼び出し元のプロセスが文字列の終端の null 文字までのすべての文字への読み取りアクセス権を持たない場合、または  _cchMax_ で指定された文字数までの読み取りアクセス権がない場合、戻り値は 0 以外です。
  
## <a name="remarks"></a>注釈

**IsBadBoundedStringPtr** 関数は **IsBadStringPtr の使用と同等です**。
  
## <a name="see-also"></a>関連項目



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

