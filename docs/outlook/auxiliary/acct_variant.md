---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: このデータ型の変数は、バリアント型 (variant) のデータ型のプロパティの値を保持します。
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316920"
---
# <a name="acctvariant"></a>ACCT_VARIANT

このデータ型の変数は、バリアント型 (variant) のデータ型のプロパティの値を保持します。
  
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
  
> variant の DWORD 値。
    
_pwsz_
  
> variant の文字列値。
    
_在庫_
  
> バリアント型 (variant) のバイナリ値を指定します。
    

