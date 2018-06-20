---
title: '[AddMarkup] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: 図面が校正履歴用にチェックされているかどうかを示します。
ms.openlocfilehash: 69430122b0a7665d7daa4a6b28f3a51745b74473
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804776"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="ac68d-103">[AddMarkup] セル ([Document Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="ac68d-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="ac68d-104">図面が校正履歴用にチェックされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ac68d-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="ac68d-105">**値**</span><span class="sxs-lookup"><span data-stu-id="ac68d-105">**Value**</span></span>|<span data-ttu-id="ac68d-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="ac68d-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ac68d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ac68d-107">TRUE</span></span>  <br/> |<span data-ttu-id="ac68d-108">図面はチェックされています。</span><span class="sxs-lookup"><span data-stu-id="ac68d-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="ac68d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ac68d-109">FALSE</span></span>  <br/> |<span data-ttu-id="ac68d-110">図面はチェックされていません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="ac68d-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac68d-111">注釈</span><span class="sxs-lookup"><span data-stu-id="ac68d-111">Remarks</span></span>

<span data-ttu-id="ac68d-112">AddMarkup セルが TRUE に設定、レビュー担当者は、元の図面ページに、マークアップ オーバーレイ ページに追加のマークアップと変更が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ac68d-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="ac68d-113">[Addmarkup] セルが FALSE で、校正履歴の記録とオフは、変更元の図面ページに適用されます。</span><span class="sxs-lookup"><span data-stu-id="ac68d-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ac68d-114">GUARD 関数を使用して、ドキュメントのマークアップを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="ac68d-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="ac68d-115">AddMarkup セルに数式が含まれている場合は = GUARD(FALSE)、校正履歴の**記録**を無効にします。</span><span class="sxs-lookup"><span data-stu-id="ac68d-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="ac68d-116">この設定は、[**校閲**] タブには、**マークアップ**のグループで**校正履歴の記録**] コマンドの設定に対応します。</span><span class="sxs-lookup"><span data-stu-id="ac68d-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="ac68d-117">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [addmarkup] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="ac68d-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac68d-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="ac68d-118">Cell name:</span></span>  <br/> |<span data-ttu-id="ac68d-119">[Addmarkup]</span><span class="sxs-lookup"><span data-stu-id="ac68d-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="ac68d-120">プログラムから、インデックスによって [addmarkup] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="ac68d-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac68d-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="ac68d-121">Section index:</span></span>  <br/> |<span data-ttu-id="ac68d-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ac68d-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ac68d-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="ac68d-123">Row index:</span></span>  <br/> |<span data-ttu-id="ac68d-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="ac68d-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="ac68d-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="ac68d-125">Cell index:</span></span>  <br/> |<span data-ttu-id="ac68d-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="ac68d-126">**visDocAddMarkup**</span></span> <br/> |
   

