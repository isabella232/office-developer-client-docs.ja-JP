---
title: HYPERLINK 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251441
localization_priority: Normal
ms.assetid: 943636a6-e135-a626-7924-11e238156548
description: 指定したアドレスに移動します。これは、ファイル、UNC、または URL パスで指定できます。
ms.openlocfilehash: 5e4952c3d56eff0cb1e6518928a7b8259f645046
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329947"
---
# <a name="hyperlink-function"></a><span data-ttu-id="33974-103">HYPERLINK 関数</span><span class="sxs-lookup"><span data-stu-id="33974-103">HYPERLINK Function</span></span>

<span data-ttu-id="33974-104">指定したアドレスに移動します。これは、ファイル、UNC、または URL パスで指定できます。</span><span class="sxs-lookup"><span data-stu-id="33974-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="33974-105">構文</span><span class="sxs-lookup"><span data-stu-id="33974-105">Syntax</span></span>

<span data-ttu-id="33974-106">HYPERLINK ("\* \* *address* \* *" [, "* \* \*\* サブアドレス \* *", "* \* *extrainfo* \* \*", \* **ウィンドウ** *, "* \* *frame* \* \*")</span><span class="sxs-lookup"><span data-stu-id="33974-106">HYPERLINK(" \*\* *address* \*\* "[," \*\* *subaddress* \*\* "," \*\* *extrainfo* \*\* ", \*\* *window* \*\*," \*\* *frame* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="33974-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="33974-107">Parameters</span></span>

|<span data-ttu-id="33974-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="33974-108">**Name**</span></span>|<span data-ttu-id="33974-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="33974-109">**Required/Optional**</span></span>|<span data-ttu-id="33974-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="33974-110">**Data Type**</span></span>|<span data-ttu-id="33974-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="33974-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="33974-112">_address_</span><span class="sxs-lookup"><span data-stu-id="33974-112">_address_</span></span> <br/> |<span data-ttu-id="33974-113">必須</span><span class="sxs-lookup"><span data-stu-id="33974-113">Required</span></span>  <br/> |<span data-ttu-id="33974-114">**String**</span><span class="sxs-lookup"><span data-stu-id="33974-114">**String**</span></span> <br/> |<span data-ttu-id="33974-115">完全パスまたは相対パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="33974-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="33974-116">_subaddress_</span><span class="sxs-lookup"><span data-stu-id="33974-116">_subaddress_</span></span> <br/> |<span data-ttu-id="33974-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="33974-117">Optional</span></span>  <br/> |<span data-ttu-id="33974-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="33974-118">**String**</span></span> <br/> |<span data-ttu-id="33974-119">リンク先の address 内の位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="33974-119">Specifies a location within address to link to.</span></span> <span data-ttu-id="33974-120">たとえば、address が、Microsoft Visio ファイルの場合は subaddress にページ名を、Microsoft Excel ファイルの場合は subaddress にワークシートまたはワークシート内の範囲を、HTML ページの URL の場合は subaddress にアンカーを指定できます。</span><span class="sxs-lookup"><span data-stu-id="33974-120">For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="33974-121">_extrainfo_</span><span class="sxs-lookup"><span data-stu-id="33974-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="33974-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="33974-122">Optional</span></span>  <br/> |<span data-ttu-id="33974-123">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="33974-123">**String**</span></span> <br/> |<span data-ttu-id="33974-124">イメージ マップの座標など、URL の判別に使用する情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="33974-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="33974-125">_ウィンドウ_</span><span class="sxs-lookup"><span data-stu-id="33974-125">_window_</span></span> <br/> |<span data-ttu-id="33974-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="33974-126">Optional</span></span>  <br/> |<span data-ttu-id="33974-127">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="33974-127">**Boolean**</span></span> <br/> |<span data-ttu-id="33974-128">ハイパーリンクを新しいウィンドウで開くかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="33974-128">Specifies whether the hyperlink is opened in a new window.</span></span> <span data-ttu-id="33974-129">既定値は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="33974-129">The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="33974-130">_フレーム_</span><span class="sxs-lookup"><span data-stu-id="33974-130">_frame_</span></span> <br/> |<span data-ttu-id="33974-131">省略可能</span><span class="sxs-lookup"><span data-stu-id="33974-131">Optional</span></span>  <br/> |<span data-ttu-id="33974-132">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="33974-132">**String**</span></span> <br/> | <span data-ttu-id="33974-p103">Microsoft Internet Explorer 3.0 以降などの ActiveX ブラウザーで、ActiveX の図面として Visio の図面を開く場合に、ターゲットとするフレームの名前を指定します。既定では、空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="33974-p103">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33974-135">解説</span><span class="sxs-lookup"><span data-stu-id="33974-135">Remarks</span></span>

<span data-ttu-id="33974-p104">図面にベース パスがない場合、図面のパスに従ってリンク先まで移動します。図面が保存されないと、ハイパーリンクは未定義になります。</span><span class="sxs-lookup"><span data-stu-id="33974-p104">If the document has no base path, Visio navigates according to the document path. If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="33974-138">[**Visio のプロパティ**] ダイアログ ボックスで指定されている [**ハイパーリンクの基点**] フィールドに基づいて、相対パスが指定されます。</span><span class="sxs-lookup"><span data-stu-id="33974-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="33974-139">図面のページに移動するには、GOTOPAGE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="33974-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="33974-140">例 1</span><span class="sxs-lookup"><span data-stu-id="33974-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="33974-141">例 2</span><span class="sxs-lookup"><span data-stu-id="33974-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="33974-142">例 3</span><span class="sxs-lookup"><span data-stu-id="33974-142">Example 3</span></span>

 `HYPERLINK("https://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="33974-143">例 4</span><span class="sxs-lookup"><span data-stu-id="33974-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

