---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: '最終更新日: 2012 年2月20日'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356848"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2つの Unicode 文字列を比較します。
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a>パラメーター

 _lcid_
  
> 順番ロケール識別子。 詳細な定義については、 [comparestring](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)の_Locale_パラメーターを参照してください。
    
 _dwFlags_
  
> 順番大文字/小文字の区別を無視するフラグ。 詳細な定義については、 _dwCmpFlags_パラメータ of [comparestringex](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)を参照してください。
    
 _pstr1_
  
> 順番比較する最初の Unicode 文字列へのポインター。
    
 _cch1_
  
> 順番最初の Unicode 文字列の文字数 (終端の null 文字は除く)。 文字列が null で終端されている場合、アプリケーションは負の値を指定できます。 この場合、 **MNLS_CompareStringW**関数は長さを自動的に決定します。 
    
 _pstr2_
  
> 順番比較する2番目の Unicode 文字列へのポインター。
    
 _cch2_
  
> 順番2番目の Unicode 文字列の文字数 (終端の null 文字は除く)。 文字列が null で終端されている場合、アプリケーションは負の値を指定できます。 この場合、関数は長さを自動的に決定します。
    
## <a name="return-value"></a>戻り値

[comparestringex](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)で記述されている値を返します。
  
## <a name="remarks"></a>解説

この関数は、 [comparestringw](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)をラップします。 **MNLS_CompareStringW**は同じパラメーターを受け取り、 [comparestringw](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)と同じ動作をします。
  
## <a name="see-also"></a>関連項目



[comparestringw](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[comparestringex](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

