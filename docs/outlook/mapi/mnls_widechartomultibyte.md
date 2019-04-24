---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: '最終更新日: 2012 年2月21日'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338732"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この関数は**WideCharToMultiByte**に似ています。これは、utf-16 (ワイド文字) 文字列を新しい文字列にマッピングします。 新しい文字列は、マルチバイト文字セットからのものであるとは限りません。
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a>パラメーター

 _ucodepage_
  
> 順番変換を実行するために使用するコードページ。
    
 _dwFlags_
  
> 順番変換の種類を示すフラグです。
    
 _lpWideCharStr_
  
> 順番変換する Unicode 文字列へのポインター。
    
 _cchWideChar_
  
> 順番変換の種類を示すフラグです。
    
 _lpmultibytestr_
  
> [out]省略可能です。 変換された文字列を受け取るバッファーへのポインター。
    
 _cchmultibyte バイト_
  
> 順番_lpmultibytestr_によって示されるバッファーのサイズ (バイト単位)。
    
 _lpdefaultchar_
  
> [in]省略可能です。 指定されたコードページで文字を表現できない場合に使用する文字へのポインター。
    
 _lpfUsedDefaultChar_
  
> [out]省略可能です。 関数が変換時に既定の文字を使用したかどうかを示すフラグへのポインター。
    
## <a name="return-value"></a>戻り値

成功した場合は、 _lpmultibytestr_が指すバッファーに書き込まれたバイト数を返します。 
  
## <a name="remarks"></a>解説

この関数は、 **WideCharToMultiByte**関数をラップします。 詳細については、「 [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)」を参照してください。
  
## <a name="see-also"></a>関連項目



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

