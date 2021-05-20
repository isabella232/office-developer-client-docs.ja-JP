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
# <a name="ftadcft"></a><span data-ttu-id="5b0f1-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="5b0f1-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="5b0f1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b0f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b0f1-105">必要に応じて、キャリー フラグを使用して、1 つの符号なし 64 ビット整数を別の整数に追加します。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5b0f1-106">実装元:</span><span class="sxs-lookup"><span data-stu-id="5b0f1-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="5b0f1-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="5b0f1-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="5b0f1-108">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="5b0f1-108">Called by:</span></span>  <br/> |<span data-ttu-id="5b0f1-109">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="5b0f1-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="5b0f1-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5b0f1-110">Parameters</span></span>

 <span data-ttu-id="5b0f1-111">_ft1_</span><span class="sxs-lookup"><span data-stu-id="5b0f1-111">_ft1_</span></span>
  
> <span data-ttu-id="5b0f1-112">[in]追加 [する最初](filetime.md) の符号なし 64 ビット整数を含む FILETIME 構造体。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="5b0f1-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="5b0f1-113">_ft2_</span></span>
  
> <span data-ttu-id="5b0f1-114">[in]追加する 2 番目の符号なし 64 ビット整数を含む FILETIME 構造体。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="5b0f1-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="5b0f1-115">_pwCarry_</span></span>
  
> <span data-ttu-id="5b0f1-116">[in, out, optional]入力時に、受信キャリー フラグへのポインター。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="5b0f1-117">出力時に、加算のキャリー結果へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="5b0f1-118">キャリー結果が不要な場合、このパラメーターは NULL に設定できます。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b0f1-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="5b0f1-119">Return value</span></span>

<span data-ttu-id="5b0f1-120">**FtAdcFt** 関数は、2 つの整数の合計を含む **FILETIME** 構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="5b0f1-121">2 つの入力パラメーターは変更されません。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="5b0f1-122">**pwCarry が** NULL 以外の場合、合計のキャリー結果 (0 または 1) が含まれる。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5b0f1-123">注釈</span><span class="sxs-lookup"><span data-stu-id="5b0f1-123">Remarks</span></span>

<span data-ttu-id="5b0f1-124">PwCarry が NULL の場合 **、FtAdcFt** 関数は **FtAddFt**  _と_ 同じです。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="5b0f1-125">_pwCarry が_ NULL ではなく、0 をポイントする場合 **、FtAdcFt** は **FtAddFt** が返すのと同じ **FILETIME** 値を返します。</span><span class="sxs-lookup"><span data-stu-id="5b0f1-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b0f1-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="5b0f1-126">See also</span></span>



[<span data-ttu-id="5b0f1-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="5b0f1-127">FtAddFt</span></span>](ftaddft.md)

