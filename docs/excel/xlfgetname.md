---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303886"
---
# <a name="xlfgetname"></a><span data-ttu-id="63734-104">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="63734-104">xlfGetName</span></span>

<span data-ttu-id="63734-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="63734-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="63734-p101">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references. Use **xlfGetName** to check the value defined by a name. To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span><span class="sxs-lookup"><span data-stu-id="63734-p101">Returns the definition of a name as it appears in the **Refers to** column of the **Name Manager** dialog box, which is displayed when you click **Name Manager** in the **Defined Names** section on the **Formulas** tab. If the definition contains references, they are given as R1C1-style references. Use **xlfGetName** to check the value defined by a name. To get the name that corresponds to a definition, use [xlfGetDef](xlfgetdef.md).</span></span>
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a><span data-ttu-id="63734-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63734-109">Parameters</span></span>

<span data-ttu-id="63734-110">_pxNameText_ (**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="63734-110">_pxNameText_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="63734-p102">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.  _pxNameText_ can also be a hidden name.</span><span class="sxs-lookup"><span data-stu-id="63734-p102">Can be a name defined on the sheet; an external reference to a name defined on the active workbook, for example,  `"!Sales"`; or an external reference to a name defined on a particular open workbook, for example,  `"[Book1]SHEET1!Sales"`.  _pxNameText_ can also be a hidden name.</span></span> 
  
<span data-ttu-id="63734-113">_pxInfoType_ (**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="63734-113">_pxInfoType_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="63734-p103">名前について返される情報の種類を指定します。**FALSE** または省略すると、定義が返されます。**TRUE** の場合、名前がシートに対してのみ定義されていると **TRUE** を返し、名前がブック全体に対して定義されていると **FALSE** を返します。</span><span class="sxs-lookup"><span data-stu-id="63734-p103">Specifies the type of information to return about the name. If **FALSE** or omitted, the definition is returned. If **TRUE**, returns **TRUE** if the name is defined for just the sheet, **FALSE** if the name is defined for the entire workbook.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="63734-117">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="63734-117">Property value/Return value</span></span>

<span data-ttu-id="63734-118">_pxRes_ (**xltypeStr**、**xltypeBool**、または **xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="63734-118">_pxRes_ (**xltypeStr**, **xltypeBool**, or **xltypeErr**)</span></span>
  
<span data-ttu-id="63734-119">_pxInfoType_ に渡された値に応じて、指定した名前の定義 (**xltypeStr**)、あるいは **TRUE** または **FALSE** (**xltypeBool**) が返されます。</span><span class="sxs-lookup"><span data-stu-id="63734-119">Depending on the value passed for  _pxInfoType_, returns the definition of the specified name (**xltypeStr**), or **TRUE** or **FALSE** (**xltypeBool**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63734-120">注釈</span><span class="sxs-lookup"><span data-stu-id="63734-120">Remarks</span></span>

<span data-ttu-id="63734-p104">**[シートの保護]** ダイアログ ボックスで **[シートとロックされたセルの内容を保護する]** チェック ボックスを選択して対象の名前が含まれるブックを保護した場合、**xlfGetName** は `#N/A` エラー値を返します。**[シートの保護]** ダイアログ ボックスを表示するには、**[校閲]** タブの **[変更]** セクションにある **[シートの保護]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="63734-p104">If the **Protect worksheet and contents of locked cells** check box has been selected in the **Protect Sheet** dialog box to protect the workbook containing the name, **xlfGetName** returns the  `#N/A` error value. To see the **Protect Sheet** dialog box, click **Protect Sheet** in the **Changes** section of the **Review** tab.</span></span> 
  
<span data-ttu-id="63734-123">次の表に、特定の _pxNameText_ 引数を指定して.**xlfGetDef** を呼び出した場合に返される値の例を 3 つ示します。</span><span class="sxs-lookup"><span data-stu-id="63734-123">The following table lists three examples of the values returned by a call to **xlfGetDef** with the specified  _pxNameText_ argument.</span></span> 
  
|<span data-ttu-id="63734-124">**Excel における定義**</span><span class="sxs-lookup"><span data-stu-id="63734-124">**Definition in Excel**</span></span>|<span data-ttu-id="63734-125">**_pxNameText_**</span><span class="sxs-lookup"><span data-stu-id="63734-125">**_pxNameText_**</span></span>|<span data-ttu-id="63734-126">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="63734-126">**Value Returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="63734-127">シートで名前 [Sales] が数値 523 として定義されています。</span><span class="sxs-lookup"><span data-stu-id="63734-127">The name Sales on a sheet is defined as the number 523.</span></span>  <br/> |<span data-ttu-id="63734-128">"Sales"</span><span class="sxs-lookup"><span data-stu-id="63734-128">"Sales"</span></span>  <br/> |<span data-ttu-id="63734-129">"=523"</span><span class="sxs-lookup"><span data-stu-id="63734-129">"=523"</span></span>  <br/> |
|<span data-ttu-id="63734-130">アクティブなシートで名前 [Profit] が、数式 =Sales-Costs として定義されています。</span><span class="sxs-lookup"><span data-stu-id="63734-130">The name Profit on the active sheet is defined as the formula =Sales-Costs.</span></span>  <br/> |<span data-ttu-id="63734-131">"!Profit"</span><span class="sxs-lookup"><span data-stu-id="63734-131">"!Profit"</span></span>  <br/> |<span data-ttu-id="63734-132">"=Sales-Costs"</span><span class="sxs-lookup"><span data-stu-id="63734-132">"=Sales-Costs"</span></span>  <br/> |
|<span data-ttu-id="63734-133">アクティブ シートで名前 [Database] が、範囲 A1:F500 として定義されています。</span><span class="sxs-lookup"><span data-stu-id="63734-133">The name Database on the active sheet is defined as the range A1:F500.</span></span>  <br/> |<span data-ttu-id="63734-134">"!Database"</span><span class="sxs-lookup"><span data-stu-id="63734-134">"!Database"</span></span>  <br/> |<span data-ttu-id="63734-135">"=R1C1:R500C6"</span><span class="sxs-lookup"><span data-stu-id="63734-135">"=R1C1:R500C6"</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63734-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="63734-136">See also</span></span>

- [<span data-ttu-id="63734-137">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="63734-137">xlfGetDef</span></span>](xlfgetdef.md)
- [<span data-ttu-id="63734-138">重要で役に立つ C API XLM 関数</span><span class="sxs-lookup"><span data-stu-id="63734-138">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)

