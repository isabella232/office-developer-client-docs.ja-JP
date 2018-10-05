---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388904"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し元のプロセスがメモリの指定された範囲に読み取りアクセス権を持っていることを確認します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiwin.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス ・ プロバイダーです。  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> [in]Null で終わる ASCII 文字列へのポインター。
    
 _cchMax_
  
> [in]文字数、文字列の最大サイズです。 関数は、文字列の終端の null 文字までのすべての文字の読み取りアクセス権のチェック、またはこのパラメーターで指定された文字の数は、どちらかが小さい。 このパラメーターが 0 の場合は 0 を返します。
    
## <a name="return-value"></a>戻り値

呼び出し元のプロセスが、文字列の終端の null 文字までのすべての文字への読み取りアクセスまたは_cchMax_で指定された文字数までの読み取りアクセス権を持つ場合は、0 を返します。
  
呼び出し元のプロセスが、文字列の終端の null 文字までのすべての文字への読み取りアクセスまたは_cchMax_で指定された文字数までの読み取りアクセス権があるないときは、0 以外を返します。
  
## <a name="remarks"></a>備考

**IsBadBoundedStringPtr**関数は、 **IsBadStringPtr**を使用すると同じです。
  
## <a name="see-also"></a>関連項目



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

