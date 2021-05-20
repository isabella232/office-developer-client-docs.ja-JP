---
title: RUNADDON 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Microsoft Visual Basic for Applications (VBA) プロジェクトでアドオンまたはマクロを実行します。
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432010"
---
# <a name="runaddon-function"></a><span data-ttu-id="9243d-103">RUNADDON 関数</span><span class="sxs-lookup"><span data-stu-id="9243d-103">RUNADDON Function</span></span>

<span data-ttu-id="9243d-104">Microsoft Visual Basic for Applications (VBA) プロジェクトでアドオンまたはマクロを実行します。</span><span class="sxs-lookup"><span data-stu-id="9243d-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9243d-105">構文</span><span class="sxs-lookup"><span data-stu-id="9243d-105">Syntax</span></span>

<span data-ttu-id="9243d-106">RUNADDON() *文字列*  ")</span><span class="sxs-lookup"><span data-stu-id="9243d-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9243d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9243d-107">Parameters</span></span>

|<span data-ttu-id="9243d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="9243d-108">**Name**</span></span>|<span data-ttu-id="9243d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="9243d-109">**Required/Optional**</span></span>|<span data-ttu-id="9243d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="9243d-110">**Data Type**</span></span>|<span data-ttu-id="9243d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="9243d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9243d-112">_string_</span><span class="sxs-lookup"><span data-stu-id="9243d-112">_string_</span></span> <br/> |<span data-ttu-id="9243d-113">必須</span><span class="sxs-lookup"><span data-stu-id="9243d-113">Required</span></span>  <br/> |<span data-ttu-id="9243d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="9243d-114">**String**</span></span> <br/> | <span data-ttu-id="9243d-115">VBA プロジェクト内の **Addons** コレクションまたはマクロ内のアドオンの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="9243d-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9243d-116">注釈</span><span class="sxs-lookup"><span data-stu-id="9243d-116">Remarks</span></span>

<span data-ttu-id="9243d-117">RUNADDON 関数呼び出しを含むドキュメントのプロジェクト (または参照されている場合は別のプロジェクト) に、string という名前のマクロ (引数を持つプロシージャ) がない場合、Microsoft Visio はアドオンの名前付き文字列 _を実行します_。</span><span class="sxs-lookup"><span data-stu-id="9243d-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="9243d-118">名前付き文字列が見つからない場合、Visioは何も実行し、エラーは報告しません。</span><span class="sxs-lookup"><span data-stu-id="9243d-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="9243d-119">**TraceFlags** プロパティを使用すると、Visio が実行しようとするプロシージャとアドオンを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="9243d-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="9243d-120">標準モジュールでプロシージャを呼び出す場合は、複数のモジュールが同じ名前のプロシージャを持つ可能性があるため、プロシージャを含むモジュール名  *(moduleName.procName* など) を文字列の先頭に付けます。</span><span class="sxs-lookup"><span data-stu-id="9243d-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="9243d-121">RUNADDON 関数呼び出しを含むドキュメントのプロジェクト以外のプロジェクトでプロシージャを呼び出す場合は、  *構文 projName.modName.procName*  を使用します (VBA プロジェクトで  *projName*  への参照を明示的に設定している必要があります)。</span><span class="sxs-lookup"><span data-stu-id="9243d-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="9243d-p102">Visio 2002 以降、RUNADDON 関数は任意の VBA コードを含む文字列を実行できなくなりました。従来 RUNADDON 関数に渡されていたコードは、RUNADDON 関数から呼び出される図面の VBA プロジェクト内のプロシージャへ移動することができます。</span><span class="sxs-lookup"><span data-stu-id="9243d-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="9243d-124">Visio でのコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定とコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9243d-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="9243d-p103">以前のバージョンの Visio では、この関数は _RUNADDON に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="9243d-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="9243d-127">例 1</span><span class="sxs-lookup"><span data-stu-id="9243d-127">Example 1</span></span>

<span data-ttu-id="9243d-128">RUNADDON("Calendar.exe")</span><span class="sxs-lookup"><span data-stu-id="9243d-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="9243d-129">アドインと呼ばれるアドオンを起動Calendar.exe。</span><span class="sxs-lookup"><span data-stu-id="9243d-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="9243d-130">例 2</span><span class="sxs-lookup"><span data-stu-id="9243d-130">Example 2</span></span>

<span data-ttu-id="9243d-131">RUNADDON("Array Shapes")</span><span class="sxs-lookup"><span data-stu-id="9243d-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="9243d-132">Array Shapes という名の (VSL 実装) アドオンを起動します。</span><span class="sxs-lookup"><span data-stu-id="9243d-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="9243d-133">例 3</span><span class="sxs-lookup"><span data-stu-id="9243d-133">Example 3</span></span>

<span data-ttu-id="9243d-134">RUNADDON("ThisDocument.ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="9243d-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="9243d-135">この関数呼び出しを含む図面プロジェクト内の **ThisDocument** モジュール内で ReportStatistics マクロを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9243d-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="9243d-136">**ThisDocument** モジュール内でマクロを起動するには文字列の前に「ThisDocument」を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="9243d-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="9243d-137">例 4</span><span class="sxs-lookup"><span data-stu-id="9243d-137">Example 4</span></span>

<span data-ttu-id="9243d-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="9243d-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="9243d-139">この関数呼び出しを含むドキュメント プロジェクト  *の ModuleName*  の ReportStatistics マクロを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9243d-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

