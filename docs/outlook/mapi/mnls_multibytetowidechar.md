---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: '最終更新日: 2012 年2月21日'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338242"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**MultiByteToWideChar**に似ています。これは、文字列を utf-16 (ワイド文字) 文字列にマッピングします。 文字文字列は、マルチバイト文字セットからのものであるとは限りません。
  
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

 _ucodepage_
  
> 順番変換を実行するために使用するコードページ。
    
 _dwFlags_
  
> 順番変換の種類を示すフラグです。
    
 _lpmultibytestr_
  
> 順番変換する文字列へのポインター。
    
 _cchmultibyte バイト_
  
> 順番_lpmultibytestr_パラメーターで指定された文字列のサイズ (バイト単位)。 
    
 _lpWideCharStr_
  
> [out]省略可能です。 変換された文字列を受け取るバッファーへのポインター。
    
 _cchWideChar_
  
> 順番_lpWideCharStr_によって示されるバッファーのサイズ (文字数)。
    
## <a name="return-value"></a>戻り値

成功した場合、 _lpWideCharStr_によって示されるバッファーに書き込まれた文字数を返します。 
  
## <a name="remarks"></a>解説

この関数は、 **MultiByteToWideChar**関数をラップします。 詳細については、「 [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx)」を参照してください。
  

