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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316913"
---
# <a name="acctbin"></a><span data-ttu-id="96058-103">ACCT_BIN</span><span class="sxs-lookup"><span data-stu-id="96058-103">ACCT_BIN</span></span>

<span data-ttu-id="96058-104">このデータ型の変数は、バイナリ値を保持します。</span><span class="sxs-lookup"><span data-stu-id="96058-104">A variable of this data type holds a binary value.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="96058-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="96058-105">Quick info</span></span>

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a><span data-ttu-id="96058-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="96058-106">Members</span></span>

<span data-ttu-id="96058-107">_cb_</span><span class="sxs-lookup"><span data-stu-id="96058-107">_cb_</span></span>
  
> <span data-ttu-id="96058-108">_pb_がポイントするバイト数。</span><span class="sxs-lookup"><span data-stu-id="96058-108">Number of bytes that  _pb_ points to.</span></span> 
    
<span data-ttu-id="96058-109">_pb_</span><span class="sxs-lookup"><span data-stu-id="96058-109">_pb_</span></span>
  
> <span data-ttu-id="96058-110">バイナリ情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="96058-110">Pointer to binary information.</span></span>
    

