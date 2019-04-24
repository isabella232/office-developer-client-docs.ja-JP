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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319062"
---
# <a name="runaddon-function"></a><span data-ttu-id="f64c2-103">RUNADDON 関数</span><span class="sxs-lookup"><span data-stu-id="f64c2-103">RUNADDON Function</span></span>

<span data-ttu-id="f64c2-104">Microsoft Visual Basic for Applications (VBA) プロジェクトでアドオンまたはマクロを実行します。</span><span class="sxs-lookup"><span data-stu-id="f64c2-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f64c2-105">構文</span><span class="sxs-lookup"><span data-stu-id="f64c2-105">Syntax</span></span>

<span data-ttu-id="f64c2-106">RUNADDON (" *string* ")</span><span class="sxs-lookup"><span data-stu-id="f64c2-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f64c2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f64c2-107">Parameters</span></span>

|<span data-ttu-id="f64c2-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="f64c2-108">**Name**</span></span>|<span data-ttu-id="f64c2-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f64c2-109">**Required/Optional**</span></span>|<span data-ttu-id="f64c2-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f64c2-110">**Data Type**</span></span>|<span data-ttu-id="f64c2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="f64c2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f64c2-112">_string_</span><span class="sxs-lookup"><span data-stu-id="f64c2-112">_string_</span></span> <br/> |<span data-ttu-id="f64c2-113">必須</span><span class="sxs-lookup"><span data-stu-id="f64c2-113">Required</span></span>  <br/> |<span data-ttu-id="f64c2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f64c2-114">**String**</span></span> <br/> | <span data-ttu-id="f64c2-115">VBA プロジェクト内の **Addons** コレクションまたはマクロ内のアドオンの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f64c2-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f64c2-116">解説</span><span class="sxs-lookup"><span data-stu-id="f64c2-116">Remarks</span></span>

<span data-ttu-id="f64c2-117">RUNADDON 関数呼び出しを含むドキュメントのプロジェクト (または、参照されている場合は別のプロジェクト) に、 _string_という名前のマクロ (引数を持たないプロシージャ) が含まれていないと、Microsoft Visio は、_文字列_という名前のアドオンを実行します。</span><span class="sxs-lookup"><span data-stu-id="f64c2-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="f64c2-118">指定した名前のアドイン__ が見つからない場合、Visio は何もエラーを報告しません。</span><span class="sxs-lookup"><span data-stu-id="f64c2-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="f64c2-119">**TraceFlags** プロパティを使用すると、Visio が実行しようとするプロシージャとアドオンを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="f64c2-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="f64c2-120">標準モジュール内のプロシージャを呼び出すときは、複数のモジュールに同じ名前のプロシージャを含めることができるので、プロシージャを含むモジュール名 (たとえば、 *procName*) で文字列の先頭に指定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f64c2-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="f64c2-121">RUNADDON 関数呼び出しを含む図面のプロジェクト以外のプロジェクトでプロシージャを呼び出すには、*から*を使用します (VBA プロジェクトの*projName*への参照を明示的に設定する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="f64c2-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="f64c2-p102">Visio 2002 以降、RUNADDON 関数は任意の VBA コードを含む文字列を実行できなくなりました。従来 RUNADDON 関数に渡されていたコードは、RUNADDON 関数から呼び出される図面の VBA プロジェクト内のプロシージャへ移動することができます。</span><span class="sxs-lookup"><span data-stu-id="f64c2-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="f64c2-124">Visio でのコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定とコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f64c2-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="f64c2-p103">以前のバージョンの Visio では、この関数は _RUNADDON に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="f64c2-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f64c2-127">例 1</span><span class="sxs-lookup"><span data-stu-id="f64c2-127">Example 1</span></span>

<span data-ttu-id="f64c2-128">RUNADDON ("Calendar")</span><span class="sxs-lookup"><span data-stu-id="f64c2-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="f64c2-129">予定表 .exe というアドオンを起動します。</span><span class="sxs-lookup"><span data-stu-id="f64c2-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f64c2-130">例 2</span><span class="sxs-lookup"><span data-stu-id="f64c2-130">Example 2</span></span>

<span data-ttu-id="f64c2-131">RUNADDON("Array Shapes")</span><span class="sxs-lookup"><span data-stu-id="f64c2-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="f64c2-132">Array Shapes という名の (VSL 実装) アドオンを起動します。</span><span class="sxs-lookup"><span data-stu-id="f64c2-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f64c2-133">例 3</span><span class="sxs-lookup"><span data-stu-id="f64c2-133">Example 3</span></span>

<span data-ttu-id="f64c2-134">RUNADDON ("ThisDocument statistics")</span><span class="sxs-lookup"><span data-stu-id="f64c2-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="f64c2-135">この関数呼び出しを含む図面プロジェクト内の **ThisDocument** モジュール内で ReportStatistics マクロを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f64c2-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="f64c2-136">**ThisDocument** モジュール内でマクロを起動するには文字列の前に「ThisDocument」を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="f64c2-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="f64c2-137">例 4</span><span class="sxs-lookup"><span data-stu-id="f64c2-137">Example 4</span></span>

<span data-ttu-id="f64c2-138">RUNADDON (" *ModuleName* .reportstatistics ")</span><span class="sxs-lookup"><span data-stu-id="f64c2-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="f64c2-139">この関数呼び出しを含むドキュメントプロジェクトの*ModuleName*内で reportstatistics マクロを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f64c2-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

