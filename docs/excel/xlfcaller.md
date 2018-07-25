---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- xlfcaller function [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798969"
---
# <a name="xlfcaller"></a><span data-ttu-id="3ade7-104">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="3ade7-104">xlfCaller</span></span>

 <span data-ttu-id="3ade7-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3ade7-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3ade7-106">現在実行中の DLL コマンドまたは関数を呼び出したセル、セルの範囲、メニューのコマンド、ツールバーのツール、またはオブジェクトに関する情報を返します。</span><span class="sxs-lookup"><span data-stu-id="3ade7-106">Returns information about the cell, range of cells, command on a menu, tool on a toolbar, or object that called the DLL command or function that is currently running.</span></span>
  
|<span data-ttu-id="3ade7-107">**呼び出し元のコード**</span><span class="sxs-lookup"><span data-stu-id="3ade7-107">**Code called from**</span></span>|<span data-ttu-id="3ade7-108">**返される値**</span><span class="sxs-lookup"><span data-stu-id="3ade7-108">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ade7-109">DLL</span><span class="sxs-lookup"><span data-stu-id="3ade7-109">DLL</span></span>  <br/> |<span data-ttu-id="3ade7-110">登録 ID。</span><span class="sxs-lookup"><span data-stu-id="3ade7-110">The Register ID.</span></span>  <br/> |
|<span data-ttu-id="3ade7-111">単一のセル</span><span class="sxs-lookup"><span data-stu-id="3ade7-111">A single cell</span></span>  <br/> |<span data-ttu-id="3ade7-112">単一セルの参照。</span><span class="sxs-lookup"><span data-stu-id="3ade7-112">A single-cell reference.</span></span>  <br/> |
|<span data-ttu-id="3ade7-113">複数セルの配列数式</span><span class="sxs-lookup"><span data-stu-id="3ade7-113">A multi-cell array formula</span></span>  <br/> |<span data-ttu-id="3ade7-114">複数セルの参照。</span><span class="sxs-lookup"><span data-stu-id="3ade7-114">A multi-cell reference.</span></span>  <br/> |
|<span data-ttu-id="3ade7-115">条件付き書式設定式</span><span class="sxs-lookup"><span data-stu-id="3ade7-115">A conditional formatting expression</span></span>  <br/> |<span data-ttu-id="3ade7-116">書式設定の条件が適用されているセルへの参照。</span><span class="sxs-lookup"><span data-stu-id="3ade7-116">A reference to the cell to which the formatting condition is applied.</span></span>  <br/> |
|<span data-ttu-id="3ade7-117">メニュー</span><span class="sxs-lookup"><span data-stu-id="3ade7-117">A menu</span></span>  <br/> | <span data-ttu-id="3ade7-118">4 つの要素の単一行配列</span><span class="sxs-lookup"><span data-stu-id="3ade7-118">A four-element single-row array:</span></span>  <br/>  <span data-ttu-id="3ade7-119">バーの ID。</span><span class="sxs-lookup"><span data-stu-id="3ade7-119">The bar ID.</span></span>  <br/>  <span data-ttu-id="3ade7-120">メニューの位置。</span><span class="sxs-lookup"><span data-stu-id="3ade7-120">The menu position.</span></span>  <br/>  <span data-ttu-id="3ade7-121">サブメニューの位置。</span><span class="sxs-lookup"><span data-stu-id="3ade7-121">The submenu position.</span></span>  <br/>  <span data-ttu-id="3ade7-122">コマンドの位置。</span><span class="sxs-lookup"><span data-stu-id="3ade7-122">The command position.</span></span>  <br/> |
|<span data-ttu-id="3ade7-123">ツールバー</span><span class="sxs-lookup"><span data-stu-id="3ade7-123">A toolbar</span></span>  <br/> | <span data-ttu-id="3ade7-124">2 つの要素の単一行配列</span><span class="sxs-lookup"><span data-stu-id="3ade7-124">A two-element single-row array:</span></span>  <br/>  <span data-ttu-id="3ade7-125">組み込みツールバーの場合はツールバー番号、カスタム ツールバーの場合はツールバー名。</span><span class="sxs-lookup"><span data-stu-id="3ade7-125">The toolbar number for built-in toolbars or the toolbar name for custom toolbars.</span></span>  <br/>  <span data-ttu-id="3ade7-126">ツールバー上の位置。</span><span class="sxs-lookup"><span data-stu-id="3ade7-126">The position on the toolbar.</span></span>  <br/> |
|<span data-ttu-id="3ade7-127">グラフィック オブジェクト</span><span class="sxs-lookup"><span data-stu-id="3ade7-127">A graphic object</span></span>  <br/> |<span data-ttu-id="3ade7-128">オブジェクトの識別子 (オブジェクト名)。</span><span class="sxs-lookup"><span data-stu-id="3ade7-128">The object identifier (object name).</span></span>  <br/> |
|<span data-ttu-id="3ade7-129">xlcOnEnter、ON.ENTER、イベント トラップに関連付けられたコマンド</span><span class="sxs-lookup"><span data-stu-id="3ade7-129">A command associated with an xlcOnEnter, ON.ENTER, event trap</span></span>  <br/> |<span data-ttu-id="3ade7-130">入力される 1 つまたは複数のセルへの参照。</span><span class="sxs-lookup"><span data-stu-id="3ade7-130">A reference to the cell or cells being entered.</span></span>  <br/> |
|<span data-ttu-id="3ade7-131">xlcOnDoubleclick、ON.DOUBLECLICK、イベント トラップに関連付けられたコマンド</span><span class="sxs-lookup"><span data-stu-id="3ade7-131">A command associated with an xlcOnDoubleclick, ON.DOUBLECLICK, event trap.</span></span>  <br/> |<span data-ttu-id="3ade7-132">ダブルクリックされたセル (必ずしもアクティブなセルではありません)。</span><span class="sxs-lookup"><span data-stu-id="3ade7-132">The cell that was double-clicked (not necessarily the active cell).</span></span>  <br/> |
|<span data-ttu-id="3ade7-133">Auto_Open、AutoClose、Auto_Activate または Auto_Deactivate マクロ</span><span class="sxs-lookup"><span data-stu-id="3ade7-133">Auto_Open, AutoClose, Auto_Activate or Auto_Deactivate macro</span></span>  <br/> |<span data-ttu-id="3ade7-134">呼び出し元シートの名前。</span><span class="sxs-lookup"><span data-stu-id="3ade7-134">The name of the calling sheet.</span></span>  <br/> |
|<span data-ttu-id="3ade7-135">この一覧にない他のメソッド</span><span class="sxs-lookup"><span data-stu-id="3ade7-135">Other methods not listed</span></span>  <br/> |<span data-ttu-id="3ade7-p101">#REF! エラー。</span><span class="sxs-lookup"><span data-stu-id="3ade7-p101">#REF! Error.</span></span>  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a><span data-ttu-id="3ade7-138">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="3ade7-138">Property Value/Return Value</span></span>

<span data-ttu-id="3ade7-p102">戻り値は、**XLOPER**/ **XLOPER12** データ型の **xltypeRef**、**xltypeSRef**、**xltypeNum**、**xltypeStr**、**xltypeErr**、または **xltypeMulti** です。これらの型のうちの 3 つは割り当て済みのメモリを指すため、必要がなくなったら、必ず [xlFree function](xlfree.md) の呼び出しで、**xlfCaller** の戻り値を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ade7-p102">The return value is one of the following **XLOPER**/ **XLOPER12** data types: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, or **xltypeMulti**. Since three of these types point to allocated memory, the return value of **xlfCaller** should always be freed in a call to the [xlFree function](xlfree.md) when it is no longer needed.</span></span> 
  
<span data-ttu-id="3ade7-141">**XLOPER**/ **XLOPER12** の詳細については、「[Excel でのメモリ管理](memory-management-in-excel.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ade7-141">For more information about **XLOPERs**/ **XLOPER12s** see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3ade7-142">注釈</span><span class="sxs-lookup"><span data-stu-id="3ade7-142">Remarks</span></span>

<span data-ttu-id="3ade7-p103">この関数は、DLL/XLL ワークシート関数から呼び出し可能な唯一の非ワークシート関数です。その他の XLM 情報関数は、コマンドまたはマクロ シート同等の関数からのみ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3ade7-p103">This function is the only non-worksheet function that can be called from a DLL/XLL worksheet function. Other XLM information functions can only be called from commands or macro-sheet equivalent functions.</span></span>
  
## <a name="example"></a><span data-ttu-id="3ade7-145">例</span><span class="sxs-lookup"><span data-stu-id="3ade7-145">Example</span></span>

 <span data-ttu-id="3ade7-p104">`\SAMPLES\EXAMPLE\EXAMPLE.C`。この関数はコマンド マクロ (xlcSelect) を呼び出し、マクロ シートから呼び出された場合にのみ正しく動作します。</span><span class="sxs-lookup"><span data-stu-id="3ade7-p104">`\SAMPLES\EXAMPLE\EXAMPLE.C`. This function calls a command macro (xlcSelect) and will work correctly only when called from a macro sheet.</span></span>
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="3ade7-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ade7-148">See also</span></span>



[<span data-ttu-id="3ade7-149">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="3ade7-149">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

