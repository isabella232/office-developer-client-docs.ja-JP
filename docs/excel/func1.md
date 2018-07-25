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
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798880"
---
# <a name="func1"></a><span data-ttu-id="111d7-104">Func1</span><span class="sxs-lookup"><span data-stu-id="111d7-104">Func1</span></span>

 <span data-ttu-id="111d7-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="111d7-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="111d7-p101">ユーザー定義のワークシート関数の例で、返される静的な文字列値について説明します。GENERIC.xll が読み込まれると、GENERIC.xll によってこの関数が登録されて、ワークシートから呼び出すことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="111d7-p101">Example user-defined worksheet function demonstrates the return of a static string value. When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="111d7-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="111d7-108">Parameters</span></span>

 <span data-ttu-id="111d7-109">_px_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="111d7-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="111d7-110">この引数は無視され、Microsoft Excel をトリガーして関数を呼び出すためだけの役目を果たします。</span><span class="sxs-lookup"><span data-stu-id="111d7-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="111d7-111">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="111d7-111">Property Value/Return Value</span></span>

 <span data-ttu-id="111d7-112">**LPXLOPER12**: 常に文字列 "Func1"</span><span class="sxs-lookup"><span data-stu-id="111d7-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="111d7-113">例</span><span class="sxs-lookup"><span data-stu-id="111d7-113">Example</span></span>

<span data-ttu-id="111d7-114">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="111d7-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="111d7-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="111d7-115">See also</span></span>



[<span data-ttu-id="111d7-116">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="111d7-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

