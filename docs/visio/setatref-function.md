---
title: SETATREF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: ユーザーインターフェイス (UI) またはオートメーションのアクションによって更新された値を別のセルにリダイレクトします。
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416805"
---
# <a name="setatref-function"></a><span data-ttu-id="76f40-103">SETATREF 関数</span><span class="sxs-lookup"><span data-stu-id="76f40-103">SETATREF Function</span></span>

<span data-ttu-id="76f40-104">ユーザーインターフェイス (UI) またはオートメーションのアクションによって更新された値を別のセルにリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="76f40-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="76f40-105">構文</span><span class="sxs-lookup"><span data-stu-id="76f40-105">Syntax</span></span>

<span data-ttu-id="76f40-106">SETATREF (\* \* *reference* \* \* [, \* \* *set_expression* \* \* [, \* \* *ignore_eval* \* \*])</span><span class="sxs-lookup"><span data-stu-id="76f40-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="76f40-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76f40-107">Parameters</span></span>

|<span data-ttu-id="76f40-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="76f40-108">**Name**</span></span>|<span data-ttu-id="76f40-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="76f40-109">**Required/Optional**</span></span>|<span data-ttu-id="76f40-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="76f40-110">**Data Type**</span></span>|<span data-ttu-id="76f40-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="76f40-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="76f40-112">_reference_</span><span class="sxs-lookup"><span data-stu-id="76f40-112">_reference_</span></span> <br/> |<span data-ttu-id="76f40-113">必須</span><span class="sxs-lookup"><span data-stu-id="76f40-113">Required</span></span>  <br/> |<span data-ttu-id="76f40-114">**String**</span><span class="sxs-lookup"><span data-stu-id="76f40-114">**String**</span></span> <br/> |<span data-ttu-id="76f40-115">更新された値をリダイレクトするセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="76f40-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="76f40-116">_set_expression_</span><span class="sxs-lookup"><span data-stu-id="76f40-116">_set_expression_</span></span> <br/> |<span data-ttu-id="76f40-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="76f40-117">Optional</span></span>  <br/> |<span data-ttu-id="76f40-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="76f40-118">**String**</span></span> <br/> |<span data-ttu-id="76f40-119">_参照_に割り当てられている式。</span><span class="sxs-lookup"><span data-stu-id="76f40-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="76f40-120">_ignore_eval_</span><span class="sxs-lookup"><span data-stu-id="76f40-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="76f40-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="76f40-121">Optional</span></span>  <br/> |<span data-ttu-id="76f40-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="76f40-122">**Boolean**</span></span> <br/> |<span data-ttu-id="76f40-123">TRUE の場合、SETATREF 関数は (0) ゼロに評価されます。FALSE (既定値) の場合、SETATREF 関数は_reference_の値に評価されます。</span><span class="sxs-lookup"><span data-stu-id="76f40-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76f40-124">注釈</span><span class="sxs-lookup"><span data-stu-id="76f40-124">Remarks</span></span>

<span data-ttu-id="76f40-125">図面ウィンドウでユーザー操作が行われたとき、またはオートメーションメソッドによって、SETATREF 数式を含むセルが更新されると、その値は SETATREF formula (_参照_) で参照されるセルにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="76f40-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="76f40-126">SETATREF 関数を含むセルの数式はそのままです。</span><span class="sxs-lookup"><span data-stu-id="76f40-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="76f40-127">_set_expression_が省略された場合、UI で設定された値またはオートメーションを使用して、参照先セルに設定されます。それ以外の場合は、 _set_expression_の内容が参照先セルに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="76f40-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="76f40-128">これにより、参照先セルに割り当てる前に、新しい値を変更または変換することができます。</span><span class="sxs-lookup"><span data-stu-id="76f40-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="76f40-129">SETATREF 関数には次の 2 つの関連する関数があります。</span><span class="sxs-lookup"><span data-stu-id="76f40-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="76f40-130">SETATREFEXPR 関数。 _set_expression_内の新しい値を表すために使用できます。</span><span class="sxs-lookup"><span data-stu-id="76f40-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="76f40-131">たとえば、 _set_expression_の SETATREFEXPR () のようになります。</span><span class="sxs-lookup"><span data-stu-id="76f40-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="76f40-132">SETATREFEXPR result から2インチを引くために使用できます。</span><span class="sxs-lookup"><span data-stu-id="76f40-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="76f40-133">SETATREFEVAL 関数を使用すると、 _set_expression_の一部を評価し、その結果に置き換える必要があることを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="76f40-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="76f40-134">SETATREF 関数は、図面ウィンドウのユーザー操作によって変更できるセルで使用するために設計されています。</span><span class="sxs-lookup"><span data-stu-id="76f40-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="76f40-135">次のセルがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="76f40-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="76f40-136">[Shape Transform] セクション - [Width]、[Height]、[Angle]、[PinX]、[PinY] の各セル</span><span class="sxs-lookup"><span data-stu-id="76f40-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="76f40-137">[Text Transform] セクション - [TxtWidth]、[TxtHeight]、[TxtAngle]、[TxtPinX]、[TxtPinY] の各セル</span><span class="sxs-lookup"><span data-stu-id="76f40-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="76f40-138">[1-D Endpoints] セクション - [BeginX]、[BeginY]、[EndX]、[EndY] の各セル</span><span class="sxs-lookup"><span data-stu-id="76f40-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="76f40-139">[Controls] セクション - [Controls.X]、[Controls.Y] の各セル</span><span class="sxs-lookup"><span data-stu-id="76f40-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="76f40-140">[Shape Data] セクション</span><span class="sxs-lookup"><span data-stu-id="76f40-140">Shape Data section</span></span>
    
<span data-ttu-id="76f40-141">SETATREF はセルの値が変更された場所を変更するため、イベントの発生に影響します。</span><span class="sxs-lookup"><span data-stu-id="76f40-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="76f40-142">セルに SETATREF が含まれている場合、 **FormulaChanged**および**CellChanged**イベントは、SETATREF を含むセルではなく、SETATREF によって参照されているセルに対して発生します。</span><span class="sxs-lookup"><span data-stu-id="76f40-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="76f40-143">SETATREF を含むセルに SETATREFEXPR も含まれている場合、function パラメーターが変更されているため、SETATREF を含むセルに対しても**FormulaChanged**イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="76f40-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="76f40-144">SETATREF 関数についてのその他の重要な点は、以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="76f40-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="76f40-145">SETATREF 関数は、他の SETATREF 関数に対し、最大 10 の参照を連鎖させることができます。</span><span class="sxs-lookup"><span data-stu-id="76f40-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="76f40-146">セルには、SETATREF 関数以外の式を含めることができます。1 つのセルに SETATREF を複数使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="76f40-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="76f40-147">図形を接着している場合、Visio は同じシート内で連鎖している SETATREF 参照に従って、参照先のセルに接着する数式を配置します。</span><span class="sxs-lookup"><span data-stu-id="76f40-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="76f40-148">オートメーションは SETATREF 関数を認識して、参照先のセルの連鎖に従います。</span><span class="sxs-lookup"><span data-stu-id="76f40-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="76f40-149">GUARD 同様、SETATREF はシェイプシートの SETF 関数による変更からセルを保護しません。</span><span class="sxs-lookup"><span data-stu-id="76f40-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="76f40-150">例1</span><span class="sxs-lookup"><span data-stu-id="76f40-150">Example1</span></span>

<span data-ttu-id="76f40-151">図形に [Width] というカスタム プロパティがあり、[Shape Transform] セクションの [Width] セルに次の数式が含まれているとします。</span><span class="sxs-lookup"><span data-stu-id="76f40-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="76f40-152">= SETATREF (Prop)</span><span class="sxs-lookup"><span data-stu-id="76f40-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="76f40-153">ユーザーが UI で図形の幅を変更した場合は、新しい値が [図形の変換] セクションの [width] セルではなく、[... width] セルに割り当てられます。[幅] セルの数式は変更されません。</span><span class="sxs-lookup"><span data-stu-id="76f40-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="76f40-154">図形データを使用して、図形の幅を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="76f40-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="76f40-155">例2</span><span class="sxs-lookup"><span data-stu-id="76f40-155">Example2</span></span>

<span data-ttu-id="76f40-p107">Visio ソリューションには階層関係を持つ図形が多く、親図形が移動する際には子図形も移動する必要があります。シェイプシートの SETATREF 関数を使用してこの関係を管理する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="76f40-p107">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved. Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="76f40-p108">次の数式は子図形の [Shape Transform] セクションに含まれます。また、親図形からのオフセット寸法を追跡する [User.DeltaX] および [User.DeltaY] というユーザー セルを定義します。これにより、親図形が移動する際に子図形も移動することができます。また、子図形が移動する場合にも階層関係を保持することができます。</span><span class="sxs-lookup"><span data-stu-id="76f40-p108">The following formulas are contained in the Shape Transform section of the child shape. Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape. This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="76f40-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span><span class="sxs-lookup"><span data-stu-id="76f40-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="76f40-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span><span class="sxs-lookup"><span data-stu-id="76f40-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="76f40-163">UI を使用して子図形を移動すると、新しい PinX および PinY の値が SETATREFEXPR 関数のパラメーターとして設定されます。</span><span class="sxs-lookup"><span data-stu-id="76f40-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="76f40-164">SETATREF 関数は、SETATREFEVAL に含まれている数式を評価し、PinX と PinY をその結果に置き換え、結果として得られた数式を、SETATREF 関数で参照されるユーザーセル (deltax および) に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="76f40-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="76f40-165">最後に、SETATREF (deltay) によって返された値が、子図形の pin 位置を計算するために、parentshape のピン位置に追加されます。</span><span class="sxs-lookup"><span data-stu-id="76f40-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

