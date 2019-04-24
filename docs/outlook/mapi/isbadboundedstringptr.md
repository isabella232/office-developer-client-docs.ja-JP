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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278835"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
呼び出し元プロセスが、指定されたメモリ範囲に対する読み取りアクセス権を持っているかどうかを確認します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapiwin  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー。  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>パラメーター

 _lpsz_
  
> 順番null で終了する ASCII 文字列へのポインター。
    
 _cchmax_
  
> 順番文字列の最大サイズを文字数で指定します。 この関数は、文字列の終端の null 文字まで、またはこのパラメーターで指定された文字数までのすべての文字に対する読み取りアクセス権をチェックします。 このパラメーターが0の場合、戻り値は0になります。
    
## <a name="return-value"></a>戻り値

呼び出し元のプロセスが文字列の終端の null 文字までのすべての文字に対する読み取りアクセス権を持っている場合、戻り値は0です。または、 _cchmax_で指定された文字数まで読み出します。
  
戻り値は、呼び出し元のプロセスが文字列の終端の null 文字までのすべての文字に対する読み取りアクセス権を持たない場合、または_cchmax_で指定された文字数までの読み取りアクセス権を持っていない場合は0以外の値です。
  
## <a name="remarks"></a>解説

**IsBadBoundedStringPtr**関数は、 **IsBadStringPtr**を使用するのと同じです。
  
## <a name="see-also"></a>関連項目



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

