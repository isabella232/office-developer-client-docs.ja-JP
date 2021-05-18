---
title: '[Hyperlink] 行 ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3065
localization_priority: Normal
ms.assetid: e3c7ae27-2e54-a174-4fb3-d16093faf759
description: 図形に関連付けられた、単一のハイパーリンクの情報を格納します。図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。
ms.openlocfilehash: 36b9b62f248e4f5b9407156a79fa674dc2e8f14d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329905"
---
# <a name="hyperlink-row-hyperlinks-section"></a><span data-ttu-id="5ee51-104">[Hyperlink] 行 ([Hyperlinks] セクション)</span><span class="sxs-lookup"><span data-stu-id="5ee51-104">Hyperlink Row (Hyperlinks Section)</span></span>

<span data-ttu-id="5ee51-p102">図形に関連付けられた、単一のハイパーリンクの情報を格納します。図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。</span><span class="sxs-lookup"><span data-stu-id="5ee51-p102">Contains the information for a single hyperlink associated with a shape. A shape will contain one Hyperlink row for each hyperlink.</span></span>
  
<span data-ttu-id="5ee51-107">[Hyperlink] 行の名前は Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="5ee51-107">Hyperlink rows are named Hyperlink.</span></span> <span data-ttu-id="5ee51-108">*名前*  を指定し、次のセルを含む。</span><span class="sxs-lookup"><span data-stu-id="5ee51-108">*name*  and contain the following cells.</span></span> <span data-ttu-id="5ee51-109">詳細については、各セルに関連する項目を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ee51-109">For more details, see the specific cell topics.</span></span> 
  
