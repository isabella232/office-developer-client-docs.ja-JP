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
ms.openlocfilehash: 3e23fa9fcb074fabacf1a2dd9ac3f632cdce5b5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576177"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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
  
> [in]ロケール識別子です。 詳細な定義は、[通常](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)の_ロケール_パラメーターを参照してください。
    
 _dwFlags_
  
> [in]大文字と小文字およびアクセント記号を無視するようにフラグを設定します。 詳細な定義は、 [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)の_dwCmpFlags_パラメーターを参照してください。
    
 _pstr1_
  
> [in]比較する最初の Unicode 文字列へのポインター。
    
 _cch1_
  
> [in]Unicode 文字列の先頭、末尾の null 文字を除いた文字数。 アプリケーションは、文字列が null で終わる場合、負の値を指定できます。 この例では、 **MNLS_CompareStringW**関数は、長さを自動的に決定します。 
    
 _pstr2_
  
> [in]比較する 2 番目の Unicode 文字列へのポインター。
    
 _cch2_
  
> [in]2 番目の Unicode 文字列は、終端の null 文字を除いた文字数。 アプリケーションは、文字列が null で終わる場合、負の値を指定できます。 この場合、関数は長さを自動的に決定します。
    
## <a name="return-value"></a>戻り値

[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)に記載されている値を返します。
  
## <a name="remarks"></a>注釈

この関数は、 [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)をラップします。 **MNLS_CompareStringW**では、同じパラメーターを取得し、 [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)と同じ動作をしました。
  
## <a name="see-also"></a>関連項目



[CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

