---
title: Excel 用 C API の新機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c 言語の api [excel 2007]、新機能
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19798948"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="08d24-104">Excel 用 C API の新機能</span><span class="sxs-lookup"><span data-stu-id="08d24-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="08d24-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="08d24-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="08d24-106">Microsoft Excel 2013 と協力して、Microsoft Excel 2013 XLL ソフトウェア開発キット (SDK) には、次の機能のサポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="08d24-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="08d24-107">**新しい関数**</span><span class="sxs-lookup"><span data-stu-id="08d24-107">**New Functions**</span></span>
    
    <span data-ttu-id="08d24-108">Microsoft Excel 2013 XLL SDK には、Excel 2013 で、新しいワークシート関数のすべてのコールバックがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="08d24-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="08d24-109">Excel 2013 関数を呼び出す方法の詳細については、 [DLL や xll ファイルから Excel への呼び出し](calling-into-excel-from-the-dll-or-xll.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08d24-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="08d24-110">**非同期のユーザー定義関数**</span><span class="sxs-lookup"><span data-stu-id="08d24-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="08d24-111">Excel 2013 は、同時に実行するいくつかの計算を有効にすると、パフォーマンスが向上する、ユーザー定義関数 (UDF) を非同期的に呼び出すことをサポートします。</span><span class="sxs-lookup"><span data-stu-id="08d24-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="08d24-112">非同期のユーザー定義関数の詳細については、 [Asynchronous User-Defined 関数](asynchronous-user-defined-functions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08d24-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="08d24-113">**クラスター コネクタ**</span><span class="sxs-lookup"><span data-stu-id="08d24-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="08d24-114">クラスター コネクタは、ハイ パフォーマンス計算クラスター上で実行するには、ユーザー定義関数を有効にします。</span><span class="sxs-lookup"><span data-stu-id="08d24-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="08d24-115">クラスター コネクタを作成する方法の詳細については、 [Excel クラスター コネクタの開発](developing-excel-cluster-connectors.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08d24-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="08d24-116">計算クラスター上で実行する XLL アドインでは、クラスター セーフな関数だけを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="08d24-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="08d24-117">関数の詳細についてを使用して、 [Excel XLL SDK API 関数を参照](excel-xll-sdk-api-function-reference.md)し、[クラスターの安全な関数](cluster-safe-functions.md)を参照できます。</span><span class="sxs-lookup"><span data-stu-id="08d24-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="08d24-118">**64 ビットのサポート**</span><span class="sxs-lookup"><span data-stu-id="08d24-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="08d24-119">コンパイルし、両方の 32 ビットおよび 64 ビットの Xll をリンクできます。</span><span class="sxs-lookup"><span data-stu-id="08d24-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="08d24-120">詳細については、 [Xll の作成](creating-xlls.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08d24-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08d24-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="08d24-121">See also</span></span>



[<span data-ttu-id="08d24-122">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="08d24-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="08d24-123">Excel �ł� C API ��g�p�����v���O���~���O</span><span class="sxs-lookup"><span data-stu-id="08d24-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="08d24-124">Excel 2007 �ɂ�����}���\`�X���b�h�����ƃ���������</span><span class="sxs-lookup"><span data-stu-id="08d24-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="08d24-125">Excel XLL SDK �̊T�v</span><span class="sxs-lookup"><span data-stu-id="08d24-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

