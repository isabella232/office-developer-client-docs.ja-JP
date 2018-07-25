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
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798953"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="448dd-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="448dd-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="448dd-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="448dd-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="448dd-106">**xltypeMissing** 型の一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="448dd-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="448dd-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="448dd-107">Parameters</span></span>

<span data-ttu-id="448dd-108">この関数にパラメーターはありません。</span><span class="sxs-lookup"><span data-stu-id="448dd-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="448dd-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="448dd-109">Return value</span></span>

<span data-ttu-id="448dd-110">**xltypeMissing** **XLOPER**/ **XLOPER12** へのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="448dd-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="448dd-111">例</span><span class="sxs-lookup"><span data-stu-id="448dd-111">Example</span></span>

<span data-ttu-id="448dd-p101">この例では、**TempMissing12** を使用して **xlcWorkspace** の 3 つの欠落した引数を指定し、その後に**ブール値** **FALSE** を続けて、ワークシートのスクロール バーの表示を抑制します。最初の 3 つの引数は、他のワークスペースの設定に対応しますが、それらの設定は影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="448dd-p101">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars. The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="448dd-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="448dd-114">See also</span></span>



[<span data-ttu-id="448dd-115">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="448dd-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

