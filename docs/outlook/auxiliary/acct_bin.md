---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: このデータ型の変数は、バイナリ値を保持します。
ms.openlocfilehash: 3dcaaf73a04ddc608e68ca7bd1f801d0a5d99bb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408125"
---
# <a name="acctbin"></a>ACCT_BIN

このデータ型の変数は、バイナリ値を保持します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a>メンバー

_cb_
  
> _pb_がポイントするバイト数。 
    
_pb_
  
> バイナリ情報へのポインター。
    

