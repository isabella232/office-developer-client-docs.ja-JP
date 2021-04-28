---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: このデータ型の変数はバイナリ値を保持します。
ms.openlocfilehash: 8299230a30b65ef8fb7856dc74618dd15ae218ac
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061336"
---
# <a name="acct_bin"></a>ACCT_BIN

このデータ型の変数はバイナリ値を保持します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    DWORD cb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a>メンバー

_cb_
  
> pb がポイントする  _バイト_ 数。 
    
_pb_
  
> バイナリ情報へのポインター。
    

