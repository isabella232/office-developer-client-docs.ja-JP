---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: '最終更新日: 2012 年 2 月 21 日'
ms.openlocfilehash: 13824c686c92901db5fa7849247b3be176aba961
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571395"
---
# <a name="mnls_widechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この関数は、UTF-16 (ワイド文字) 文字列を新しい文字列にマップする **WideCharToMultiByte** に似ています。 新しい文字列は、必ずしもマルチバイト文字セットとは限りません。
  
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

 _uCodePage_
  
> [in]変換の実行に使用するコード ページ。
    
 _dwFlags_
  
> [in]変換の種類を示すフラグ。
    
 _lpWideCharStr_
  
> [in]変換する Unicode 文字列へのポインター。
    
 _cchWideChar_
  
> [in]変換の種類を示すフラグ。
    
 _lpMultiByteStr_
  
> [out]省略可能です。 変換された文字列を受け取るバッファーへのポインター。
    
 _cchMultiByte_
  
> [in]  _lpMultiByteStr_ で示されるバッファーのサイズ (バイト単位)。
    
 _lpDefaultChar_
  
> [in]省略可能です。 指定したコード ページで文字を表現できない場合に使用する文字へのポインター。
    
 _lpfUsedDefaultChar_
  
> [out]省略可能です。 関数が変換で既定の文字を使用したかどうかを示すフラグへのポインター。
    
## <a name="return-value"></a>戻り値

成功した場合  _、lpMultiByteStr_ が指すバッファーに書き込まれたバイト数を返します。 
  
## <a name="remarks"></a>注釈

この関数は **、WideCharToMultiByte 関数をラップ** します。 詳細については [、「WideCharToMultiByte」を参照してください](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)。
  
## <a name="see-also"></a>関連項目



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

