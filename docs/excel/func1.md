---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- func1 function [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304082"
---
# <a name="func1"></a><span data-ttu-id="02900-104">Func1</span><span class="sxs-lookup"><span data-stu-id="02900-104">Func1</span></span>

 <span data-ttu-id="02900-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="02900-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="02900-p101">ユーザー定義のワークシート関数の例で、返される静的な文字列値について説明します。GENERIC.xll が読み込まれると、GENERIC.xll によってこの関数が登録されて、ワークシートから呼び出すことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="02900-p101">Example user-defined worksheet function demonstrates the return of a static string value. When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="02900-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="02900-108">Parameters</span></span>

 <span data-ttu-id="02900-109">_px_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="02900-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="02900-110">この引数は無視され、Microsoft Excel をトリガーして関数を呼び出すためだけの役目を果たします。</span><span class="sxs-lookup"><span data-stu-id="02900-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="02900-111">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="02900-111">Property value/Return value</span></span>

 <span data-ttu-id="02900-112">**LPXLOPER12**: 常に文字列 "Func1"</span><span class="sxs-lookup"><span data-stu-id="02900-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="02900-113">例</span><span class="sxs-lookup"><span data-stu-id="02900-113">Example</span></span>

<span data-ttu-id="02900-114">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02900-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="02900-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="02900-115">See also</span></span>



[<span data-ttu-id="02900-116">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="02900-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

