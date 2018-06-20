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
description: アドオンまたはマクロで、Microsoft Visual Basic for Applications (VBA) プロジェクトを実行します。
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806343"
---
# <a name="runaddon-function"></a><span data-ttu-id="4d53d-103">RUNADDON 関数</span><span class="sxs-lookup"><span data-stu-id="4d53d-103">RUNADDON Function</span></span>

<span data-ttu-id="4d53d-104">アドオンまたはマクロで、Microsoft Visual Basic for Applications (VBA) プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="4d53d-104">Executes an add-on or a macro in a Microsoft Visual Basic for Applications (VBA) project.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4d53d-105">構文</span><span class="sxs-lookup"><span data-stu-id="4d53d-105">Syntax</span></span>

<span data-ttu-id="4d53d-106">RUNADDON (以下"*文字列*")</span><span class="sxs-lookup"><span data-stu-id="4d53d-106">RUNADDON(" *string*  ")</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4d53d-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="4d53d-107">Parameters</span></span>

|<span data-ttu-id="4d53d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="4d53d-108">**Name**</span></span>|<span data-ttu-id="4d53d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="4d53d-109">**Required/Optional**</span></span>|<span data-ttu-id="4d53d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="4d53d-110">**Data Type**</span></span>|<span data-ttu-id="4d53d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="4d53d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4d53d-112">_string_</span><span class="sxs-lookup"><span data-stu-id="4d53d-112">_string_</span></span> <br/> |<span data-ttu-id="4d53d-113">必須</span><span class="sxs-lookup"><span data-stu-id="4d53d-113">Required</span></span>  <br/> |<span data-ttu-id="4d53d-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="4d53d-114">**String**</span></span> <br/> | <span data-ttu-id="4d53d-115">**Addons**コレクション内のアドオンまたは VBA プロジェクト内のマクロの名前です。</span><span class="sxs-lookup"><span data-stu-id="4d53d-115">The name of an add-on in the **Addons** collection or a macro in a VBA project.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d53d-116">備考</span><span class="sxs-lookup"><span data-stu-id="4d53d-116">Remarks</span></span>

<span data-ttu-id="4d53d-117">RUNADDON 関数呼び出しを含む図面のプロジェクト (または別のプロジェクトが参照されている場合) は_文字列_をという名前のマクロ (引数を持たないプロシージャ) を持たない場合、Microsoft Visio は、 _string_という名前のアドオンを実行します。</span><span class="sxs-lookup"><span data-stu-id="4d53d-117">If the project of the document that contains the RUNADDON function call (or another project if it is referenced) does not have a macro (a procedure with no arguments) named  _string_, Microsoft Visio runs the add-on named  _string_.</span></span> <span data-ttu-id="4d53d-118">_String_という名前のアドオンが見つからない場合、Visio は何もし、エラーは報告されません。</span><span class="sxs-lookup"><span data-stu-id="4d53d-118">If no add-on named  _string_ can be found, Visio does nothing and reports no error.</span></span> <span data-ttu-id="4d53d-119">( **TraceFlags**プロパティはプロシージャを実行しようとしている Visio のアドオンを監視するのに使用ことができます)。</span><span class="sxs-lookup"><span data-stu-id="4d53d-119">(You can use the **TraceFlags** property to monitor the procedures and add-ons that Visio attempts to run.)</span></span> 
  
<span data-ttu-id="4d53d-120">標準モジュールでプロシージャを呼び出す、ときに、複数のモジュールが同じ名前のプロシージャを持つことができますので、プロシージャ (たとえば、 *moduleName.procName*) を含むモジュールの名前を持つ文字列を付けることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4d53d-120">When you call a procedure in a standard module, it is recommended that you prefix the string with the module name that contains the procedure (for example,  *moduleName.procName*), because more than one module can have a procedure with the same name.</span></span> 
  
