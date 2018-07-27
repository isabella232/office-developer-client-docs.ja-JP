---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper function [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798993"
---
# <a name="xloper12toxloper"></a><span data-ttu-id="90761-104">XLOper12ToXLOper</span><span class="sxs-lookup"><span data-stu-id="90761-104">XLOper12ToXLOper</span></span>

<span data-ttu-id="90761-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="90761-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="90761-106">新しい **XLOPER12** から古いい **XLOPER** への変換に使用する変換ルーチンです。</span><span class="sxs-lookup"><span data-stu-id="90761-106">Conversion routine used to convert from the new **XLOPER12** to the old **XLOPER**.</span></span>
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a><span data-ttu-id="90761-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="90761-107">Parameters</span></span>

<span data-ttu-id="90761-108">_pxloper12_ (**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="90761-108">_pxloper12_ (**LPXLOPER12**)</span></span>
  
<span data-ttu-id="90761-109">変換対象のソース **XLOPER12** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="90761-109">Pointer to the source **XLOPER12** to be converted.</span></span> 
  
<span data-ttu-id="90761-110">_pxloper_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="90761-110">_pxloper_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="90761-111">変換された値を格納するターゲット **XLOPER** へのポインター。</span><span class="sxs-lookup"><span data-stu-id="90761-111">Pointer to the target **XLOPER** to contain the converted value.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="90761-112">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="90761-112">Property Value/Return Value</span></span>

<span data-ttu-id="90761-113">変換が成功した場合は **TRUE**。それ以外の場合は **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="90761-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="90761-114">注釈</span><span class="sxs-lookup"><span data-stu-id="90761-114">Remarks</span></span>

<span data-ttu-id="90761-p101">**XLOPER12** の型によっては、この関数は、変換されてターゲット **XLOPER** をポイントする値に新しいメモリ バッファーを割り当てます。変換が成功した場合、そのコピーに関連付けられたメモリを解放する責任は、呼び出し元にあります。メモリを解放するには、**FreeXLOperT** を使用するか、**free** を使用して直接解放します。</span><span class="sxs-lookup"><span data-stu-id="90761-p101">Depending on the type of the **XLOPER12**, this function allocates a new memory buffer for the converted values, which are pointed to in the target **XLOPER**. The caller is responsible for freeing any memory associated with the copy if the conversion is a success; **FreeXLOperT** can be used, or it can be done directly by using **free**.</span></span>
  
<span data-ttu-id="90761-117">変換が失敗した場合は、呼び出し元でメモリを解放する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="90761-117">If the conversion fails, the caller does not need to free any memory.</span></span>
  
<span data-ttu-id="90761-118">**XLOPER12** から **XLOPER** への変換は、**XLOPER12** に収まりきらないほど大きい配列や参照、または長い文字列が **XLOPER** に格納されていると、失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="90761-118">Conversion from an **XLOPER12** to an **XLOPER** can fail when the **XLOPER12** contains an array or reference that is too large or a string that is too long for the **XLOPER** to contain.</span></span> 
  
<span data-ttu-id="90761-119">**XLOPER12** の Unicode ワイド文字文字列は、ロケールに依存する方法で **XLOPER** の ASCII バイト文字列に変換されます。</span><span class="sxs-lookup"><span data-stu-id="90761-119">**XLOPER12** Unicode wide-character strings are converted to **XLOPER** ASCII byte strings in a way that is locale-dependent.</span></span> 
  
<span data-ttu-id="90761-p102">**XLOPER12** **xltypeInt** は 32 ビット符号付き整数です。**XLOPER** **xltypeInt** は 16 ビット符号付き整数です。指定された **XLOPER12** 整数が **XLOPER** 整数の制限を超える場合は、その整数は 8 バイトの double に変換され、**xltypeNum** 型の **XLOPER** で返されます。この場合にのみ、この関数は変換した **XLOPER** の型を変更します。</span><span class="sxs-lookup"><span data-stu-id="90761-p102">The **XLOPER12** **xltypeInt** is a 32-bit signed integer, whereas the **XLOPER** **xltypeInt** is a 16-bit signed integer. When a supplied **XLOPER12** integer exceeds the limit of an **XLOPER** integer, the integer is converted to an 8-byte double and returned in an **XLOPER** of type **xltypeNum**. This is the only case in which this function changes the type of the converted **XLOPER**.</span></span>
  
### <a name="example"></a><span data-ttu-id="90761-123">例</span><span class="sxs-lookup"><span data-stu-id="90761-123">Example</span></span>

<span data-ttu-id="90761-124">この関数のコードについては、`\SAMPLES\FRAMEWRK\FRAMEWRK.C` ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="90761-124">See the file  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` for the code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="90761-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="90761-125">See also</span></span>

- [<span data-ttu-id="90761-126">フレームワーク ライブラリの関数</span><span class="sxs-lookup"><span data-stu-id="90761-126">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

