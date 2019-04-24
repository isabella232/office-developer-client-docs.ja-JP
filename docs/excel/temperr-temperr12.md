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
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310347"
---
# <a name="temperrtemperr12"></a><span data-ttu-id="a280c-104">TempErr/TempErr12</span><span class="sxs-lookup"><span data-stu-id="a280c-104">TempErr/TempErr12</span></span>

 <span data-ttu-id="a280c-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a280c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a280c-106">Microsoft Excel ワークシートのエラーを含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="a280c-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing a Microsoft Excel worksheet error.</span></span> 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a><span data-ttu-id="a280c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a280c-107">Parameters</span></span>

 <span data-ttu-id="a280c-108">_err_</span><span class="sxs-lookup"><span data-stu-id="a280c-108">_err_</span></span>
  
<span data-ttu-id="a280c-109">目的のエラー コードまたはリテラル数値と同等の数値を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="a280c-109">The desired error code, or its literal numeric equivalent, as shown in the following table.</span></span>
  
|<span data-ttu-id="a280c-110">**エラー**</span><span class="sxs-lookup"><span data-stu-id="a280c-110">**Error**</span></span>|<span data-ttu-id="a280c-111">**XLCALL.H で定義されたエラー コード**</span><span class="sxs-lookup"><span data-stu-id="a280c-111">**Error code defined in XLCALL.H**</span></span>|<span data-ttu-id="a280c-112">**同等の 10 進数**</span><span class="sxs-lookup"><span data-stu-id="a280c-112">**Decimal equivalent**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a280c-113">#NULL</span><span class="sxs-lookup"><span data-stu-id="a280c-113">#NULL</span></span>  <br/> |<span data-ttu-id="a280c-114">**xlerrNull**</span><span class="sxs-lookup"><span data-stu-id="a280c-114">**xlerrNull**</span></span> <br/> |<span data-ttu-id="a280c-115">.0</span><span class="sxs-lookup"><span data-stu-id="a280c-115">0</span></span>  <br/> |
|<span data-ttu-id="a280c-116">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="a280c-116">#DIV/0!</span></span>  <br/> |<span data-ttu-id="a280c-117">**xlerrDiv0**</span><span class="sxs-lookup"><span data-stu-id="a280c-117">**xlerrDiv0**</span></span> <br/> |<span data-ttu-id="a280c-118">7</span><span class="sxs-lookup"><span data-stu-id="a280c-118">7</span></span>  <br/> |
|<span data-ttu-id="a280c-119">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="a280c-119">#VALUE!</span></span>  <br/> |<span data-ttu-id="a280c-120">**xlerrValue**</span><span class="sxs-lookup"><span data-stu-id="a280c-120">**xlerrValue**</span></span> <br/> |<span data-ttu-id="a280c-121">約</span><span class="sxs-lookup"><span data-stu-id="a280c-121">15</span></span>  <br/> |
|<span data-ttu-id="a280c-122">#REF!</span><span class="sxs-lookup"><span data-stu-id="a280c-122">#REF!</span></span>  <br/> |<span data-ttu-id="a280c-123">**xlerrRef**</span><span class="sxs-lookup"><span data-stu-id="a280c-123">**xlerrRef**</span></span> <br/> |<span data-ttu-id="a280c-124">最高</span><span class="sxs-lookup"><span data-stu-id="a280c-124">23</span></span>  <br/> |
|<span data-ttu-id="a280c-125">#NAME?</span><span class="sxs-lookup"><span data-stu-id="a280c-125">#NAME?</span></span>  <br/> |<span data-ttu-id="a280c-126">**xlerrName**</span><span class="sxs-lookup"><span data-stu-id="a280c-126">**xlerrName**</span></span> <br/> |<span data-ttu-id="a280c-127">29</span><span class="sxs-lookup"><span data-stu-id="a280c-127">29</span></span>  <br/> |
|<span data-ttu-id="a280c-128">#NUM!</span><span class="sxs-lookup"><span data-stu-id="a280c-128">#NUM!</span></span>  <br/> |<span data-ttu-id="a280c-129">**xlerrNum**</span><span class="sxs-lookup"><span data-stu-id="a280c-129">**xlerrNum**</span></span> <br/> |<span data-ttu-id="a280c-130">36</span><span class="sxs-lookup"><span data-stu-id="a280c-130">36</span></span>  <br/> |
|<span data-ttu-id="a280c-131">#N/A</span><span class="sxs-lookup"><span data-stu-id="a280c-131">#N/A</span></span>  <br/> |<span data-ttu-id="a280c-132">**xlerrNA**</span><span class="sxs-lookup"><span data-stu-id="a280c-132">**xlerrNA**</span></span> <br/> |<span data-ttu-id="a280c-133">42</span><span class="sxs-lookup"><span data-stu-id="a280c-133">42</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="a280c-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="a280c-134">Return value</span></span>

<span data-ttu-id="a280c-135">渡されたエラー コードを含む **xltypeBool** を返します。</span><span class="sxs-lookup"><span data-stu-id="a280c-135">Returns an **xltypeBool** containing the error code passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a280c-136">例</span><span class="sxs-lookup"><span data-stu-id="a280c-136">Example</span></span>

<span data-ttu-id="a280c-p101">この例では、**TempErr12** 関数を使用して #VALUE! エラーを Excel に返します。</span><span class="sxs-lookup"><span data-stu-id="a280c-p101">This example uses the **TempErr12** function to return a #VALUE! error to Excel.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a280c-p102">フレームワーク ライブラリ関数 **TempErr12** は、内部バッファーからメモリを割り当てます。割り当てられたメモリは通常、フレームワーク関数 **Excel12f** が呼び出されると解放されます。**Excel12f** を呼び出さずに、この例の関数を繰り返し呼び出すと、メモリ リークが発生します。</span><span class="sxs-lookup"><span data-stu-id="a280c-p102">The Framework library function **TempErr12** allocates memory from an internal buffer, which is normally freed when the Framework function **Excel12f** is called. If this example function is called repeatedly without **Excel12f** being called, a memory leak occurs.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a><span data-ttu-id="a280c-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="a280c-141">See also</span></span>



[<span data-ttu-id="a280c-142">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="a280c-142">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

