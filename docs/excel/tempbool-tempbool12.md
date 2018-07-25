---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- tempbool function [excel 2007],TempBool12 function [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798946"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="a41ee-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="a41ee-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="a41ee-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a41ee-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a41ee-106">**ブール値** **TRUE** または **FALSE** を含む一時 **XLOPER**/ **XLOPER12** を作成するフレームワーク ライブラリ関数。</span><span class="sxs-lookup"><span data-stu-id="a41ee-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="a41ee-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a41ee-107">Parameters</span></span>

 <span data-ttu-id="a41ee-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="a41ee-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="a41ee-109">**FALSE** を返すには 0 を使用します。**TRUE** を返すには 0 以外の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a41ee-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a41ee-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="a41ee-110">Property Value/Return Value</span></span>

<span data-ttu-id="a41ee-111">渡された論理値を含む **xltypeBool** **ブール値** を返します。</span><span class="sxs-lookup"><span data-stu-id="a41ee-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a41ee-112">例</span><span class="sxs-lookup"><span data-stu-id="a41ee-112">Example</span></span>

<span data-ttu-id="a41ee-p101">次の例では、**TempBool12** 関数を使用して、ステータス バーをクリアにします。[Excel/Excel12f](excel-excel12f.md) 関数が呼び出されると、一時メモリが解放されます。</span><span class="sxs-lookup"><span data-stu-id="a41ee-p101">The following example uses the **TempBool12** function to clear the status bar. Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="a41ee-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="a41ee-115">See also</span></span>



[<span data-ttu-id="a41ee-116">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="a41ee-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

