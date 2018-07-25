---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- temperr function [excel 2007],TempErr12 function [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798943"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="5c0b8-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="5c0b8-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="5c0b8-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5c0b8-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5c0b8-106">Microsoft Excel ワークシートのエラーを含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="5c0b8-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="5c0b8-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5c0b8-107">Parameters</span></span>

 <span data-ttu-id="5c0b8-108">_err_</span><span class="sxs-lookup"><span data-stu-id="5c0b8-108">_err_</span></span>
  
<span data-ttu-id="5c0b8-109">目的のエラー コードまたはリテラル数値と同等の数値を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="5c0b8-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="5c0b8-110">**エラー**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-110">**Error**</span></span>|<span data-ttu-id="5c0b8-111">**XLCALL.H で定義されたエラー コード**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="5c0b8-112">**同等の 10 進数**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5c0b8-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="5c0b8-113">#NULL</span></span>  <br/> |<span data-ttu-id="5c0b8-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-114">**xlErrNull**</span></span> <br/> |<span data-ttu-id="5c0b8-115">0</span><span class="sxs-lookup"><span data-stu-id="5c0b8-115">{0}</span></span>  <br/> |
|<span data-ttu-id="5c0b8-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="5c0b8-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="5c0b8-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-117">**xlErrDiv0**</span></span> <br/> |<span data-ttu-id="5c0b8-118">7</span><span class="sxs-lookup"><span data-stu-id="5c0b8-118">-7</span></span>  <br/> |
|<span data-ttu-id="5c0b8-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="5c0b8-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="5c0b8-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-120">**xlErrValue**</span></span> <br/> |<span data-ttu-id="5c0b8-121">15</span><span class="sxs-lookup"><span data-stu-id="5c0b8-121">-15</span></span>  <br/> |
|<span data-ttu-id="5c0b8-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="5c0b8-122">#REF!</span></span>  <br/> |<span data-ttu-id="5c0b8-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-123">**xlErrRef**</span></span> <br/> |<span data-ttu-id="5c0b8-124">23</span><span class="sxs-lookup"><span data-stu-id="5c0b8-124">2.3</span></span>  <br/> |
|<span data-ttu-id="5c0b8-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="5c0b8-125">#NAME?</span></span>  <br/> |<span data-ttu-id="5c0b8-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-126">**xlErrName**</span></span> <br/> |<span data-ttu-id="5c0b8-127">29</span><span class="sxs-lookup"><span data-stu-id="5c0b8-127">-29</span></span>  <br/> |
|<span data-ttu-id="5c0b8-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="5c0b8-128">#NUM!</span></span>  <br/> |<span data-ttu-id="5c0b8-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-129">**xlErrNum**</span></span> <br/> |<span data-ttu-id="5c0b8-130">36</span><span class="sxs-lookup"><span data-stu-id="5c0b8-130">-36</span></span>  <br/> |
|<span data-ttu-id="5c0b8-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="5c0b8-131">#N/A</span></span>  <br/> |<span data-ttu-id="5c0b8-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="5c0b8-132">**xlErrNA**</span></span> <br/> |<span data-ttu-id="5c0b8-133">42</span><span class="sxs-lookup"><span data-stu-id="5c0b8-133">4.2</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="5c0b8-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="5c0b8-134">Return value</span></span>

<span data-ttu-id="5c0b8-135">渡されたエラー コードを含む **xltypeBool** を返します。</span><span class="sxs-lookup"><span data-stu-id="5c0b8-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5c0b8-136">例</span><span class="sxs-lookup"><span data-stu-id="5c0b8-136">Example</span></span>

<span data-ttu-id="5c0b8-p101">この例では、**TempErr12** 関数を使用して #VALUE! エラーを Excel に返します。</span><span class="sxs-lookup"><span data-stu-id="5c0b8-p101">This example uses the **TempErr12** function to return a #VALUE! error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5c0b8-p102">フレームワーク ライブラリ関数 **TempErr12** は、内部バッファーからメモリを割り当てます。割り当てられたメモリは通常、フレームワーク関数 **Excel12f** が呼び出されると解放されます。**Excel12f** を呼び出さずに、この例の関数を繰り返し呼び出すと、メモリ リークが発生します。</span><span class="sxs-lookup"><span data-stu-id="5c0b8-p102">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called. If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="5c0b8-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c0b8-141">See also</span></span>



[<span data-ttu-id="5c0b8-142">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="5c0b8-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

