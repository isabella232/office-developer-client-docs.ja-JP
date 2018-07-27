---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798992"
---
# <a name="xlfgetdef"></a><span data-ttu-id="70a0c-104">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="70a0c-104">xlfGetDef</span></span>

<span data-ttu-id="70a0c-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="70a0c-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="70a0c-106">ブックの特定の領域、値、数式に定義されている名前をテキストとして返します。</span><span class="sxs-lookup"><span data-stu-id="70a0c-106">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook.</span></span> <span data-ttu-id="70a0c-107">Excel では、この値は、**[名前の管理]** ダイアログ ボックスの **[名前]** 列に表示されます。このダイアログ ボックスは、**[数式]** タブの **[定義された名前]** セクションで **[名前の管理]** をクリックすると表示されます。**xlfGetDef** を使用して、定義に対応する名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="70a0c-107">Returns the name, as text, that is defined for a particular area, value, or formula in a workbook. In Excel, this value is displayed in the **Name** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. Use **xlfGetDef** to get the name that corresponds to a definition. To get the definition of a name, use xlfGetName.</span></span> <span data-ttu-id="70a0c-108">名前の定義を取得するには、[xlfGetName](xlfgetname.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="70a0c-108">To get the definition of a name, use [xlfGetName](xlfgetname.md).</span></span>
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a><span data-ttu-id="70a0c-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="70a0c-109">Parameters</span></span>

<span data-ttu-id="70a0c-110">_pxDefText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="70a0c-110">_pxDefText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="70a0c-111">参照、値、オブジェクト、数式など、参照先の名前として定義できるあらゆるものを指定できます。</span><span class="sxs-lookup"><span data-stu-id="70a0c-111">Can be anything you can define a name to refer to, including a reference, a value, an object, or a formula.</span></span>
  
<span data-ttu-id="70a0c-p102">参照の場合は、`"R3C5"` などの R1C1 スタイルで指定する必要があります。_pxDefText_ が値または数式の場合、**[名前の管理]** ダイアログ ボックスの **[参照範囲]** 列に表示される等号 (=) を含める必要はありません。_pxDefText_ に複数の名前が存在する場合、**xlfGetDef** は最初の名前を返します。_pxDefText_ に一致する名前がない場合、**xlfGetDef** はエラー値 `#NAME?` を返します。</span><span class="sxs-lookup"><span data-stu-id="70a0c-p102">References must be given in R1C1 style, such as  `"R3C5"`. If  _pxDefText_ is a value or formula, it is not necessary to include the equal sign that is displayed in the **Refers To** column in the **Name Manager** dialog box. If there is more than one name for  _pxDefText_, **xlfGetDef** returns the first name. If no name matches  _pxDefText_, **xlfGetDef** returns the  `#NAME?` error value.</span></span> 
  
<span data-ttu-id="70a0c-116">_pxDocumentText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="70a0c-116">_pxDocumentText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="70a0c-p103">_pxDefText_ が存在するシートを指定します。_pxDocumentText_ が省略されると、アクティブなシートとして想定されます。</span><span class="sxs-lookup"><span data-stu-id="70a0c-p103">Specifies the sheet that  _pxDefText_ is on. If  _pxDocumentText_ is omitted, it is assumed to be the active sheet.</span></span> 
  
<span data-ttu-id="70a0c-119">_pxTypeNum_ (**xltypeNum**)</span><span class="sxs-lookup"><span data-stu-id="70a0c-119">_pxTypeNum_ (**xltypeNum**)</span></span>
  
<span data-ttu-id="70a0c-120">返す名前の種類を指定する、1 から 3 の範囲の数値です。</span><span class="sxs-lookup"><span data-stu-id="70a0c-120">A number from 1 to 3 specifying which types of names are returned.</span></span>
  
|<span data-ttu-id="70a0c-121">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="70a0c-121">**_pxTypeNum_**</span></span>|<span data-ttu-id="70a0c-122">**返される値**</span><span class="sxs-lookup"><span data-stu-id="70a0c-122">**Returns**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70a0c-123">1 または省略</span><span class="sxs-lookup"><span data-stu-id="70a0c-123">1 or omitted</span></span>  <br/> |<span data-ttu-id="70a0c-124">標準名のみ。</span><span class="sxs-lookup"><span data-stu-id="70a0c-124">Normal names only.</span></span>  <br/> |
|<span data-ttu-id="70a0c-125">2</span><span class="sxs-lookup"><span data-stu-id="70a0c-125">-2</span></span>  <br/> |<span data-ttu-id="70a0c-126">非表示名のみ。</span><span class="sxs-lookup"><span data-stu-id="70a0c-126">Hidden names only.</span></span>  <br/> |
|<span data-ttu-id="70a0c-127">3</span><span class="sxs-lookup"><span data-stu-id="70a0c-127">"3"</span></span>  <br/> |<span data-ttu-id="70a0c-128">すべての名前。</span><span class="sxs-lookup"><span data-stu-id="70a0c-128">All names.</span></span>  <br/> |
   
## <a name="property-valuereturn-value"></a><span data-ttu-id="70a0c-129">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="70a0c-129">Property Value/Return Value</span></span>

 <span data-ttu-id="70a0c-130">_pxRes_ (**xltypeStr** または **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="70a0c-130">_pxRes_ (**xltypeStr** or **xltypeErr**)</span></span>
  
<span data-ttu-id="70a0c-131">指定の定義に関連付けられている名前を返します。</span><span class="sxs-lookup"><span data-stu-id="70a0c-131">Returns the name associated with the specified definition.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70a0c-132">注釈</span><span class="sxs-lookup"><span data-stu-id="70a0c-132">Remarks</span></span>

<span data-ttu-id="70a0c-133">次の表に、特定の引数を指定して **xlfGetDef** を呼び出した場合に返される値の例を 4 つ示します。</span><span class="sxs-lookup"><span data-stu-id="70a0c-133">The following table lists four examples of the values returned by a call to **xlfGetDef** with the specified arguments.</span></span> 
  
|<span data-ttu-id="70a0c-134">**Excel で定義された名前**</span><span class="sxs-lookup"><span data-stu-id="70a0c-134">**Name defined in Excel**</span></span>|<span data-ttu-id="70a0c-135">**_pxDefText_**</span><span class="sxs-lookup"><span data-stu-id="70a0c-135">**_pxDefText_**</span></span>|<span data-ttu-id="70a0c-136">**_pxDocumentText_**</span><span class="sxs-lookup"><span data-stu-id="70a0c-136">**_pxDocumentText_**</span></span>|<span data-ttu-id="70a0c-137">**_pxTypeNum_**</span><span class="sxs-lookup"><span data-stu-id="70a0c-137">**_pxTypeNum_**</span></span>|<span data-ttu-id="70a0c-138">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="70a0c-138">**Value Returned**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="70a0c-139">Sheet4 の指定の範囲には「Sales」という名前が付いています。</span><span class="sxs-lookup"><span data-stu-id="70a0c-139">The specified range in Sheet4 is named Sales.</span></span>  <br/> |<span data-ttu-id="70a0c-140">"R2C2:R9C6"</span><span class="sxs-lookup"><span data-stu-id="70a0c-140">"R2C2:R9C6"</span></span>  <br/> |<span data-ttu-id="70a0c-141">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="70a0c-141">"Sheet4"</span></span>  <br/> |<span data-ttu-id="70a0c-142">\<省略\></span><span class="sxs-lookup"><span data-stu-id="70a0c-142">\<omitted\></span></span>  <br/> |<span data-ttu-id="70a0c-143">"Sales"</span><span class="sxs-lookup"><span data-stu-id="70a0c-143">"Sales"</span></span>  <br/> |
|<span data-ttu-id="70a0c-144">Sheet4 の値 100 は、「Constant」として定義されています。</span><span class="sxs-lookup"><span data-stu-id="70a0c-144">The value 100 in Sheet4 is defined as Constant.</span></span>  <br/> |<span data-ttu-id="70a0c-145">"100"</span><span class="sxs-lookup"><span data-stu-id="70a0c-145">"100"</span></span>  <br/> |<span data-ttu-id="70a0c-146">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="70a0c-146">"Sheet4"</span></span>  <br/> |<span data-ttu-id="70a0c-147">\<省略\></span><span class="sxs-lookup"><span data-stu-id="70a0c-147">\<omitted\></span></span>  <br/> |<span data-ttu-id="70a0c-148">"Constant"</span><span class="sxs-lookup"><span data-stu-id="70a0c-148">"Constant"</span></span>  <br/> |
|<span data-ttu-id="70a0c-149">Sheet4 の指定の数式には「SumTotal」という名前が付いています。</span><span class="sxs-lookup"><span data-stu-id="70a0c-149">The specified formula in Sheet4 is named SumTotal.</span></span>  <br/> |<span data-ttu-id="70a0c-150">"SUM(R1C1:R10C1)"</span><span class="sxs-lookup"><span data-stu-id="70a0c-150">"SUM(R1C1:R10C1)"</span></span>  <br/> |<span data-ttu-id="70a0c-151">"Sheet4"</span><span class="sxs-lookup"><span data-stu-id="70a0c-151">"Sheet4"</span></span>  <br/> |<span data-ttu-id="70a0c-152">\<省略\></span><span class="sxs-lookup"><span data-stu-id="70a0c-152">\<omitted\></span></span>  <br/> |<span data-ttu-id="70a0c-153">"SumTotal"</span><span class="sxs-lookup"><span data-stu-id="70a0c-153">"SumTotal"</span></span>  <br/> |
|<span data-ttu-id="70a0c-154">アクティブなシートの非表示名「Counter」として 3 が定義されています。</span><span class="sxs-lookup"><span data-stu-id="70a0c-154">3 is defined as the hidden name Counter on the active sheet.</span></span>  <br/> |<span data-ttu-id="70a0c-155">"3"</span><span class="sxs-lookup"><span data-stu-id="70a0c-155">"3"</span></span>  <br/> |<span data-ttu-id="70a0c-156">\<省略\></span><span class="sxs-lookup"><span data-stu-id="70a0c-156">\<omitted\></span></span>  <br/> |<span data-ttu-id="70a0c-157">2</span><span class="sxs-lookup"><span data-stu-id="70a0c-157">-2</span></span>  <br/> |<span data-ttu-id="70a0c-158">"Counter"</span><span class="sxs-lookup"><span data-stu-id="70a0c-158">"Counter"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70a0c-159">関連項目</span><span class="sxs-lookup"><span data-stu-id="70a0c-159">See also</span></span>

- [<span data-ttu-id="70a0c-160">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="70a0c-160">xlfgetname</span></span>](xlfgetname.md)
- [<span data-ttu-id="70a0c-161">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="70a0c-161">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

