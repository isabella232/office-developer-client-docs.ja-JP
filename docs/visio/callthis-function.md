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
description: (VBA) プロジェクトを Microsoft Visual Basic for Applications プロシージャを呼び出します。
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804940"
---
# <a name="callthis-function"></a><span data-ttu-id="6edb2-103">CALLTHIS 関数</span><span class="sxs-lookup"><span data-stu-id="6edb2-103">CALLTHIS Function</span></span>

<span data-ttu-id="6edb2-104">(VBA) プロジェクトを Microsoft Visual Basic for Applications プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6edb2-105">構文</span><span class="sxs-lookup"><span data-stu-id="6edb2-105">Syntax</span></span>

<span data-ttu-id="6edb2-106">CALLTHIS ("* **手順** *」、["* **プロジェクト** *」]、[* * *arg1* * *、* **引数 2* * *,...])</span><span class="sxs-lookup"><span data-stu-id="6edb2-106">CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6edb2-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="6edb2-107">Parameters</span></span>

|<span data-ttu-id="6edb2-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6edb2-108">**Name**</span></span>|<span data-ttu-id="6edb2-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6edb2-109">**Required/Optional**</span></span>|<span data-ttu-id="6edb2-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6edb2-110">**Data Type**</span></span>|<span data-ttu-id="6edb2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6edb2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6edb2-112">_手順_</span><span class="sxs-lookup"><span data-stu-id="6edb2-112">_procedure_</span></span> <br/> |<span data-ttu-id="6edb2-113">必須</span><span class="sxs-lookup"><span data-stu-id="6edb2-113">Required</span></span>  <br/> |<span data-ttu-id="6edb2-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6edb2-114">**String**</span></span> <br/> | <span data-ttu-id="6edb2-115">呼び出すプロシージャの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="6edb2-116">_プロジェクト_</span><span class="sxs-lookup"><span data-stu-id="6edb2-116">_project_</span></span> <br/> |<span data-ttu-id="6edb2-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="6edb2-117">Optional</span></span>  <br/> |<span data-ttu-id="6edb2-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="6edb2-118">**String**</span></span> <br/> |<span data-ttu-id="6edb2-119">プロシージャが含まれるプロジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="6edb2-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="6edb2-120">_arg_</span></span> <br/> |<span data-ttu-id="6edb2-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="6edb2-121">Optional</span></span>  <br/> |<span data-ttu-id="6edb2-122">**数値、文字列、日付、または通貨**</span><span class="sxs-lookup"><span data-stu-id="6edb2-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="6edb2-123">パラメーターとしてプロシージャに渡されます。</span><span class="sxs-lookup"><span data-stu-id="6edb2-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6edb2-124">注釈</span><span class="sxs-lookup"><span data-stu-id="6edb2-124">Remarks</span></span>

