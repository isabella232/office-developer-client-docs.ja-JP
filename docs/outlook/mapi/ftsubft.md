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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: edd789a586adc71289ff821aa7cf7a33f79fb738
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408419"
---
# <a name="ftsubft"></a><span data-ttu-id="ce9ee-103">FtSubFt</span><span class="sxs-lookup"><span data-stu-id="ce9ee-103">FtSubFt</span></span>

  
  
<span data-ttu-id="ce9ee-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce9ee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce9ee-105">1 つの符号なし 64 ビット整数を別の整数から減算します。</span><span class="sxs-lookup"><span data-stu-id="ce9ee-105">Subtracts one unsigned 64-bit integer from another.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce9ee-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ce9ee-106">Header file:</span></span>  <br/> |<span data-ttu-id="ce9ee-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ce9ee-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ce9ee-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ce9ee-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ce9ee-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ce9ee-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ce9ee-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ce9ee-110">Called by:</span></span>  <br/> |<span data-ttu-id="ce9ee-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ce9ee-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtSubFt(
  FILETIME Minuend,
  FILETIME Subtrahend
);
```

## <a name="parameters"></a><span data-ttu-id="ce9ee-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ce9ee-112">Parameters</span></span>

 <span data-ttu-id="ce9ee-113">_Minuend_</span><span class="sxs-lookup"><span data-stu-id="ce9ee-113">_Minuend_</span></span>
  
> <span data-ttu-id="ce9ee-114">[in]_Subtrahend_ パラメーターの値を減算する符号なし 64 ビット整数を含む [FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="ce9ee-114">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer from which the value in the  _Subtrahend_ parameter is to be subtracted.</span></span> 
    
 <span data-ttu-id="ce9ee-115">_Subtrahend_</span><span class="sxs-lookup"><span data-stu-id="ce9ee-115">_Subtrahend_</span></span>
  
> <span data-ttu-id="ce9ee-116">[in]_Minuend_ パラメーターで示される値から減算された符号なし 64 ビット整数を含む **FILETIME** 構造体。</span><span class="sxs-lookup"><span data-stu-id="ce9ee-116">[in] A **FILETIME** structure that contains the unsigned 64-bit integer that is subtracted from the value indicated by the  _Minuend_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ce9ee-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="ce9ee-117">Return value</span></span>

<span data-ttu-id="ce9ee-118">**FtSubFt** 関数は、減算の結果を含む **FILETIME** 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="ce9ee-118">The **FtSubFt** function returns a **FILETIME** structure that contains the result of the subtraction.</span></span> <span data-ttu-id="ce9ee-119">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="ce9ee-119">The two input parameters remain unchanged.</span></span> 
  

