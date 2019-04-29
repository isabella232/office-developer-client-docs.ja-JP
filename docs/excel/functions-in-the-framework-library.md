---
title: �t���[�����[�N ���C�u�����̊֐�
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- framework library functions [excel 2007],functions [Excel 2007], Framework library
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417547"
---
# <a name="functions-in-the-framework-library"></a><span data-ttu-id="5242e-104">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="5242e-104">Functions in the Framework Library</span></span>

<span data-ttu-id="5242e-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5242e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5242e-106">フレームワーク ライブラリは、XLL を簡単に記述できるようにするために作成されました。</span><span class="sxs-lookup"><span data-stu-id="5242e-106">The Framework Library was created to help make writing XLLs easier.</span></span> <span data-ttu-id="5242e-107">これには、**XLOPER**/ **XLOPER12** メモリの管理、一時 **XLOPER**/ **XLOPER12** の作成、Microsoft Excel のコールバック関数の確実な呼び出し (**Excel4**、**Excel4v**、\*\* Excel12 **、** Excel12v \*\*)、接続されている端末上のデバッグ文字列の印刷のための単純な関数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5242e-107">It includes simple functions for managing **XLOPER**/ **XLOPER12** memory, creating temporary **XLOPER**/ **XLOPER12**, robustly calling the Microsoft Excel callback functions (**Excel4**, **Excel4v**, \*\* Excel12 \*\*, \*\* Excel12v \*\*) and printing debugging strings on an attached terminal.</span></span>
  
<span data-ttu-id="5242e-108">このライブラリに含まれている関数は、次のようなコードの一部を簡略化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5242e-108">The functions included in this library help simplify a piece of code that looks like the following.</span></span>
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

<span data-ttu-id="5242e-109">簡略化されたコードは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="5242e-109">The simplified code looks like the following example.</span></span>
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

<span data-ttu-id="5242e-110">次の関数がフレームワーク ライブラリに含まれています。</span><span class="sxs-lookup"><span data-stu-id="5242e-110">The following functions are included in the Framework library:</span></span>
  
||
|:-----|
|[<span data-ttu-id="5242e-111">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="5242e-111">debugPrintf</span></span>](debugprintf.md) <br/> |
|<span data-ttu-id="5242e-112">**GetTempMemory**</span><span class="sxs-lookup"><span data-stu-id="5242e-112">**GetTempMemory**</span></span> <br/> |
|<span data-ttu-id="5242e-113">**FreeAllTempMemory**</span><span class="sxs-lookup"><span data-stu-id="5242e-113">**FreeAllTempMemory**</span></span> <br/> |
|[<span data-ttu-id="5242e-114">InitFramework</span><span class="sxs-lookup"><span data-stu-id="5242e-114">InitFramework</span></span>](initframework.md) <br/> |
|[<span data-ttu-id="5242e-115">QuitFramework</span><span class="sxs-lookup"><span data-stu-id="5242e-115">QuitFramework</span></span>](quitframework.md) <br/> |
   
|<span data-ttu-id="5242e-116">**XLOPER で使用する関数**</span><span class="sxs-lookup"><span data-stu-id="5242e-116">**Functions Used with XLOPERs**</span></span>|<span data-ttu-id="5242e-117">**XLOPER12 で使用する関数**</span><span class="sxs-lookup"><span data-stu-id="5242e-117">**Functions Used with XLOPER12s**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5242e-118">Excel</span><span class="sxs-lookup"><span data-stu-id="5242e-118">Excel</span></span>](excel-excel12f.md) <br/> |[<span data-ttu-id="5242e-119">Excel12f</span><span class="sxs-lookup"><span data-stu-id="5242e-119">Excel12f</span></span>](excel-excel12f.md) <br/> |
|[<span data-ttu-id="5242e-120">TempNum</span><span class="sxs-lookup"><span data-stu-id="5242e-120">TempNum</span></span>](tempnum-tempnum12.md) <br/> |[<span data-ttu-id="5242e-121">TempNum12</span><span class="sxs-lookup"><span data-stu-id="5242e-121">TempNum12</span></span>](tempnum-tempnum12.md) <br/> |
|[<span data-ttu-id="5242e-122">TempStr</span><span class="sxs-lookup"><span data-stu-id="5242e-122">TempStr</span></span>](tempstr.md) <br/> |[<span data-ttu-id="5242e-123">TempStr12</span><span class="sxs-lookup"><span data-stu-id="5242e-123">TempStr12</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="5242e-124">TempStrConst</span><span class="sxs-lookup"><span data-stu-id="5242e-124">TempStrConst</span></span>](tempstrconst-tempstr12.md) <br/> |[<span data-ttu-id="5242e-125">TempStr12Const</span><span class="sxs-lookup"><span data-stu-id="5242e-125">TempStr12Const</span></span>](tempstrconst-tempstr12.md) <br/> |
|[<span data-ttu-id="5242e-126">TempBool</span><span class="sxs-lookup"><span data-stu-id="5242e-126">TempBool</span></span>](tempbool-tempbool12.md) <br/> |[<span data-ttu-id="5242e-127">TempBool12</span><span class="sxs-lookup"><span data-stu-id="5242e-127">TempBool12</span></span>](tempbool-tempbool12.md) <br/> |
|[<span data-ttu-id="5242e-128">TempInt</span><span class="sxs-lookup"><span data-stu-id="5242e-128">TempInt</span></span>](tempint-tempint12.md) <br/> |[<span data-ttu-id="5242e-129">TempInt12</span><span class="sxs-lookup"><span data-stu-id="5242e-129">TempInt12</span></span>](tempint-tempint12.md) <br/> |
|[<span data-ttu-id="5242e-130">TempErr</span><span class="sxs-lookup"><span data-stu-id="5242e-130">TempErr</span></span>](temperr-temperr12.md) <br/> |[<span data-ttu-id="5242e-131">TempErr12</span><span class="sxs-lookup"><span data-stu-id="5242e-131">TempErr12</span></span>](temperr-temperr12.md) <br/> |
|[<span data-ttu-id="5242e-132">TempActiveRef</span><span class="sxs-lookup"><span data-stu-id="5242e-132">TempActiveRef</span></span>](tempactiveref-tempactiveref12.md) <br/> |[<span data-ttu-id="5242e-133">TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="5242e-133">TempActiveRef12</span></span>](tempactiveref-tempactiveref12.md) <br/> |
|[<span data-ttu-id="5242e-134">TempActiveCell</span><span class="sxs-lookup"><span data-stu-id="5242e-134">TempActiveCell</span></span>](tempactivecell-tempactivecell12.md) <br/> |[<span data-ttu-id="5242e-135">TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="5242e-135">TempActiveCell12</span></span>](tempactivecell-tempactivecell12.md) <br/> |
|[<span data-ttu-id="5242e-136">TempActiveRow</span><span class="sxs-lookup"><span data-stu-id="5242e-136">TempActiveRow</span></span>](tempactiverow-tempactiverow12.md) <br/> |[<span data-ttu-id="5242e-137">TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="5242e-137">TempActiveRow12</span></span>](tempactiverow-tempactiverow12.md) <br/> |
|[<span data-ttu-id="5242e-138">TempActiveColumn</span><span class="sxs-lookup"><span data-stu-id="5242e-138">TempActiveColumn</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |[<span data-ttu-id="5242e-139">TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="5242e-139">TempActiveColumn12</span></span>](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[<span data-ttu-id="5242e-140">TempMissing</span><span class="sxs-lookup"><span data-stu-id="5242e-140">TempMissing</span></span>](tempmissing-tempmissing12.md) <br/> |[<span data-ttu-id="5242e-141">TempMissing12</span><span class="sxs-lookup"><span data-stu-id="5242e-141">TempMissing12</span></span>](tempmissing-tempmissing12.md) <br/> |
   
<span data-ttu-id="5242e-p102">これらの関数を使用すると、DLL または XLL を記述するために必要な時間を短くできます。また、サンプル アプリケーション GENERIC から開発を開始しても開発時間を短縮できます。GENERIC.C をテンプレートとして使用して、XLL のフレームワークをセットアップしてから、既存のコードを独自のコードに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="5242e-p102">Use of these functions shortens the amount of time required to write a DLL or XLL. Starting development from the sample application GENERIC also shortens development time. Use GENERIC.C as a template to help set up the framework of an XLL, and then replace the existing code with your own.</span></span>
  
<span data-ttu-id="5242e-p103">一時 **XLOPER**/ **XLOPER12** 関数は、フレームワーク ライブラリで管理されるローカル ヒープのメモリを使って **XLOPER**/ **XLOPER12** の値を作成します。**XLOPER**/ **XLOPER12** の値は、**FreeAllTempMemory** 関数を呼び出すまで、あるいは **Excel** または **Excel12f** 関数を呼び出すまで、有効です (**Excel** 関数と **Excel12f** 関数は、すべての一時メモリを解放してから戻ります)。</span><span class="sxs-lookup"><span data-stu-id="5242e-p103">The temporary **XLOPER**/ **XLOPER12** functions create **XLOPER**/ **XLOPER12** values by using memory from a local heap managed by the Framework library. The **XLOPER**/ **XLOPER12** values remain valid until you call the **FreeAllTempMemory** function or either of the **Excel** or **Excel12f** functions. (The **Excel** and **Excel12f** functions free all temporary memory before returning.)</span></span> 
  
<span data-ttu-id="5242e-148">フレームワーク ライブラリの関数を使用するには、FRAMEWRK.H ファイルを C コードに含め、FRAMEWRK.C ファイルまたは FRMWRK32.LIB ファイルをコード プロジェクトに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5242e-148">To use the Framework library functions, you must include the FRAMEWRK.H file in your C code and add the FRAMEWRK.C or FRMWRK32.LIB files to your code project.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5242e-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="5242e-149">See also</span></span>

- [<span data-ttu-id="5242e-150">Excel XLL SDK API 関数リファレンス</span><span class="sxs-lookup"><span data-stu-id="5242e-150">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

