---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: '最終更新日: 2012 年 2 月 20 日'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356848"
---
# <a name="mnls_comparestringw"></a>MNLS_CompareStringW

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
2 つの Unicode 文字列を比較します。
  
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
  
> [in]ロケール識別子。 詳細な定義については  _、CompareString の Locale_ パラメーターを [参照してください](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)。
    
 _dwFlags_
  
> [in]大文字と小文字の区別を無視するフラグ。 詳細な定義については  _、CompareStringEx の dwCmpFlags_ パラメーター [を参照してください](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)。
    
 _pstr1_
  
> [in]比較する最初の Unicode 文字列へのポインター。
    
 _cch1_
  
> [in]終端の null 文字を除く、最初の Unicode 文字列の文字の長さ。 文字列が null 終端の場合、アプリケーションは負の値を指定できます。 この場合、この関数 **はMNLS_CompareStringW** 長さを自動的に決定します。 
    
 _pstr2_
  
> [in]比較する 2 番目の Unicode 文字列へのポインター。
    
 _cch2_
  
> [in]2 番目の Unicode 文字列の文字の長さ (終端の null 文字を除く)。 文字列が null 終端の場合、アプリケーションは負の値を指定できます。 この場合、関数は自動的に長さを決定します。
    
## <a name="return-value"></a>戻り値

CompareStringEx で説明されている [値を返します](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)。
  
## <a name="remarks"></a>注釈

この関数は [CompareStringW をラップします](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)。 **MNLS_CompareStringW** 同じパラメーターを受け取り [、CompareStringW と同じ動作をします](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)。
  
## <a name="see-also"></a>関連項目



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

