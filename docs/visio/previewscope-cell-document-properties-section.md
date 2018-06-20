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
ms.openlocfilehash: 865da052f710481c146d3c2692ddf506018be789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806098"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="7e8ac-104">[PreviewScope] セル ([Document Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="7e8ac-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="7e8ac-p102">図面にプレビューを含めるかどうかを指定します。図面にプレビューを含める場合は、プレビューに表示するページを指定します (最初のページのみ、または図面のすべてのページ)。</span><span class="sxs-lookup"><span data-stu-id="7e8ac-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="7e8ac-107">**値**</span><span class="sxs-lookup"><span data-stu-id="7e8ac-107">**Value**</span></span>|<span data-ttu-id="7e8ac-108">**プレビューの範囲**</span><span class="sxs-lookup"><span data-stu-id="7e8ac-108">**Preview scope**</span></span>|<span data-ttu-id="7e8ac-109">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="7e8ac-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7e8ac-110">0</span><span class="sxs-lookup"><span data-stu-id="7e8ac-110">0</span></span>  <br/> | <span data-ttu-id="7e8ac-111">最初のページ</span><span class="sxs-lookup"><span data-stu-id="7e8ac-111">First page</span></span>  <br/> |<span data-ttu-id="7e8ac-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="7e8ac-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="7e8ac-113">1</span><span class="sxs-lookup"><span data-stu-id="7e8ac-113">1</span></span>  <br/> | <span data-ttu-id="7e8ac-114">なし</span><span class="sxs-lookup"><span data-stu-id="7e8ac-114">None</span></span>  <br/> |<span data-ttu-id="7e8ac-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="7e8ac-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="7e8ac-116">2</span><span class="sxs-lookup"><span data-stu-id="7e8ac-116">2</span></span>  <br/> | <span data-ttu-id="7e8ac-117">すべてのページ</span><span class="sxs-lookup"><span data-stu-id="7e8ac-117">All pages</span></span>  <br/> |<span data-ttu-id="7e8ac-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="7e8ac-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e8ac-119">備考</span><span class="sxs-lookup"><span data-stu-id="7e8ac-119">Remarks</span></span>

<span data-ttu-id="7e8ac-120">[**概要**] タブ、[**プロパティ**] ダイアログ ボックスでこの値を設定することもできます ( **Office**ボタンをクリックして、[**情報**] タブをクリックして、**ドキュメントのプロパティ**] をクリックし、[**詳細プロパティ**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="7e8ac-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="7e8ac-121">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[PreviewScope] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="7e8ac-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e8ac-122">セル名:</span><span class="sxs-lookup"><span data-stu-id="7e8ac-122">Cell name:</span></span>  <br/> | <span data-ttu-id="7e8ac-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="7e8ac-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="7e8ac-124">プログラムから、インデックスによって [PreviewScope] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7e8ac-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7e8ac-125">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7e8ac-125">Section index:</span></span>  <br/> |<span data-ttu-id="7e8ac-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7e8ac-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7e8ac-127">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7e8ac-127">Row index:</span></span>  <br/> |<span data-ttu-id="7e8ac-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="7e8ac-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="7e8ac-129">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7e8ac-129">Cell index:</span></span>  <br/> |<span data-ttu-id="7e8ac-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="7e8ac-130">**visDocPreviewScope**</span></span> <br/> |
   

