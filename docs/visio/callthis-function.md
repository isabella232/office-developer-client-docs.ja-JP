---
title: CALLTHIS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Microsoft Visual Basic for Applications (VBA) プロジェクトでプロシージャを呼び出します。
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413816"
---
# <a name="callthis-function"></a><span data-ttu-id="f3c3c-103">CALLTHIS 関数</span><span class="sxs-lookup"><span data-stu-id="f3c3c-103">CALLTHIS Function</span></span>

<span data-ttu-id="f3c3c-104">Microsoft Visual Basic for Applications (VBA) プロジェクトでプロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f3c3c-105">構文</span><span class="sxs-lookup"><span data-stu-id="f3c3c-105">Syntax</span></span>

<span data-ttu-id="f3c3c-106">CALLTHIS(" \*\* *procedure* \*\* ",[" \*\* *project* \*\* "],[ \*\* *arg1* \*\*, \*\* *arg2* \*\*,...])</span><span class="sxs-lookup"><span data-stu-id="f3c3c-106">CALLTHIS(" \*\* *procedure* \*\* ",[" \*\* *project* \*\* "],[ \*\* *arg1* \*\*, \*\* *arg2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f3c3c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f3c3c-107">Parameters</span></span>

|<span data-ttu-id="f3c3c-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="f3c3c-108">**Name**</span></span>|<span data-ttu-id="f3c3c-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f3c3c-109">**Required/Optional**</span></span>|<span data-ttu-id="f3c3c-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f3c3c-110">**Data Type**</span></span>|<span data-ttu-id="f3c3c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="f3c3c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f3c3c-112">_procedure_</span><span class="sxs-lookup"><span data-stu-id="f3c3c-112">_procedure_</span></span> <br/> |<span data-ttu-id="f3c3c-113">必須</span><span class="sxs-lookup"><span data-stu-id="f3c3c-113">Required</span></span>  <br/> |<span data-ttu-id="f3c3c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f3c3c-114">**String**</span></span> <br/> | <span data-ttu-id="f3c3c-115">呼び出すプロシージャの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="f3c3c-116">_project_</span><span class="sxs-lookup"><span data-stu-id="f3c3c-116">_project_</span></span> <br/> |<span data-ttu-id="f3c3c-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="f3c3c-117">Optional</span></span>  <br/> |<span data-ttu-id="f3c3c-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="f3c3c-118">**String**</span></span> <br/> |<span data-ttu-id="f3c3c-119">プロシージャが含まれるプロジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="f3c3c-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="f3c3c-120">_arg_</span></span> <br/> |<span data-ttu-id="f3c3c-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="f3c3c-121">Optional</span></span>  <br/> |<span data-ttu-id="f3c3c-122">**数値型 (Number)、文字列型 (String)、日付型 (Date)、または通貨型 (Currency)**</span><span class="sxs-lookup"><span data-stu-id="f3c3c-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="f3c3c-123">パラメーターとしてプロシージャに渡されます。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f3c3c-124">注釈</span><span class="sxs-lookup"><span data-stu-id="f3c3c-124">Remarks</span></span>

<span data-ttu-id="f3c3c-125">VBA プロジェクトでは、  *プロシージャは次*  のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="f3c3c-126">procedure(*vsoShape* As Visio。Shape [arg1 As type, arg2 As type...])</span><span class="sxs-lookup"><span data-stu-id="f3c3c-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="f3c3c-127">*ここで、vsoShape* は、評価される **CALLTHIS** 数式と _arg1 、arg2_..を含む Shape オブジェクトへの参照です。は、その数式で指定された引数です。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="f3c3c-128">*vsoShape は*、C++ メンバー プロシージャに渡される "this" 引数と非常に似たものに注意してください。したがって、名前 "CALLTHIS."</span><span class="sxs-lookup"><span data-stu-id="f3c3c-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="f3c3c-129">実際には、CALLTHIS を含む数式を含むセルは、「このプロシージャを呼び出して、自分の図形への参照を渡す」と読み取ります。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="f3c3c-130">project _が_ 指定されている場合、Microsoft Visio開いているすべてのドキュメントがスキャンされ、そのプロジェクトに含まれるプロジェクトの _プロシージャが呼_ び出されます。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="f3c3c-131">project _が_ 省略されている場合、または null ("") の場合、Visio は、評価される CALLTHIS 数式を含むドキュメントの VBA プロジェクトにあると仮定します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="f3c3c-132">_arg1 、_ _arg2..._ の数値は、外部単位で渡されます。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="f3c3c-133">たとえば、高さが 3 cm の図形から [Height] セルの値を渡すと、3 が渡されます。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="f3c3c-134">数値を別の単位に変換して渡すには、FORMATEX 関数を使用するか、NULL 値と単位の組み合わせを追加して明示的に単位を適用します (0 ft + Height など)。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="f3c3c-135">CALLTHIS 関数の 2 番目のカンマはオプションです。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="f3c3c-136">これは、プロシージャに追加するパラメーターの数に応じて指定します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="f3c3c-137">2 番目のコンマを追加しない以外のパラメーターを使用しない場合は  `(vsoShape as Visio.Shape)` 、CALLTHIS("",) を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="f3c3c-138">たとえばパラメーターを 2 つ追加する場合は、CALLTHIS("",,,) のように記述します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="f3c3c-139">CALLTHIS 関数は常に 0 に評価され、プロシージャの呼び出しは再計算プロセスが終了した後、アイドル時間中に行われます。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="f3c3c-140">_プロシージャ_ は値を返しますが、Visio無視します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="f3c3c-141">_プロシージャ_ は、Visio が文書内の別のセルの数式または結果を設定することで認識できる値を返しますが、CALLTHIS数式を上書きしない限り、プロシージャを呼び出したセルは返されません。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="f3c3c-142">CALLTHIS 関数では、図面のプロジェクトが別のプロジェクトを参照していなくても、そのプロジェクトを呼び出すことができます。この点が、RUNADDON 関数とは異なる点です。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="f3c3c-143">Visio インスタンスが数式の CALLTHIS 関数を評価する場合、その結果呼び出された VBA コードでは、この数式を使用しているセルを含んだ図面を閉じないでください。アプリケーション エラーが発生して Visio が終了します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="f3c3c-144">CALLTHIS 関数を使用するセルを含んだ図面を閉じる必要がある場合、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="f3c3c-145">VBA 以外のコードを使用して図面を閉じます。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="f3c3c-146">閉じる図面以外のプロジェクトから図面を閉じます。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="f3c3c-147">図面を閉じる代わりに、ウィンドウを閉じるためのウィンドウ メッセージを図面に通知します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="f3c3c-148">Visio のコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定およびコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f3c3c-149">例 1</span><span class="sxs-lookup"><span data-stu-id="f3c3c-149">Example 1</span></span>

<span data-ttu-id="f3c3c-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span><span class="sxs-lookup"><span data-stu-id="f3c3c-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="f3c3c-151">モジュール内の p という名前のプロシージャを呼び出し、Height の値をセンチメートル単位 (7.62 cm など) で渡します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f3c3c-152">例 2</span><span class="sxs-lookup"><span data-stu-id="f3c3c-152">Example 2</span></span>

<span data-ttu-id="f3c3c-153">CALLTHIS("q",,0 cm+Height,Width)</span><span class="sxs-lookup"><span data-stu-id="f3c3c-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="f3c3c-154">モジュール内の q という名前のプロシージャを呼び出し、セルの高さをセンチメートル単位で、幅を内部単位で渡します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f3c3c-155">例 3</span><span class="sxs-lookup"><span data-stu-id="f3c3c-155">Example 3</span></span>

<span data-ttu-id="f3c3c-156">ThisDocument クラス モジュールの  *次の手順を*  使用します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="f3c3c-157">図形の [EventDblClick] セルでは、上記のプロシージャと共に次のいずれかの構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3c3c-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="f3c3c-158">CALLTHIS("ThisDocument.A",)</span><span class="sxs-lookup"><span data-stu-id="f3c3c-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="f3c3c-159">CALLTHIS("ThisDocument.B","Click")</span><span class="sxs-lookup"><span data-stu-id="f3c3c-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="f3c3c-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span><span class="sxs-lookup"><span data-stu-id="f3c3c-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

