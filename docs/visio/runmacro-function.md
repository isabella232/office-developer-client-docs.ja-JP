---
title: RUNMACRO 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: マクロを Microsoft Visual Basic for Applications (VBA) プロジェクトします。
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806340"
---
# <a name="runmacro-function"></a><span data-ttu-id="ee1fe-103">RUNMACRO 関数</span><span class="sxs-lookup"><span data-stu-id="ee1fe-103">RUNMACRO Function</span></span>

<span data-ttu-id="ee1fe-104">マクロを Microsoft Visual Basic for Applications (VBA) プロジェクトします。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-104">Calls a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ee1fe-105">構文</span><span class="sxs-lookup"><span data-stu-id="ee1fe-105">Syntax</span></span>

<span data-ttu-id="ee1fe-106">RUNMACRO (* **マクロ名** * [、* * *projname_opt* * *])</span><span class="sxs-lookup"><span data-stu-id="ee1fe-106">RUNMACRO (** *macroname* ** [, ** *projname_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ee1fe-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ee1fe-107">Parameters</span></span>

|<span data-ttu-id="ee1fe-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="ee1fe-108">**Name**</span></span>|<span data-ttu-id="ee1fe-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ee1fe-109">**Required/Optional**</span></span>|<span data-ttu-id="ee1fe-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ee1fe-110">**Data Type**</span></span>|<span data-ttu-id="ee1fe-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="ee1fe-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ee1fe-112">_マクロ名_</span><span class="sxs-lookup"><span data-stu-id="ee1fe-112">_macroname_</span></span> <br/> |<span data-ttu-id="ee1fe-113">必須</span><span class="sxs-lookup"><span data-stu-id="ee1fe-113">Required</span></span>  <br/> |<span data-ttu-id="ee1fe-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="ee1fe-114">**String**</span></span> <br/> |<span data-ttu-id="ee1fe-115">呼び出すマクロの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-115">The name of the macro to call.</span></span>  <br/> |
| <span data-ttu-id="ee1fe-116">_projname_opt_</span><span class="sxs-lookup"><span data-stu-id="ee1fe-116">_projname_opt_</span></span> <br/> |<span data-ttu-id="ee1fe-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="ee1fe-117">Optional</span></span>  <br/> |<span data-ttu-id="ee1fe-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="ee1fe-118">**String**</span></span> <br/> | <span data-ttu-id="ee1fe-119">マクロが含まれるプロジェクトを指定します。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-119">The project that contains the macro.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee1fe-120">注釈</span><span class="sxs-lookup"><span data-stu-id="ee1fe-120">Remarks</span></span>

<span data-ttu-id="ee1fe-121">プロジェクトが指定されている場合、Microsoft Visio は、1 つ含まれている_projname_opt_と呼び出し_マクロ名_をプロジェクト内のすべての開いているドキュメントをスキャンします。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-121">If a project is specified, Microsoft Visio scans all open documents for the one containing  _projname_opt_ and calls  _macroname_ in that project.</span></span> <span data-ttu-id="ee1fe-122">_Projname_opt_が省略されるか null の場合 ("")、_マクロ名_を評価する RUNMACRO 数式を含む文書の VBA プロジェクト内にあると見なされます。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-122">If  _projname_opt_ is omitted or null (""),  _macroname_ is assumed to be in the VBA project of the document that contains the RUNMACRO formula being evaluated.</span></span> 
  
<span data-ttu-id="ee1fe-123">RUNMACRO 関数は、_マクロ名_に評価される式を所有している図形への参照に合格しないことで、CALLTHIS 関数とは異なります。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-123">The RUNMACRO function differs from the CALLTHIS function in that it does not pass a reference to the shape that owns the formula being evaluated to  _macroname_.</span></span> <span data-ttu-id="ee1fe-124">CALLTHIS のような RUNMACRO 関数は_projname_opt_をそれへの呼び出しをへの参照を必要としません。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-124">Like CALLTHIS, the RUNMACRO function doesn't require a reference to  _projname_opt_ to call into it.</span></span> 
  
 <span data-ttu-id="ee1fe-125">Visio インスタンスが数式の RUNMACRO 関数を評価するときに呼び出す VBA コードでは、この数式を使用しているセルを含んだ図面を閉じないでください。アプリケーション エラーが発生して Visio が終了します。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-125">VBA code that is invoked when the Visio instance evaluates a RUNMACRO function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="ee1fe-126">RUNMACRO 関数を使用するセルを含んだ図面を閉じる必要がある場合、次のいずれかの操作を行います。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-126">If you need to close the document containing the cell that uses the RUNMACRO function, use one of the following techniques:</span></span>
  
- <span data-ttu-id="ee1fe-127">VBA 以外のコードを使用して図面を閉じます。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-127">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="ee1fe-128">閉じる図面以外のプロジェクトから図面を閉じます。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-128">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="ee1fe-129">図面を閉じる代わりに、ウィンドウを閉じるためのウィンドウ メッセージを図面に通知します。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-129">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="ee1fe-130">Visio でのコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定およびコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-130">For more information about running code in Visio, see [About security settings and running code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ee1fe-131">例</span><span class="sxs-lookup"><span data-stu-id="ee1fe-131">Example</span></span>

<span data-ttu-id="ee1fe-132">次の例では、RUNMACRO 数式を含む VBA プロジェクトの ThisDocument クラス モジュールの MyTest というマクロを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ee1fe-132">The following example invokes a macro called MyTest in the ThisDocument class module of the VBA project containing the RUNMACRO formula.</span></span> 
  
<span data-ttu-id="ee1fe-133">RUNMACRO ("ThisDocument.MyTest")</span><span class="sxs-lookup"><span data-stu-id="ee1fe-133">RUNMACRO ("ThisDocument.MyTest")</span></span> 
  

