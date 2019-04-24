---
title: Excel XLL SDK API �֐����t�@�����X
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api function reference [excel 2007],functions [Excel 2007],reference [Excel 2007],Excel 2007 XLL Software Development Kit, reference
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: e116021a3dc24de7decbe0dad76cc762cd66d032
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304124"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="550a4-104">Excel XLL SDK API 関数リファレンス</span><span class="sxs-lookup"><span data-stu-id="550a4-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="550a4-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="550a4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="550a4-106">Microsoft Excel 2013 XLL SDK には、XLL の記述を高速化するために設計されたフレームワーク ライブラリのソース ファイルと 2 つのサンプル プロジェクト (Example と Generic) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="550a4-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="550a4-107">このセクションでは、次の関数リファレンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="550a4-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="550a4-108">XLL ファイルが呼び出すことのできる Excel コールバック。</span><span class="sxs-lookup"><span data-stu-id="550a4-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="550a4-109">Microsoft Excel が検索する XLL コールバック。</span><span class="sxs-lookup"><span data-stu-id="550a4-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="550a4-110">サンプルとフレームワークのプロジェクトの主要な機能。</span><span class="sxs-lookup"><span data-stu-id="550a4-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="550a4-111">サンプル プロジェクト</span><span class="sxs-lookup"><span data-stu-id="550a4-111">Sample projects</span></span>

<span data-ttu-id="550a4-112">Excel 2013 XLL SDK には、次のサンプル プロジェクトのソース ファイルと Microsoft Visual Studio のプロジェクト ファイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="550a4-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="550a4-113">**Framework** プロジェクト (`SAMPLES\FRAMEWRK\`) には、ライブラリ (FRAMEWRK.lib) にビルドできるプロジェクトが含まれており、他の XLL プロジェクトにリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="550a4-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="550a4-114">ライブラリには、XLL をより簡単に記述するための多くの関数とツールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="550a4-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="550a4-115">このライブラリは、他の両方のプロジェクトで、ヘッダー ファイル FRAMEWRK.h と組み合わせて使われます。</span><span class="sxs-lookup"><span data-stu-id="550a4-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="550a4-116">**Example** プロジェクト (`SAMPLES\EXAMPLE\`) には、XLL (EXAMPLE.xll) にビルドできるプロジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="550a4-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="550a4-117">XLL には、フレームワーク ライブラリを使う多くの例や、**xlAutoOpen** などの XLL アドイン インターフェイスの実装例が含まれます。</span><span class="sxs-lookup"><span data-stu-id="550a4-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="550a4-118">**Generic** プロジェクト (`SAMPLES\GENERIC\`) には、XLL (GENERIC.xll) にビルドできるプロジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="550a4-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="550a4-119">XLL は、関数とコマンドのいくつかの例を示します。また、独自の XLL を記述するための土台とするのに適しています。</span><span class="sxs-lookup"><span data-stu-id="550a4-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="550a4-120">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="550a4-120">In this section</span></span>

- [<span data-ttu-id="550a4-121">アドイン マネージャーと XLL インターフェイス関数</span><span class="sxs-lookup"><span data-stu-id="550a4-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="550a4-122">C API コールバック関数 Excel4、Excel12</span><span class="sxs-lookup"><span data-stu-id="550a4-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="550a4-123">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="550a4-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="550a4-124">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="550a4-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="550a4-125">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="550a4-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="550a4-126">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="550a4-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="550a4-127">Excel クラスター コネクタ関数</span><span class="sxs-lookup"><span data-stu-id="550a4-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="550a4-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="550a4-128">See also</span></span>

- [<span data-ttu-id="550a4-129">Excel での C API を使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="550a4-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="550a4-130">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="550a4-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

