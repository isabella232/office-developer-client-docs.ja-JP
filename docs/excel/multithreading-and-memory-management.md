---
title: マルチスレッド処理とメモリ管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414467"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="42429-103">マルチスレッド処理とメモリ管理</span><span class="sxs-lookup"><span data-stu-id="42429-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="42429-104">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="42429-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="42429-p101">メモリの適切な処理は、Microsoft Excel の信頼性の高い XLL アドインの作成に不可欠です。適切なメモリ バッファーの割り当てや、不要になったバッファー メモリの解放を行わないと、パフォーマンスが低下し、リソース競合が発生し、Excel が不安定になります。</span><span class="sxs-lookup"><span data-stu-id="42429-p101">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel. Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="42429-p102">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating. In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span><span class="sxs-lookup"><span data-stu-id="42429-p102">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating. In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="42429-109">次のトピックでは、XLL でメモリやスレッドを管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="42429-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="42429-110">Excel のメモリ管理</span><span class="sxs-lookup"><span data-stu-id="42429-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="42429-111">Excel におけるマルチスレッド処理とメモリ競合</span><span class="sxs-lookup"><span data-stu-id="42429-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="42429-112">Excel でのマルチスレッド再計算</span><span class="sxs-lookup"><span data-stu-id="42429-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="42429-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="42429-113">See also</span></span>



[<span data-ttu-id="42429-114">Excel XLL の開発</span><span class="sxs-lookup"><span data-stu-id="42429-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

