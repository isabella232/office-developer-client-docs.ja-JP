---
title: C API コールバック関数 Excel4、Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api callback
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 221ea4c9c706d11acd31d3f2870d326a7189d299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798757"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="ba05a-104">C API コールバック関数 Excel4、Excel12</span><span class="sxs-lookup"><span data-stu-id="ba05a-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="ba05a-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ba05a-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ba05a-p101">**Excel4** 関数と **Excel12** 関数は、DLL による内部 Microsoft Excel ワークシート関数、マクロ シート関数またはコマンド、XLL 専用の特殊な関数またはコマンドの呼び出しを可能にするために提供されています。**Excel4** 関数は、Excel の最近のすべてのバージョンでサポートされています。**Excel12** 関数は、Excel 2007 以降でサポートされています。両方の関数は 2 つのフォームで提供されます。</span><span class="sxs-lookup"><span data-stu-id="ba05a-p101">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command. All recent versions of Excel support the **Excel4** function. Starting in Excel 2007 the **Excel12** function is supported. Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="ba05a-110">可変長引数リスト フォーム (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="ba05a-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="ba05a-111">引数の配列フォーム (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="ba05a-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="ba05a-112">引数がこれらのコールバックに渡される方法を除いて、2 つのフォームは機能的に同等です。</span><span class="sxs-lookup"><span data-stu-id="ba05a-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent. The basic concepts for both forms are fully described in Excel4/Excel12. Excel4v/Excel12v covers other issues about this form.</span></span> <span data-ttu-id="ba05a-113">両方のフォームの基本概念については、「[Excel4/Excel12](excel4-excel12.md)」で詳しく説明されています。</span><span class="sxs-lookup"><span data-stu-id="ba05a-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="ba05a-114">「[Excel4v/Excel12v](excel4v-excel12v.md)」では、このフォームに関するその他の問題が取り上げられています。</span><span class="sxs-lookup"><span data-stu-id="ba05a-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="ba05a-115">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="ba05a-115">In this section</span></span>

[<span data-ttu-id="ba05a-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="ba05a-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="ba05a-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="ba05a-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

