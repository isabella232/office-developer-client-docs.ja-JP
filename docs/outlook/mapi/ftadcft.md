---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429706"
---
# <a name="ftadcft"></a><span data-ttu-id="c46c4-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="c46c4-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="c46c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c46c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c46c4-105">符号なしの64ビット整数をもう1つ別に追加します。オプションで、キャリーフラグを使用します。</span><span class="sxs-lookup"><span data-stu-id="c46c4-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c46c4-106">実装元:</span><span class="sxs-lookup"><span data-stu-id="c46c4-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="c46c4-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="c46c4-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="c46c4-108">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c46c4-108">Called by:</span></span>  <br/> |<span data-ttu-id="c46c4-109">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="c46c4-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="c46c4-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c46c4-110">Parameters</span></span>

 <span data-ttu-id="c46c4-111">_ft1_</span><span class="sxs-lookup"><span data-stu-id="c46c4-111">_ft1_</span></span>
  
> <span data-ttu-id="c46c4-112">順番追加する最初の未署名の64ビット整数を含む[FILETIME](filetime.md)構造体。</span><span class="sxs-lookup"><span data-stu-id="c46c4-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="c46c4-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="c46c4-113">_ft2_</span></span>
  
> <span data-ttu-id="c46c4-114">順番追加する2番目の符号なし64ビット整数を含む FILETIME 構造。</span><span class="sxs-lookup"><span data-stu-id="c46c4-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="c46c4-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="c46c4-115">_pwCarry_</span></span>
  
> <span data-ttu-id="c46c4-116">[入力、出力、オプション]入力時に、着信キャリーフラグへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c46c4-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="c46c4-117">出力時に、追加のキャリー結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c46c4-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="c46c4-118">キャリー result が必要ない場合は、このパラメーターを NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c46c4-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c46c4-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="c46c4-119">Return value</span></span>

<span data-ttu-id="c46c4-120">**ftadcft**関数は、2つの整数の合計を含む**FILETIME**構造を返します。</span><span class="sxs-lookup"><span data-stu-id="c46c4-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="c46c4-121">2つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="c46c4-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="c46c4-122">**pwCarry**が NULL 以外の場合は、sum のキャリー結果 (0 または 1) を含みます。</span><span class="sxs-lookup"><span data-stu-id="c46c4-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c46c4-123">注釈</span><span class="sxs-lookup"><span data-stu-id="c46c4-123">Remarks</span></span>

<span data-ttu-id="c46c4-124">**ftadcft**関数は、 _pwCarry_が NULL の場合、 **ftaddft**と同じです。</span><span class="sxs-lookup"><span data-stu-id="c46c4-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="c46c4-125">_pwCarry_が NULL ではなく0をポイントしている場合、 **ftadcft**は**ftaddft**が返すのと同じ**FILETIME**値を返します。</span><span class="sxs-lookup"><span data-stu-id="c46c4-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c46c4-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="c46c4-126">See also</span></span>



[<span data-ttu-id="c46c4-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="c46c4-127">FtAddFt</span></span>](ftaddft.md)

