---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: このデータ型の変数は、バリアント 型であるプロパティの値を保持します。
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424400"
---
# <a name="acct_variant"></a>ACCT_VARIANT

このデータ型の変数は、バリアント 型であるプロパティの値を保持します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a>メンバー

_dwType_
  
> バリアントの種類:
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_dw_
  
> バリアントの DWORD 値。
    
_pwsz_
  
> variant の文字列値。
    
_bin_
  
> バリアントのバイナリ値。
    