<span data-ttu-id="4d53d-121">プロジェクト内のプロシージャを呼び出す以外の RUNADDON 関数呼び出しを含む図面のプロジェクトを使用して、構文*projName.modName.procName* (する必要がありますが明示的に設定する*projName*への参照、VBA プロジェクトに)。</span><span class="sxs-lookup"><span data-stu-id="4d53d-121">To call a procedure in a project other than the project of the document that contains the RUNADDON function call, use the syntax  *projName.modName.procName*  (you must have explicitly set a reference to  *projName*  in your VBA project).</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="4d53d-p102">Visio 2002 以降、RUNADDON 関数は任意の VBA コードを含む文字列を実行できなくなりました。従来 RUNADDON 関数に渡されていたコードは、RUNADDON 関数から呼び出される図面の VBA プロジェクト内のプロシージャへ移動することができます。</span><span class="sxs-lookup"><span data-stu-id="4d53d-p102">Beginning with Visio 2002, the RUNADDON function cannot execute a string containing arbitrary VBA code. Code that was formerly passed to the RUNADDON function can be moved to a procedure in a document's VBA project that is called from the RUNADDON function.</span></span> 
  
<span data-ttu-id="4d53d-124">Visio のコードの実行の詳細について[セキュリティ設定について、Visio でのコードの実行](about-security-settings-and-running-code-in-visio-shapesheet.md)でこの「シェイプ シート リファレンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d53d-124">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
<span data-ttu-id="4d53d-p103">以前のバージョンの Visio では、この関数は _RUNADDON に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。</span><span class="sxs-lookup"><span data-stu-id="4d53d-p103">In earlier versions of Visio, this function appears as _RUNADDON. Visio versions 4.0 and later accept either style.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4d53d-127">例 1</span><span class="sxs-lookup"><span data-stu-id="4d53d-127">Example 1</span></span>

<span data-ttu-id="4d53d-128">RUNADDON("Calendar.exe")</span><span class="sxs-lookup"><span data-stu-id="4d53d-128">RUNADDON("Calendar.exe")</span></span>
  
<span data-ttu-id="4d53d-129">Calendar.exe と呼ばれるアドオンを起動します。</span><span class="sxs-lookup"><span data-stu-id="4d53d-129">Launches an add-on called Calendar.exe.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4d53d-130">例 2</span><span class="sxs-lookup"><span data-stu-id="4d53d-130">Example 2</span></span>

<span data-ttu-id="4d53d-131">RUNADDON("Array Shapes")</span><span class="sxs-lookup"><span data-stu-id="4d53d-131">RUNADDON("Array Shapes")</span></span>
  
<span data-ttu-id="4d53d-132">Array Shapes という名の (VSL 実装) アドオンを起動します。</span><span class="sxs-lookup"><span data-stu-id="4d53d-132">Launches the (VSL-implemented) add-on whose name is Array Shapes.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4d53d-133">例 3</span><span class="sxs-lookup"><span data-stu-id="4d53d-133">Example 3</span></span>

<span data-ttu-id="4d53d-134">RUNADDON("ThisDocument.ReportStatistics")</span><span class="sxs-lookup"><span data-stu-id="4d53d-134">RUNADDON("ThisDocument.ReportStatistics")</span></span>
  
<span data-ttu-id="4d53d-135">この関数の呼び出しが含まれているドキュメント プロジェクトの**ThisDocument**モジュール内の ReportStatistics マクロを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4d53d-135">Calls the ReportStatistics macro in the **ThisDocument** module in the document project containing this function call.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="4d53d-136">**ThisDocument**モジュール内のマクロを呼び出すには、"ThisDocument"のように文字列を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d53d-136">To invoke a macro in the **ThisDocument** module, you must preface the string with "ThisDocument" as shown.</span></span> 
  
## <a name="example-4"></a><span data-ttu-id="4d53d-137">例 4</span><span class="sxs-lookup"><span data-stu-id="4d53d-137">Example 4</span></span>

<span data-ttu-id="4d53d-138">RUNADDON ("*します*。ReportStatistics」)</span><span class="sxs-lookup"><span data-stu-id="4d53d-138">RUNADDON(" *ModuleName*  .ReportStatistics")</span></span> 
  
<span data-ttu-id="4d53d-139">ドキュメントを含むプロジェクトをこの関数の呼び出しで、*モジュール名*で ReportStatistics マクロを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4d53d-139">Calls the ReportStatistics macro in  *ModuleName*  in the document project that contains this function call.</span></span> 
  

