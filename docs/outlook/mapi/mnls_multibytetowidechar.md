---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: '最終更新日: 2012 年 2 月 21 日'
ms.openlocfilehash: a5f0d0d3e209ec1bb1b87b822badcb581a540a35
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583969"
---
# <a name="mnls_multibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**MultiByteToWideChar** と同様に、文字列を UTF-16 (ワイド文字) 文字列にマップします。 文字列は、必ずしもマルチバイト文字セットとは限りません。
  
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
  
> [in]変換の実行に使用するコード ページ。
    
 _dwFlags_
  
> [in]変換の種類を示すフラグ。
    
 _lpMultiByteStr_
  
> [in]変換する文字列へのポインター。
    
 _cchMultiByte_
  
> [in]  _lpMultiByteStr_ パラメーターで示される文字列のサイズ (バイト単位)。 
    
 _lpWideCharStr_
  
> [out]省略可能です。 変換された文字列を受け取るバッファーへのポインター。
    
 _cchWideChar_
  
> [in]  _lpWideCharStr_ で示されるバッファーのサイズ (文字)。
    
## <a name="return-value"></a>戻り値

成功した場合  _、lpWideCharStr_ で示されるバッファーに書き込まれた文字数を返します。 
  
## <a name="remarks"></a>注釈

この関数は **、MultiByteToWideChar 関数をラップ** します。 詳細については [、「MultiByteToWideChar」を参照してください](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx)。
  

