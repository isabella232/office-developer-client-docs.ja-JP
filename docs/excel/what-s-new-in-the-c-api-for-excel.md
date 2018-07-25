---
title: Excel 用 C API の新機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],新機能
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19798948"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="07b4c-104">Excel 用 C API の新機能</span><span class="sxs-lookup"><span data-stu-id="07b4c-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="07b4c-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="07b4c-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="07b4c-106">Microsoft Excel 2013 と同時に、Microsoft Excel 2013 XLL ソフトウェア開発キット (SDK) にも次の機能のサポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="07b4c-106">In conjunction with xl15long, the xl15long XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="07b4c-107">**新機能**</span><span class="sxs-lookup"><span data-stu-id="07b4c-107">**New Functions**</span></span>
    
    <span data-ttu-id="07b4c-108">Microsoft Excel 2013 XLL SDK は、Excel 2013 のすべての新しいワークシート関数へのコール バックをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="07b4c-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="07b4c-109">Excel 2013 関数の呼び出しの詳細については、「[DLL または XLL から Excel に呼び出す](calling-into-excel-from-the-dll-or-xll.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07b4c-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="07b4c-110">**非同期のユーザー定義関数**</span><span class="sxs-lookup"><span data-stu-id="07b4c-110">**Asynchronous User-Defined Functions**</span></span>
    
    <span data-ttu-id="07b4c-111">Excel 2013 ではユーザー定義関数 (UDF) の非同期の呼び出しをサポートしています。これは、さまざまな計算の同時実行を可能にすることで、パフォーマンスを向上します。</span><span class="sxs-lookup"><span data-stu-id="07b4c-111">xl15short supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time. For more information about asynchronous UDFs, see Asynchronous User-Defined Functions.</span></span> <span data-ttu-id="07b4c-112">非同期 UDF の詳細については、「[非同期のユーザー定義関数](asynchronous-user-defined-functions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07b4c-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="07b4c-113">**クラスター コネクタ**</span><span class="sxs-lookup"><span data-stu-id="07b4c-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="07b4c-114">クラスター コネクタは、UDF を高パフォーマンスの計算クラスター上で実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="07b4c-114">Cluster connectors enable UDFs to run on high-performance compute clusters. For more information about creating cluster connectors, see Developing Excel 2013 Cluster Connectors.</span></span> <span data-ttu-id="07b4c-115">クラスター コネクタの作成の詳細については、「[Excel クラスター コネクタの開発](developing-excel-cluster-connectors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07b4c-115">Cluster connectors enable UDFs to run on high-performance compute clusters. For more information about creating cluster connectors, see [Developing Excel 2013 Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="07b4c-116">計算クラスター上で実行する予定の XLL アドインは、クラスター セーフ関数のみを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b4c-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions. For more information about the functions you can use, see Excel 2013 XLL SDK API Function Reference and Cluster Safe Functions.</span></span> <span data-ttu-id="07b4c-117">使用可能な関数の詳細については、「[Excel XLL SDK API 関数リファレンス](excel-xll-sdk-api-function-reference.md)」および「[クラスター セーフ関数](cluster-safe-functions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07b4c-117">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions. For more information about the functions you can use, see [Excel 2013 XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="07b4c-118">**64 ビットのサポート**</span><span class="sxs-lookup"><span data-stu-id="07b4c-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="07b4c-119">32 ビットと 64 ビットの XLL をコンパイルおよびリンクできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="07b4c-119">You can now compile and link both 32-bit and 64-bit XLLs. For more information, see Creating XLLs.</span></span> <span data-ttu-id="07b4c-120">詳細については、「[XLL を作成する](creating-xlls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07b4c-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="07b4c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="07b4c-121">See also</span></span>



[<span data-ttu-id="07b4c-122">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="07b4c-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="07b4c-123">Excel での C API を使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="07b4c-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="07b4c-124">Excel におけるマルチスレッド処理とメモリ競合</span><span class="sxs-lookup"><span data-stu-id="07b4c-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="07b4c-125">Excel XLL SDK の概要</span><span class="sxs-lookup"><span data-stu-id="07b4c-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

