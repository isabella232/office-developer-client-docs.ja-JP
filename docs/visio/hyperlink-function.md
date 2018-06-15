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
description: ファイル、UNC、または URL にすることができますが、指定したアドレスに移動したパスです。
ms.openlocfilehash: 4e86fd3682d5d9e26c52839e76d2016d654b3141
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805540"
---
# <a name="hyperlink-function"></a><span data-ttu-id="cd87b-103">HYPERLINK 関数</span><span class="sxs-lookup"><span data-stu-id="cd87b-103">HYPERLINK Function</span></span>

<span data-ttu-id="cd87b-104">ファイル、UNC、または URL にすることができますが、指定したアドレスに移動したパスです。</span><span class="sxs-lookup"><span data-stu-id="cd87b-104">Navigates to the specified address, which can be a file, UNC, or URL path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="cd87b-105">構文</span><span class="sxs-lookup"><span data-stu-id="cd87b-105">Syntax</span></span>

<span data-ttu-id="cd87b-106">ハイパーリンク ("* **アドレス** *」[」* **サブアドレス** *「,」* * *extrainfo* * *」、* **ウィンドウ** *、"* **フレーム** *"])</span><span class="sxs-lookup"><span data-stu-id="cd87b-106">HYPERLINK(" ** *address* ** "[," ** *subaddress* ** "," ** *extrainfo* ** ", ** *window* **," ** *frame* ** "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cd87b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd87b-107">Parameters</span></span>

|<span data-ttu-id="cd87b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="cd87b-108">**Name**</span></span>|<span data-ttu-id="cd87b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="cd87b-109">**Required/Optional**</span></span>|<span data-ttu-id="cd87b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="cd87b-110">**Data Type**</span></span>|<span data-ttu-id="cd87b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="cd87b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cd87b-112">_アドレス_</span><span class="sxs-lookup"><span data-stu-id="cd87b-112">_address_</span></span> <br/> |<span data-ttu-id="cd87b-113">必須</span><span class="sxs-lookup"><span data-stu-id="cd87b-113">Required</span></span>  <br/> |<span data-ttu-id="cd87b-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="cd87b-114">**String**</span></span> <br/> |<span data-ttu-id="cd87b-115">完全パスまたは相対パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="cd87b-115">A full path or a relative path.</span></span>  <br/> |
| <span data-ttu-id="cd87b-116">_サブアドレス_</span><span class="sxs-lookup"><span data-stu-id="cd87b-116">_subaddress_</span></span> <br/> |<span data-ttu-id="cd87b-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="cd87b-117">Optional</span></span>  <br/> |<span data-ttu-id="cd87b-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="cd87b-118">**String**</span></span> <br/> |<span data-ttu-id="cd87b-119">リンク先のアドレス内の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="cd87b-119">Specifies a location within address to link to.</span></span> <span data-ttu-id="cd87b-120">たとえば、アドレスが、Microsoft Visio ファイルの場合は、サブアドレスは、ページの名前です。サブアドレスは、ワークシートまたは範囲は、ワークシート内で場合は、Microsoft Excel のファイルでは、します。場合は HTML ページの URL、サブアドレスのアンカーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cd87b-120">For example, if address is a Microsoft Visio file, subaddress can be a page name; if a Microsoft Excel file, subaddress can be a worksheet or range within a worksheet; if a URL for an HTML page, subaddress can be an anchor.</span></span>  <br/> |
| <span data-ttu-id="cd87b-121">_extrainfo_</span><span class="sxs-lookup"><span data-stu-id="cd87b-121">_extrainfo_</span></span> <br/> |<span data-ttu-id="cd87b-122">省略可能</span><span class="sxs-lookup"><span data-stu-id="cd87b-122">Optional</span></span>  <br/> |<span data-ttu-id="cd87b-123">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="cd87b-123">**String**</span></span> <br/> |<span data-ttu-id="cd87b-124">イメージ マップの座標など、URL の判別に使用する情報を渡します。</span><span class="sxs-lookup"><span data-stu-id="cd87b-124">Passes information used in resolving the URL, such as the coordinates of an image map.</span></span>  <br/> |
| <span data-ttu-id="cd87b-125">_ウィンドウ_</span><span class="sxs-lookup"><span data-stu-id="cd87b-125">_window_</span></span> <br/> |<span data-ttu-id="cd87b-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="cd87b-126">Optional</span></span>  <br/> |<span data-ttu-id="cd87b-127">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="cd87b-127">**Boolean**</span></span> <br/> |<span data-ttu-id="cd87b-p102">ハイパーリンクを新しいウィンドウで開くかどうかを指定します。既定値は FALSE です。</span><span class="sxs-lookup"><span data-stu-id="cd87b-p102">Specifies whether the hyperlink is opened in a new window. The default value is FALSE.</span></span>  <br/> |
| <span data-ttu-id="cd87b-130">_フレーム_</span><span class="sxs-lookup"><span data-stu-id="cd87b-130">_frame_</span></span> <br/> |<span data-ttu-id="cd87b-131">省略可能</span><span class="sxs-lookup"><span data-stu-id="cd87b-131">Optional</span></span>  <br/> |<span data-ttu-id="cd87b-132">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="cd87b-132">**String**</span></span> <br/> | <span data-ttu-id="cd87b-p103">Microsoft Internet Explorer 3.0 以降などの ActiveX ブラウザーで、ActiveX の図面として Visio の図面を開く場合に、ターゲットとするフレームの名前を指定します。既定では、空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="cd87b-p103">Specifies the name of a frame to target when Visio is open as an Active document in an ActiveX browser, such as Microsoft Internet Explorer 3.0 or later. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd87b-135">注釈</span><span class="sxs-lookup"><span data-stu-id="cd87b-135">Remarks</span></span>

<span data-ttu-id="cd87b-p104">図面にベース パスがない場合、図面のパスに従ってリンク先まで移動します。図面が保存されないと、ハイパーリンクは未定義になります。</span><span class="sxs-lookup"><span data-stu-id="cd87b-p104">If the document has no base path, Visio navigates according to the document path. If the document has not been saved, the hyperlink is undefined.</span></span> 
  
<span data-ttu-id="cd87b-138">相対パスは、 **Visio のプロパティ**] ダイアログ ボックスで指定されている**ハイパーリンクの基点**] のフィールドに基づいています。</span><span class="sxs-lookup"><span data-stu-id="cd87b-138">Relative paths are based on the **Hyperlink base** field specified in the **Visio Properties** dialog box.</span></span> 
  
<span data-ttu-id="cd87b-139">図面のページに移動するには、GOTOPAGE 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd87b-139">You can use the GOTOPAGE function to navigate to pages of a document.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="cd87b-140">例 1</span><span class="sxs-lookup"><span data-stu-id="cd87b-140">Example 1</span></span>

 `HYPERLINK("C:\My Documents\Drawing1.vsdx")`
  
## <a name="example-2"></a><span data-ttu-id="cd87b-141">例 2</span><span class="sxs-lookup"><span data-stu-id="cd87b-141">Example 2</span></span>

 `HYPERLINK("\\Server\Share\Drawing1.vsdx")`
  
## <a name="example-3"></a><span data-ttu-id="cd87b-142">例 3</span><span class="sxs-lookup"><span data-stu-id="cd87b-142">Example 3</span></span>

 `HYPERLINK("http://www.microsoft.com")`
  
## <a name="example-4"></a><span data-ttu-id="cd87b-143">例 4</span><span class="sxs-lookup"><span data-stu-id="cd87b-143">Example 4</span></span>

 `HYPERLINK("..\data.xlsx","sheet1!A1")`
  

