---
title: FtSubFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtSubFt
api_type:
- COM
ms.assetid: 6619fc41-5518-44ce-85c1-6b0077ed5cb9
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 954630b0b92772d961dc61084c28a9ab419e4c2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800146"
---
# <a name="ftsubft"></a><span data-ttu-id="83025-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="83025-103">FtSubFt</span></span>

  
  
<span data-ttu-id="83025-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="83025-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="83025-105">別の 1 つの符号なし 64 ビット整数を減算します。</span><span class="sxs-lookup"><span data-stu-id="83025-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="83025-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="83025-106">Header file:</span></span>  <br/> |<span data-ttu-id="83025-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="83025-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="83025-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="83025-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="83025-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="83025-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="83025-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="83025-110">Called by:</span></span>  <br/> |<span data-ttu-id="83025-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="83025-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="83025-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="83025-112">Parameters</span></span>

 <span data-ttu-id="83025-113">_被減数_</span><span class="sxs-lookup"><span data-stu-id="83025-113">_Minuend_</span></span>
  
> <span data-ttu-id="83025-114">[in]減算される元となる_減数_パラメーターの値は、64 ビットの符号なし整数を格納する[FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="83025-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="83025-115">_減数_</span><span class="sxs-lookup"><span data-stu-id="83025-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="83025-116">[in]_被減数_パラメーターで指定された値から減算する符号なし 64 ビット整数を格納する**FILETIME**構造体。</span><span class="sxs-lookup"><span data-stu-id="83025-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="83025-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="83025-117">Return value</span></span>

<span data-ttu-id="83025-118">**FtSubFt**関数では、減算の結果を格納する**FILETIME**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="83025-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="83025-119">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="83025-119">The two input parameters remain unchanged.</span></span> 
  

