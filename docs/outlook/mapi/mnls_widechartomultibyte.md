---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: '最終更新日: 2012 年 2 月 21 日'
ms.openlocfilehash: f5cb63ca3d421073b00a448f762ecf0137494f2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801663"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**適用されます**: Outlook 
  
この関数は、 **WideCharToMultiByte**utf-16 (ワイド文字) の文字列を新しい文字列にマップするに似ています。 新しい文字の文字列とは限りませんマルチバイトの文字からは設定されません。
  
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

## <a name="parameters"></a>Parameters

 _uCodePage_
  
> [in]変換の実行に使用するコード ページです。
    
 _dwFlags_
  
> [in]変換の種類を示すフラグです。
    
 _lpWideCharStr_
  
> [in]変換する Unicode 文字列へのポインター。
    
 _cchWideChar_
  
> [in]変換の種類を示すフラグです。
    
 _lpMultiByteStr_
  
> [out]省略可能です。 変換後の文字列を受け取るバッファーへのポインター。
    
 _cchMultiByte_
  
> [in]_LpMultiByteStr_で示されるバッファーのバイト単位のサイズです。
    
 _lpDefaultChar_
  
> [in]省略可能です。 指定したコード ページで文字を表現できない場合に使用する文字へのポインター。
    
 _lpfUsedDefaultChar_
  
> [out]省略可能です。 関数が変換時に既定の文字を使用されるかどうかであることを示すフラグへのポインター。
    
## <a name="return-value"></a>�߂�l

正常終了した場合、 _lpMultiByteStr_が指すバッファーに書き込まれたバイト数を返します。 
  
## <a name="remarks"></a>備考

この関数は、 **WideCharToMultiByte**関数をラップします。 詳細については、 [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)を参照してください。
  
## <a name="see-also"></a>関連項目



[WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)

