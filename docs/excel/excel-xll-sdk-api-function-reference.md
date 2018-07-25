---
title: Excel XLL SDK API 関数リファレンス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api function reference [excel 2007],functions [Excel 2007],reference [Excel 2007],Excel 2007 XLL Software Development Kit, reference
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798874"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="14c68-104">Excel XLL SDK API 関数リファレンス</span><span class="sxs-lookup"><span data-stu-id="14c68-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="14c68-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="14c68-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="14c68-106">Microsoft Excel 2013 XLL SDK には、XLL の記述を高速化するために設計されたフレームワーク ライブラリのソース ファイルと 2 つのサンプル プロジェクト (Example と Generic) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="14c68-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="14c68-107">このセクションでは、次の関数リファレンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="14c68-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="14c68-108">XLL ファイルが呼び出すことのできる Excel コールバック。</span><span class="sxs-lookup"><span data-stu-id="14c68-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="14c68-109">Microsoft Excel が検索する XLL コールバック。</span><span class="sxs-lookup"><span data-stu-id="14c68-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="14c68-110">サンプルとフレームワークのプロジェクトの主要な機能。</span><span class="sxs-lookup"><span data-stu-id="14c68-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="14c68-111">サンプル プロジェクト</span><span class="sxs-lookup"><span data-stu-id="14c68-111">Sample Projects</span></span>

<span data-ttu-id="14c68-112">Excel 2013 XLL SDK には、次のサンプル プロジェクトのソース ファイルと Microsoft Visual Studio のプロジェクト ファイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="14c68-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="14c68-113">**Framework** プロジェクト (`SAMPLES\FRAMEWRK\`) には、ライブラリ (FRAMEWRK.lib) にビルドできるプロジェクトが含まれており、他の XLL プロジェクトにリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="14c68-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="14c68-114">ライブラリには、XLL をより簡単に記述するための多くの関数とツールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="14c68-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="14c68-115">このライブラリは、他の両方のプロジェクトで、ヘッダー ファイル FRAMEWRK.h と組み合わせて使われます。</span><span class="sxs-lookup"><span data-stu-id="14c68-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="14c68-116">**Example** プロジェクト (`SAMPLES\EXAMPLE\`) には、XLL (EXAMPLE.xll) にビルドできるプロジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="14c68-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="14c68-117">XLL には、フレームワーク ライブラリを使う多くの例や、**xlAutoOpen** などの XLL アドイン インターフェイスの実装例が含まれます。</span><span class="sxs-lookup"><span data-stu-id="14c68-117">The Example project (SAMPLES\EXAMPLE\) contains a project that can be built to an XLL, EXAMPLE.xll. The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="14c68-118">**Generic** プロジェクト (`SAMPLES\GENERIC\`) には、XLL (GENERIC.xll) にビルドできるプロジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="14c68-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="14c68-119">XLL は、関数とコマンドのいくつかの例を示します。また、独自の XLL を記述するための土台とするのに適しています。</span><span class="sxs-lookup"><span data-stu-id="14c68-119">The Generic project (SAMPLES\GENERIC\) contains a project that can be built to an XLL, GENERIC.xll. The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="14c68-120">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="14c68-120">In this section</span></span>

- [<span data-ttu-id="14c68-121">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="14c68-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="14c68-122">C API コールバック関数 Excel4、Excel12</span><span class="sxs-lookup"><span data-stu-id="14c68-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="14c68-123">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="14c68-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="14c68-124">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="14c68-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="14c68-125">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="14c68-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="14c68-126">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="14c68-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="14c68-127">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="14c68-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="14c68-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="14c68-128">See also</span></span>

- [<span data-ttu-id="14c68-129">Excel での C API を使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="14c68-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="14c68-130">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="14c68-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