<span data-ttu-id="6edb2-125">VBA プロジェクトでは、*プロシージャ*は次のように定義されます。</span><span class="sxs-lookup"><span data-stu-id="6edb2-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="6edb2-126">プロシージャ (*vsoShape*としてほとんどの場合において [arg1 と arg2... の種類として、入力])</span><span class="sxs-lookup"><span data-stu-id="6edb2-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="6edb2-127">*vsoShape*への参照が評価される CALLTHIS 数式を含んだ**Shape**オブジェクトおよび_arg1_、 *arg2*がその数式で指定された引数。</span><span class="sxs-lookup"><span data-stu-id="6edb2-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="6edb2-128">その*vsoShape*は、C++ のメンバー プロシージャに渡される"this"引数と同じように非常に近いものに注意してください。したがって名前"CALLTHIS"にします。</span><span class="sxs-lookup"><span data-stu-id="6edb2-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="6edb2-129">実際には、CALLTHIS を含む数式を含むセル読み取ることができるようには、「このプロシージャ呼び出すし、、図形に対する参照を渡すこと。</span><span class="sxs-lookup"><span data-stu-id="6edb2-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="6edb2-130">_プロジェクト_が指定されている場合、Microsoft Visio は、1 つ含まれている_プロジェクト_と呼び出し_プロシージャ_そのプロジェクト内のすべての開いているドキュメントをスキャンします。</span><span class="sxs-lookup"><span data-stu-id="6edb2-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="6edb2-131">_プロジェクト_が省略されるか null の場合 ("")、Visio では、対象となる CALLTHIS 数式を含む文書の VBA プロジェクト内の_プロシージャ_が前提としています。</span><span class="sxs-lookup"><span data-stu-id="6edb2-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="6edb2-132">_Arg1_に数値、 _arg2..._ は外部単位で渡されます。</span><span class="sxs-lookup"><span data-stu-id="6edb2-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="6edb2-133">たとえば、高さが 3 cm の図形から [Height] セルの値を渡すと、3 が渡されます。</span><span class="sxs-lookup"><span data-stu-id="6edb2-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="6edb2-134">渡すには別の単位数が、FORMATEX 関数を使用または明示的に null 単位 1 組、0 ft + 高さなどを追加することで単位を変換します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="6edb2-135">CALLTHIS 関数の 2 番目のカンマはオプションです。</span><span class="sxs-lookup"><span data-stu-id="6edb2-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="6edb2-136">それは、プロシージャに追加する追加のパラメーターの数に対応しています。</span><span class="sxs-lookup"><span data-stu-id="6edb2-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="6edb2-137">以外の場合は、追加パラメーターを使用しないと、 `(vsoShape as Visio.Shape)` 、2 つ目のコンマを追加しません。CALLTHIS("",) を使用します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="6edb2-138">2 つのパラメーターを追加する場合は、たとえば、CALLTHIS("",,,) を使用します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="6edb2-139">CALLTHIS 関数は常に 0 に評価し、_プロシージャ_への呼び出しは、再計算処理が完了したら、アイドル時間中に発生します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="6edb2-140">_プロシージャ_は、値を返すことができますが、Visio では無視されます。</span><span class="sxs-lookup"><span data-stu-id="6edb2-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="6edb2-141">_プロシージャ_では、CALLTHIS 数式を上書きする場合を除き、Visio は、ドキュメント内の数式または他のセルの結果を設定することで認識できる値がない_プロシージャ_を呼び出したセルを返します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="6edb2-142">CALLTHIS 関数では、図面のプロジェクトが別のプロジェクトを参照していなくても、そのプロジェクトを呼び出すことができます。この点が、RUNADDON 関数とは異なる点です。</span><span class="sxs-lookup"><span data-stu-id="6edb2-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="6edb2-143">Visio インスタンスが数式の CALLTHIS 関数を評価する場合、その結果呼び出された VBA コードでは、この数式を使用しているセルを含んだ図面を閉じないでください。アプリケーション エラーが発生して Visio が終了します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="6edb2-144">CALLTHIS 関数を使用するセルを含んだ図面を閉じる必要がある場合、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="6edb2-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="6edb2-145">VBA 以外のコードを使用して図面を閉じます。</span><span class="sxs-lookup"><span data-stu-id="6edb2-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="6edb2-146">閉じる図面以外のプロジェクトから図面を閉じます。</span><span class="sxs-lookup"><span data-stu-id="6edb2-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="6edb2-147">図面を閉じる代わりに、ウィンドウを閉じるためのウィンドウ メッセージを図面に通知します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="6edb2-148">Visio のコードの実行の詳細について[セキュリティ設定について、Visio でのコードの実行](about-security-settings-and-running-code-in-visio-shapesheet.md)でこの「シェイプ シート リファレンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6edb2-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6edb2-149">例 1</span><span class="sxs-lookup"><span data-stu-id="6edb2-149">Example 1</span></span>

<span data-ttu-id="6edb2-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span><span class="sxs-lookup"><span data-stu-id="6edb2-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="6edb2-151">モジュール内の p という名前のプロシージャを呼び出し、Height の値をセンチメートル単位 (7.62 cm など) で渡します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6edb2-152">例 2</span><span class="sxs-lookup"><span data-stu-id="6edb2-152">Example 2</span></span>

<span data-ttu-id="6edb2-153">CALLTHIS("q",,0 cm+Height,Width)</span><span class="sxs-lookup"><span data-stu-id="6edb2-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="6edb2-154">モジュール内の q という名前のプロシージャを呼び出し、セルの高さをセンチメートル単位で、幅を内部単位で渡します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6edb2-155">例 3</span><span class="sxs-lookup"><span data-stu-id="6edb2-155">Example 3</span></span>

<span data-ttu-id="6edb2-156">*ThisDocument*クラス モジュールに次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="6edb2-157">図形の [EventDblClick] セルでは、上記のプロシージャと共に次のいずれかの構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="6edb2-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="6edb2-158">CALLTHIS("ThisDocument.A",)</span><span class="sxs-lookup"><span data-stu-id="6edb2-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="6edb2-159">CALLTHIS("ThisDocument.B",,"Click")</span><span class="sxs-lookup"><span data-stu-id="6edb2-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="6edb2-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span><span class="sxs-lookup"><span data-stu-id="6edb2-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

