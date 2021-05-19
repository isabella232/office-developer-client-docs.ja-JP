---
title: '[PreviewScope] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: 図面にプレビューを含めるかどうかを指定します。図面にプレビューを含める場合は、プレビューに表示するページを指定します (最初のページのみ、または図面のすべてのページ)。
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426507"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="1dd74-104">[PreviewScope] セル ([Document Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="1dd74-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="1dd74-p102">図面にプレビューを含めるかどうかを指定します。図面にプレビューを含める場合は、プレビューに表示するページを指定します (最初のページのみ、または図面のすべてのページ)。</span><span class="sxs-lookup"><span data-stu-id="1dd74-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="1dd74-107">**値**</span><span class="sxs-lookup"><span data-stu-id="1dd74-107">**Value**</span></span>|<span data-ttu-id="1dd74-108">**プレビューの範囲**</span><span class="sxs-lookup"><span data-stu-id="1dd74-108">**Preview scope**</span></span>|<span data-ttu-id="1dd74-109">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="1dd74-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1dd74-110">0</span><span class="sxs-lookup"><span data-stu-id="1dd74-110">0</span></span>  <br/> | <span data-ttu-id="1dd74-111">最初のページ</span><span class="sxs-lookup"><span data-stu-id="1dd74-111">First page</span></span>  <br/> |<span data-ttu-id="1dd74-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="1dd74-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="1dd74-113">1</span><span class="sxs-lookup"><span data-stu-id="1dd74-113">1</span></span>  <br/> | <span data-ttu-id="1dd74-114">なし</span><span class="sxs-lookup"><span data-stu-id="1dd74-114">None</span></span>  <br/> |<span data-ttu-id="1dd74-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="1dd74-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="1dd74-116">2</span><span class="sxs-lookup"><span data-stu-id="1dd74-116">2</span></span>  <br/> | <span data-ttu-id="1dd74-117">すべてのページ</span><span class="sxs-lookup"><span data-stu-id="1dd74-117">All pages</span></span>  <br/> |<span data-ttu-id="1dd74-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="1dd74-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1dd74-119">注釈</span><span class="sxs-lookup"><span data-stu-id="1dd74-119">Remarks</span></span>

<span data-ttu-id="1dd74-120">この値は、[プロパティ] ダイアログボックスの [概要] タブで設定することもできます **([Office]** ボタンをクリックし、[情報] タブをクリックし、[ドキュメントのプロパティ] をクリックし、[詳細プロパティ] をクリック **します**)。</span><span class="sxs-lookup"><span data-stu-id="1dd74-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="1dd74-121">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PreviewScope] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1dd74-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1dd74-122">セル名:</span><span class="sxs-lookup"><span data-stu-id="1dd74-122">Cell name:</span></span>  <br/> | <span data-ttu-id="1dd74-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="1dd74-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="1dd74-124">プログラムから、インデックスによって [PreviewScope] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1dd74-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1dd74-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1dd74-125">Section index:</span></span>  <br/> |<span data-ttu-id="1dd74-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1dd74-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1dd74-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1dd74-127">Row index:</span></span>  <br/> |<span data-ttu-id="1dd74-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="1dd74-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="1dd74-129">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1dd74-129">Cell index:</span></span>  <br/> |<span data-ttu-id="1dd74-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="1dd74-130">**visDocPreviewScope**</span></span> <br/> |
   

