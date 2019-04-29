---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12 function [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404597"
---
# <a name="xlopertoxloper12"></a><span data-ttu-id="a1c30-104">XLOperToXLOper12</span><span class="sxs-lookup"><span data-stu-id="a1c30-104">XLOperToXLOper12</span></span>

<span data-ttu-id="a1c30-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a1c30-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a1c30-106">古い **XLOPER** から新しい **XLOPER12** への変換に使用する変換ルーチン。</span><span class="sxs-lookup"><span data-stu-id="a1c30-106">Conversion routine used to convert from the old **XLOPER** to the new **XLOPER12**.</span></span>
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a><span data-ttu-id="a1c30-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1c30-107">Parameters</span></span>

<span data-ttu-id="a1c30-108">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="a1c30-108">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="a1c30-109">変換対象のソース **XLOPER** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1c30-109">Pointer to the source **XLOPER** to be converted.</span></span> 
  
<span data-ttu-id="a1c30-110">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="a1c30-110">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="a1c30-111">変換された値を格納するターゲット **XLOPER12** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1c30-111">Pointer to the target **XLOPER12** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a1c30-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="a1c30-112">Property value/Return value</span></span>

<span data-ttu-id="a1c30-113">変換が成功した場合は **TRUE**。それ以外の場合は **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a1c30-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1c30-114">注釈</span><span class="sxs-lookup"><span data-stu-id="a1c30-114">Remarks</span></span>

<span data-ttu-id="a1c30-p101">**XLOPER** の型によっては、この関数は、変換されてターゲット **XLOPER12** をポイントする値に新しいメモリ バッファーを割り当てます。変換が成功した場合、そのコピーに関連付けられたメモリを解放する責任は、呼び出し元にあります。メモリを解放するには、**FreeXLOper12T** を使用するか、**free** を使用して直接解放します。</span><span class="sxs-lookup"><span data-stu-id="a1c30-p101">Depending on the type of the **XLOPER**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER12**. The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOper12T** can be used, or it can be done directly using **free**.</span></span>
  
<span data-ttu-id="a1c30-117">変換が失敗した場合は、呼び出し元でメモリを解放する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a1c30-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="a1c30-p102">通常は、任意の **XLOPER** を **XLOPER12** に変換できます。それとは対照的に、**XLOPER12** を **XLOPER** に変換する場合、**XLOPER** に格納するには大きすぎる配列または参照が **XLOPER12** に含まれていると、変換は失敗します。</span><span class="sxs-lookup"><span data-stu-id="a1c30-p102">In general, conversion from any **XLOPER** to an **XLOPER12** is possible. In contrast, conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="a1c30-120">**XLOPER** ASCII バイト文字列は、ロケールに依存する方法で **XLOPER12** Unicode 再度文字列に変換されます。</span><span class="sxs-lookup"><span data-stu-id="a1c30-120">**XLOPER** ASCII byte strings are converted to **XLOPER12** Unicode wide-character strings in a way that is locale-dependent.</span></span> 
  
### <a name="example"></a><span data-ttu-id="a1c30-121">例</span><span class="sxs-lookup"><span data-stu-id="a1c30-121">Example</span></span>

<span data-ttu-id="a1c30-122">この関数のコードについては、`\SAMPLES\FRAMEWRK\FRAMEWRK.C` ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1c30-122">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  

