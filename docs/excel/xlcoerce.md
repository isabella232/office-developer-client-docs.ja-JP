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
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798976"
---
# <a name="xlcoerce"></a><span data-ttu-id="68d09-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="68d09-104">xlCoerce</span></span>

 <span data-ttu-id="68d09-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="68d09-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="68d09-106">**XLOPER**/ **XLOPER12** の型を別の型に変換するか、シートのセルの値を検索します。</span><span class="sxs-lookup"><span data-stu-id="68d09-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="68d09-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68d09-107">Parameters</span></span>

 <span data-ttu-id="68d09-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="68d09-108">_pxSource_</span></span>
  
<span data-ttu-id="68d09-109">変換対象のソース **XLOPER**/ **XLOPER12**。</span><span class="sxs-lookup"><span data-stu-id="68d09-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="68d09-110">_pxDestType_ (**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="68d09-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="68d09-111">(省略可能)。</span><span class="sxs-lookup"><span data-stu-id="68d09-111">Optional.</span></span> <span data-ttu-id="68d09-112">受け入れ可能な変換後の型のビット マスク。</span><span class="sxs-lookup"><span data-stu-id="68d09-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="68d09-113">ビット単位の **OR** 演算子 ( | ) を使用して、複数の使用可能な型を指定します。</span><span class="sxs-lookup"><span data-stu-id="68d09-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="68d09-114">この引数を省略すると、単一セルへの参照が **xltypeStr**、**xltypeNum**、**xltypeBool**、**xltypeErr**、**xltypeNil** (参照先セルが空の場合) の値型のいずれかに変換され、セルのブロックへの参照は **xltypeMulti** に変換されます。</span><span class="sxs-lookup"><span data-stu-id="68d09-114">(Optional). A bit-mask of the resulting types you are willing to accept. You should use the bitwise OR operator ( | ) to specify multiple possible types. If this argument is omitted, references to single cells are converted to one of the value types xltypeStr, xltypeNum, xltypeBool, xltypeErr, xltypeNil (if the referred-to cell is empty), and references to blocks of cells are converted to xltypeMulti. This makes xlCoerce the most convenient way to look up cell values.</span></span> <span data-ttu-id="68d09-115">これにより **xlCoerce** はセル値を検索する最も便利な方法になります。</span><span class="sxs-lookup"><span data-stu-id="68d09-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="68d09-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="68d09-116">Property Value/Return Value</span></span>

<span data-ttu-id="68d09-117">強制変換された値 (**xltypeStr**、**xltypeNum**、**xltypeBool**、**xltypeErr**、**xltypeNil**、または **xltypeMulti**) を返します。</span><span class="sxs-lookup"><span data-stu-id="68d09-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="68d09-118">注釈</span><span class="sxs-lookup"><span data-stu-id="68d09-118">Remarks</span></span>

 <span data-ttu-id="68d09-p102">**xlCoerce** は **xltypeBigData** または **xltypeFlow** に変換できず、その逆の変換もできません。**xltypeMissing** または **xltypeNil** の型を _pxDestType_ として渡すことは、引数を省略することに相当します。たとえば、文字列には数字に変換でないものがあります。</span><span class="sxs-lookup"><span data-stu-id="68d09-p102">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**. Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument. Conversion can fail in some cases. For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="68d09-123">配列または複数セルの参照を単一値の型に変換すると、結果は一番上の左のセルまたは配列の要素の値になります。</span><span class="sxs-lookup"><span data-stu-id="68d09-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="68d09-124">例</span><span class="sxs-lookup"><span data-stu-id="68d09-124">Example</span></span>

<span data-ttu-id="68d09-125">次のコードは、`\SAMPLES\EXAMPLE\EXAMPLE.C` にあります。</span><span class="sxs-lookup"><span data-stu-id="68d09-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="68d09-p103">ここに示される強制手順が削除され、**xInt** が直接 **xlcAlert** に渡されるように、**XlcAlert** 関数は暗黙的に引数を文字列に変換しようとします。**xlcAlert** はコマンドのマクロであるため、このコードはマクロ シートから呼び出されたときのみ正しく作動します。</span><span class="sxs-lookup"><span data-stu-id="68d09-p103">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**. As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="68d09-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="68d09-128">See also</span></span>



[<span data-ttu-id="68d09-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="68d09-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="68d09-130">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="68d09-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

