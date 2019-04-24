---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit function [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310858"
---
# <a name="fexit"></a><span data-ttu-id="c460c-104">fExit</span><span class="sxs-lookup"><span data-stu-id="c460c-104">fExit</span></span>

 <span data-ttu-id="c460c-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c460c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c460c-p101">GENERIC.xll をアンロードするサンプル ユーザー定義コマンド。GENERIC.xll が読み込まれると、このコマンドにアクセスするのに使用するユーザー定義メニュー [Generic] を作成します。</span><span class="sxs-lookup"><span data-stu-id="c460c-p101">Example user-defined command that unloads GENERIC.xll. When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span> 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a><span data-ttu-id="c460c-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c460c-108">Parameters</span></span>

<span data-ttu-id="c460c-109">この関数にはパラメーターはありません。</span><span class="sxs-lookup"><span data-stu-id="c460c-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c460c-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="c460c-110">Property value/Return value</span></span>

<span data-ttu-id="c460c-111">この関数は、常に 1 を返します。</span><span class="sxs-lookup"><span data-stu-id="c460c-111">The function always returns 1.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c460c-112">注釈</span><span class="sxs-lookup"><span data-stu-id="c460c-112">Remarks</span></span>

<span data-ttu-id="c460c-p102">これは、GENERIC.xll を終了するためにユーザーが開始するルーチンです。この関数で単に `UNREGISTER("GENERIC.XLL")` を呼び出すことは避けてください。その場合、この DLL 内のすべての関数が強制的に登録解除されます。これらの関数が他のいずれかに登録されている場合も同じです。代わりに、一度に 1 つずつ関数を登録解除してください。</span><span class="sxs-lookup"><span data-stu-id="c460c-p102">This is a user-initiated routine to exit GENERIC.xll You should avoid simply calling  `UNREGISTER("GENERIC.XLL")` in this function. This would forcefully unregister all the functions in this DLL, even if they are registered somewhere else. Instead, unregister the functions one at a time.</span></span> 
  
### <a name="example"></a><span data-ttu-id="c460c-116">例</span><span class="sxs-lookup"><span data-stu-id="c460c-116">Example</span></span>

<span data-ttu-id="c460c-117">この関数のソース コードについては、`\SAMPLES\GENERIC\GENERIC.C` を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c460c-117">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c460c-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="c460c-118">See also</span></span>



[<span data-ttu-id="c460c-119">汎用 DLL の関数</span><span class="sxs-lookup"><span data-stu-id="c460c-119">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

