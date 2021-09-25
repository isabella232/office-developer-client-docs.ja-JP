---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: このデータ型の変数はバイナリ値を保持します。
ms.openlocfilehash: 315336db9a62c3ae7e56feb871bcd0b2f7971d48
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596651"
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
    