|<span data-ttu-id="5ee51-110">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5ee51-110">**Cell**</span></span>|<span data-ttu-id="5ee51-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5ee51-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5ee51-112">説明</span><span class="sxs-lookup"><span data-stu-id="5ee51-112">Description</span></span>](description-cell-hyperlinks-section.md) <br/> |<span data-ttu-id="5ee51-113">ハイパーリンクを説明するテキスト文字列です。</span><span class="sxs-lookup"><span data-stu-id="5ee51-113">A descriptive text string for a hyperlink.</span></span>  <br/> |
|[<span data-ttu-id="5ee51-114">Address</span><span class="sxs-lookup"><span data-stu-id="5ee51-114">Address</span></span>](address-cell-hyperlinks-section.md) <br/> |<span data-ttu-id="5ee51-115">移動先の URL アドレス、MS-DOS ファイル名、または UNC パスです。</span><span class="sxs-lookup"><span data-stu-id="5ee51-115">A URL address, MS-DOS file name, or UNC path to which to jump.</span></span>  <br/> |
|[<span data-ttu-id="5ee51-116">SubAddress</span><span class="sxs-lookup"><span data-stu-id="5ee51-116">SubAddress</span></span>](subaddress-cell-hyperlinks-section.md) <br/> |<span data-ttu-id="5ee51-117">リンク先のターゲット図面内での位置です。</span><span class="sxs-lookup"><span data-stu-id="5ee51-117">A location within the target document to link to.</span></span>  <br/> |
|[<span data-ttu-id="5ee51-118">ExtraInfo</span><span class="sxs-lookup"><span data-stu-id="5ee51-118">ExtraInfo</span></span>](extrainfo-cell-hyperlinks-section.md) <br/> |<span data-ttu-id="5ee51-119">URL の解決に使用される情報を渡す文字列です。</span><span class="sxs-lookup"><span data-stu-id="5ee51-119">A string that passes information to be used in resolving a URL.</span></span>  <br/> |
|[<span data-ttu-id="5ee51-120">Frame</span><span class="sxs-lookup"><span data-stu-id="5ee51-120">Frame</span></span>](frame-cell-hyperlinks-section.md) <br/> |<span data-ttu-id="5ee51-p104">ActiveX コンテナーで、ActiveX の図面として Microsoft Office Visio の図面を開く場合に、ターゲットとするフレームの名前です。既定では、空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="5ee51-p104">The name of a frame to target when Microsoft Office Visio is open as an Active document in an ActiveX container. The default is an empty string.</span></span>  <br/> |
|[<span data-ttu-id="5ee51-123">SortKey</span><span class="sxs-lookup"><span data-stu-id="5ee51-123">SortKey</span></span>](sortkey-cell-hyperlinks-section.md) <br/> |<span data-ttu-id="5ee51-124">ハイパーリンクがショートカット メニューに表示されるときの順序を判別します。</span><span class="sxs-lookup"><span data-stu-id="5ee51-124">Determines the order of hyperlinks as they appear on the shortcut menu.</span></span>  <br/> |
|[<span data-ttu-id="5ee51-125">NewWindow</span><span class="sxs-lookup"><span data-stu-id="5ee51-125">NewWindow</span></span>](newwindow-cell-hyperlinks-section.md) <br/> |<span data-ttu-id="5ee51-126">ハイパーリンクを新しいウィンドウで開くかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="5ee51-126">Specifies whether to open the hyperlink in a new window.</span></span> <span data-ttu-id="5ee51-127">TRUE の場合、リンクされたページ、ドキュメント、または Web サイトを新しいウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="5ee51-127">If TRUE, opens the linked page, document, or website in a new window.</span></span> <span data-ttu-id="5ee51-128">既定値は "FALSE" です。</span><span class="sxs-lookup"><span data-stu-id="5ee51-128">The default is FALSE.</span></span>  <br/> |
|[<span data-ttu-id="5ee51-129">Default</span><span class="sxs-lookup"><span data-stu-id="5ee51-129">Default</span></span>](default-cell-hyperlinks-section.md) <br/> |<span data-ttu-id="5ee51-130">図形またはページに対する既定のハイパーリンクです。</span><span class="sxs-lookup"><span data-stu-id="5ee51-130">The default hyperlink for a shape or page.</span></span>  <br/> |
|[<span data-ttu-id="5ee51-131">非表示</span><span class="sxs-lookup"><span data-stu-id="5ee51-131">Invisible</span></span>](invisible-cell-hyperlinks-section.md) <br/> |<span data-ttu-id="5ee51-132">ハイパーリンクがショートカット メニューに表示されるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5ee51-132">Indicates whether the hyperlink appears on the shortcut menu.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ee51-133">注釈</span><span class="sxs-lookup"><span data-stu-id="5ee51-133">Remarks</span></span>

 <span data-ttu-id="5ee51-134">必要に応じて [Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="5ee51-134">You can add as many Hyperlink.</span></span>  <span data-ttu-id="5ee51-135">*必要に*  応じて行に名前を付け、行にわかりやすい名前を割り当て、セル値を設定します。</span><span class="sxs-lookup"><span data-stu-id="5ee51-135">*name*  rows as you need, assign meaningful names to the rows, and set cell values.</span></span> <span data-ttu-id="5ee51-136">既存の [Hyperlinks] セクションにハイパーリンクを追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ee51-136">To add hyperlinks to an existing Hyperlinks section, right-click a row and click **Insert Row** on the shortcut menu.</span></span> 
  
<span data-ttu-id="5ee51-137">これらのセルは行名で参照できます。これは、赤いテキストの ShapeSheet ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5ee51-137">You can reference these cells by their row name, which appears in a ShapeSheet window in red text.</span></span> <span data-ttu-id="5ee51-138">ハイパーリンクにわかりやすい名前を割り当てる。</span><span class="sxs-lookup"><span data-stu-id="5ee51-138">To assign meaningful names to Hyperlink.</span></span> <span data-ttu-id="5ee51-139">*行*  に名前を付け、行をクリックし、  *マーケティング*  などの名前を入力して、行名 Hyperlink.Marketing を作成します。</span><span class="sxs-lookup"><span data-stu-id="5ee51-139">*name*  rows, click the row, and then type a name such as  *Marketing*  , for example, to create the row name Hyperlink.Marketing.</span></span> <span data-ttu-id="5ee51-140">次に、Hyperlink.Marketing.Description を使用して [説明] セルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="5ee51-140">You can then reference the Description cell using Hyperlink.Marketing.Description.</span></span> 
  
<span data-ttu-id="5ee51-141">入力する行名は、セクション内で一意の名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ee51-141">The row name you enter must be unique within the section.</span></span>
  

