---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: このデータ型の変数は、バリアント 型であるプロパティの値を保持します。
ms.openlocfilehash: 07b6280d7f2dd710375fe59a1811fdd3bb87b695
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621172"
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
    

