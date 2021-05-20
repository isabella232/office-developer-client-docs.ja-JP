---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- tempmissing function [excel 2007],TempMissing12 function [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435958"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="085ac-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="085ac-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="085ac-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="085ac-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="085ac-106">**xltypeMissing** 型の一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="085ac-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="085ac-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="085ac-107">Parameters</span></span>

<span data-ttu-id="085ac-108">この関数にパラメーターはありません。</span><span class="sxs-lookup"><span data-stu-id="085ac-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="085ac-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="085ac-109">Return value</span></span>

<span data-ttu-id="085ac-110">**xltypeMissing** **XLOPER**/ **XLOPER12** へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="085ac-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="085ac-111">例</span><span class="sxs-lookup"><span data-stu-id="085ac-111">Example</span></span>

<span data-ttu-id="085ac-p101">この例では、**TempMissing12** を使用して **xlcWorkspace** の 3 つの欠落した引数を指定し、その後に **ブール値** **FALSE** を続けて、ワークシートのスクロール バーの表示を抑制します。最初の 3 つの引数は、他のワークスペースの設定に対応しますが、それらの設定は影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="085ac-p101">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars. The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="085ac-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="085ac-114">See also</span></span>



[<span data-ttu-id="085ac-115">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="085ac-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

