---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: '最終更新日: 2012 年 2 月 21 日'
ms.openlocfilehash: ab082c8ac70bf851097080fb41033f76bccc3044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801653"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**適用対象**: Outlook 
  
**MultiByteToWideChar**文字の文字列を utf-16 (ワイド文字) の文字列にマップするに似ています。 文字の文字列とは限りませんマルチバイトの文字からは設定されません。
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a>パラメーター

 _uCodePage_
  
> [in]変換の実行に使用するコード ページです。
    
 _dwFlags_
  
> [in]変換の種類を示すフラグです。
    
 _lpMultiByteStr_
  
> [in]変換する文字の文字列へのポインター。
    
 _cchMultiByte_
  
> [in]_LpMultiByteStr_パラメーターで指定された文字列のバイト単位のサイズです。 
    
 _lpWideCharStr_
  
> [out]省略可能です。 変換後の文字列を受け取るバッファーへのポインター。
    
 _cchWideChar_
  
> [in]_LpWideCharStr_で示されるバッファーの文字のサイズです。
    
## <a name="return-value"></a>戻り値

正常終了した場合は、 _lpWideCharStr_で示されるバッファーに書き込まれた文字数を返します。 
  
## <a name="remarks"></a>注釈

この関数は、 **MultiByteToWideChar**の関数をラップします。 詳細については、 [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx)を参照してください。
  

