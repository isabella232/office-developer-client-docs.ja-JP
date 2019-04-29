---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- xlcoerce function [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424834"
---
# <a name="xlcoerce"></a><span data-ttu-id="97578-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="97578-104">xlCoerce</span></span>

 <span data-ttu-id="97578-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="97578-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="97578-106">**XLOPER**/ **XLOPER12** の型を別の型に変換するか、シートのセルの値を検索します。</span><span class="sxs-lookup"><span data-stu-id="97578-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="97578-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97578-107">Parameters</span></span>

 <span data-ttu-id="97578-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="97578-108">_pxSource_</span></span>
  
<span data-ttu-id="97578-109">変換対象のソース **XLOPER**/ **XLOPER12**。</span><span class="sxs-lookup"><span data-stu-id="97578-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="97578-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="97578-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="97578-p101">(Optional). A bit-mask of the resulting types you are willing to accept. You should use the bitwise **OR** operator ( | ) to specify multiple possible types. If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**. This makes **xlCoerce** the most convenient way to look up cell values.</span><span class="sxs-lookup"><span data-stu-id="97578-p101">(Optional). A bit-mask of the resulting types you are willing to accept. You should use the bitwise **OR** operator ( | ) to specify multiple possible types. If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**. This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="97578-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="97578-116">Property value/Return value</span></span>

<span data-ttu-id="97578-117">強制変換された値 (**xltypeStr**、**xltypeNum**、**xltypeBool**、**xltypeErr**、**xltypeNil**、または **xltypeMulti**) を返します。</span><span class="sxs-lookup"><span data-stu-id="97578-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97578-118">注釈</span><span class="sxs-lookup"><span data-stu-id="97578-118">Remarks</span></span>

 <span data-ttu-id="97578-p102">**xlCoerce** は **xltypeBigData** または **xltypeFlow** に変換できず、その逆の変換もできません。**xltypeMissing** または **xltypeNil** の型を _pxDestType_ として渡すことは、引数を省略することに相当します。たとえば、文字列には数字に変換でないものがあります。</span><span class="sxs-lookup"><span data-stu-id="97578-p102">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**. Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument. Conversion can fail in some cases. For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="97578-123">配列または複数セルの参照を単一値の型に変換すると、結果は一番上の左のセルまたは配列の要素の値になります。</span><span class="sxs-lookup"><span data-stu-id="97578-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="97578-124">例</span><span class="sxs-lookup"><span data-stu-id="97578-124">Example</span></span>

<span data-ttu-id="97578-125">次のコードは、`\SAMPLES\EXAMPLE\EXAMPLE.C` にあります。</span><span class="sxs-lookup"><span data-stu-id="97578-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="97578-p103">ここに示される強制手順が削除され、**xInt** が直接 **xlcAlert** に渡されるように、**XlcAlert** 関数は暗黙的に引数を文字列に変換しようとします。**xlcAlert** はコマンドのマクロであるため、このコードはマクロ シートから呼び出されたときのみ正しく作動します。</span><span class="sxs-lookup"><span data-stu-id="97578-p103">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**. As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="97578-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="97578-128">See also</span></span>



[<span data-ttu-id="97578-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="97578-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="97578-130">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="97578-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

