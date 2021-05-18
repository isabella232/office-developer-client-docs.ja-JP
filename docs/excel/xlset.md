---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- xlset function [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404604"
---
# <a name="xlset"></a><span data-ttu-id="01331-104">xlSet</span><span class="sxs-lookup"><span data-stu-id="01331-104">xlSet</span></span>

<span data-ttu-id="01331-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="01331-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="01331-p101">定数値をセルや範囲にすばやく配置します。詳しくは、「[Excel アドイン (XLL) 開発における既知の問題](known-issues-in-excel-xll-development.md)」の「xlSet と配列数式を含むブック」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="01331-p101">Puts constant values into cells or ranges very quickly. For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a><span data-ttu-id="01331-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="01331-108">Parameters</span></span>

<span data-ttu-id="01331-109">_pxReference_ (**xltypeRef** または **xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="01331-109">_pxReference_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="01331-p102">A rectangular reference describing the target cell or cells. The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span><span class="sxs-lookup"><span data-stu-id="01331-p102">A rectangular reference describing the target cell or cells. The reference must describe adjacent cells, so that in an **xltypeRef** `val.mref.lpmref->count` must be set to 1.</span></span> 
  
<span data-ttu-id="01331-112">_pxValue_</span><span class="sxs-lookup"><span data-stu-id="01331-112">_pxValue_</span></span>
  
<span data-ttu-id="01331-p103">セルに配置される値です。詳しくは、「解説」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="01331-p103">The value or values to be placed into the cell or cells. For more information, see the "Remarks" section.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01331-115">注釈</span><span class="sxs-lookup"><span data-stu-id="01331-115">Remarks</span></span>

### <a name="pxvalue-argument"></a><span data-ttu-id="01331-116">pxValue 引数</span><span class="sxs-lookup"><span data-stu-id="01331-116">pxValue argument</span></span>

<span data-ttu-id="01331-p104">_pxValue_ には、値または配列のいずれかを指定できます。値の場合は、指定の範囲全体にその値が入力されます。配列 (**xltypeMulti**) の場合は、配列の要素が長方形の対応する場所に配置されます。</span><span class="sxs-lookup"><span data-stu-id="01331-p104">_pxValue_ can either be a value or an array. If it is a value, the entire destination range is filled with that value. If it is an array (**xltypeMulti**), the elements of the array are put into the corresponding locations in the rectangle.</span></span>
  
<span data-ttu-id="01331-p105">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle. If you use a vertical array, it is duplicated right to fill the entire rectangle. If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A** s.</span><span class="sxs-lookup"><span data-stu-id="01331-p105">If you use a horizontal array for the second argument, it is duplicated down to fill the entire rectangle. If you use a vertical array, it is duplicated right to fill the entire rectangle. If you use a rectangular array, and it is too small for the rectangular range you want to put it in, that range is padded with **#N/A** s.</span></span>
  
<span data-ttu-id="01331-123">対象範囲がソース配列よりも小さい場合は、対象範囲の境界まで値がコピーされ、余分なデータは無視されます。</span><span class="sxs-lookup"><span data-stu-id="01331-123">If the target range is smaller than the source array, the values are copied in up to the limits of the target range and the extra data are ignored.</span></span>
  
<span data-ttu-id="01331-p106">指定の長方形の要素を消去する場合は、ソース配列で **xltypeNil** 型の配列要素を使用します。指定の長方形全体を消去するには、2 番目の引数を省略します。</span><span class="sxs-lookup"><span data-stu-id="01331-p106">To clear an element of the destination rectangle, use an **xltypeNil** type array element in the source array. To clear the entire destination rectangle, omit the second argument.</span></span> 
  
### <a name="restrictions"></a><span data-ttu-id="01331-126">制限</span><span class="sxs-lookup"><span data-stu-id="01331-126">Restrictions</span></span>

<span data-ttu-id="01331-p107">**xlSet** を元に戻すことはできません。また、以前は使用可能だった、元に戻す操作に関する情報が破棄されます。</span><span class="sxs-lookup"><span data-stu-id="01331-p107">**xlSet** cannot be undone. In addition, it destroys any undo information that may have been available before.</span></span> 
  
<span data-ttu-id="01331-129">**xlSet** では、セルに定数のみを配置でき、数式は配置できません。</span><span class="sxs-lookup"><span data-stu-id="01331-129">**xlSet** can put only constants, not formulas, into cells.</span></span> 
  
<span data-ttu-id="01331-130">**xlSet** は、クラス 3 コマンドと同等の関数として動作します。つまり、DLL がオブジェクト、マクロ、メニュー、ツールバー、ショートカット キー、**[マクロ]** ダイアログ ボックスの **[実行]** ボタン (Excel 2007 以降ではリボンの **[表示]** タブ、以前のバージョンでは **[ツール]** メニューからアクセス可能) から呼び出された場合にのみ DLL で使用できます。</span><span class="sxs-lookup"><span data-stu-id="01331-130">**xlSet** behaves as a Class 3 command-equivalent function; that is, it is available only inside a DLL when the DLL is called from an object, macro, menu, toolbar, shortcut key, or the **Run** button in the **Macro** dialog box (accessed from **View** tab on the ribbon starting in Excel 2007, and the **Tools** menu in earlier versions).</span></span> 
  
## <a name="example"></a><span data-ttu-id="01331-131">例</span><span class="sxs-lookup"><span data-stu-id="01331-131">Example</span></span>

<span data-ttu-id="01331-p108">次の例では、マクロから渡された値が B205:B206 に入力されます。このコマンド関数の例には引数が必要であり、**Application.Run** メソッドを使用して、XLM マクロ シートや VBA モジュールから呼び出される場合にのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="01331-p108">The following example fills B205:B206 with the value that was passed in from a macro. This command function example requires an argument, and so will only work if called from an XLM macro sheet, or from a VBA module using the **Application.Run** method.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="01331-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="01331-134">See also</span></span>

- [<span data-ttu-id="01331-135">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="01331-135">xlCoerce</span></span>](xlcoerce.md)
- [<span data-ttu-id="01331-136">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="01331-136">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

