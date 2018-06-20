---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: このデータ型の変数は、バリアント データ型のプロパティの値を保持します。
ms.openlocfilehash: c85af4bd4fefffb4fadf671bb7cf5b7f072d5e95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799303"
---
# <a name="acctvariant"></a>ACCT_VARIANT

このデータ型の変数は、バリアント データ型のプロパティの値を保持します。
  
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
  
> バリアントの種類です。
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_dw_
  
> バリアントの DWORD 値です。
    
_pwsz_
  
> バリアント型の値の文字列を指定します。
    
_箱_
  
> バリアントのバイナリ値です。
    

