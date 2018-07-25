---
title: 重要で役に立つ C API XLM 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api xlm
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 410a6009bf6bbb8146dcc1354e7f5688c28d96c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798793"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="177bb-104">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="177bb-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="177bb-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="177bb-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="177bb-p101">このセクションで説明する関数は、DLL や XLL 開発者に特に便利な Microsoft Excel のコールバック関数です。これらの関数のうち、**xlfRegister** は、XLL と DLL で関数とコマンドを登録して Excel から直接呼び出せるようにする場合、必要不可欠です。DLL と XLL の関数やコマンドを登録解除するには、**xlfUnregister** 関数と **xlfSetName** 関数を組み合わせて使用します。</span><span class="sxs-lookup"><span data-stu-id="177bb-p101">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers. Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel. The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="177bb-p102">多くの関数は、XLL の開発時の役立つ C API を通じて、Excel によって公開されます。これらは Excel ワークシートに対応する関数と、XLM マクロ シートで使用できる関数およびコマンドです。</span><span class="sxs-lookup"><span data-stu-id="177bb-p102">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs. They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="177bb-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="177bb-111">In this section</span></span>

[<span data-ttu-id="177bb-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="177bb-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="177bb-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="177bb-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="177bb-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="177bb-114">xlfgetdef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="177bb-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="177bb-115">xlfgetname</span></span>](xlfgetname.md)
  
[<span data-ttu-id="177bb-116">xlfRegister (形式 1)</span><span class="sxs-lookup"><span data-stu-id="177bb-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="177bb-117">xlfRegister (形式 2)</span><span class="sxs-lookup"><span data-stu-id="177bb-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="177bb-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="177bb-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="177bb-119">xlfUnregister (形式 1)</span><span class="sxs-lookup"><span data-stu-id="177bb-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="177bb-120">xlfUnregister (形式 2)</span><span class="sxs-lookup"><span data-stu-id="177bb-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="177bb-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="177bb-121">xlfSetName</span></span>](xlfsetname.md)
  

