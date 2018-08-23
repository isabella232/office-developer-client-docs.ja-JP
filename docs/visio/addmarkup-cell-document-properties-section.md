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
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="30b93-103">[AddMarkup] セル ([ドキュメントのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="30b93-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="30b93-104">図面が校正履歴用にチェックされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="30b93-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="30b93-105">**値**</span><span class="sxs-lookup"><span data-stu-id="30b93-105">**Value**</span></span>|<span data-ttu-id="30b93-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="30b93-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30b93-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="30b93-107">TRUE</span></span>  <br/> |<span data-ttu-id="30b93-108">図面はチェックされています。</span><span class="sxs-lookup"><span data-stu-id="30b93-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="30b93-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="30b93-109">FALSE</span></span>  <br/> |<span data-ttu-id="30b93-110">図面はチェックされていません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="30b93-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30b93-111">注釈</span><span class="sxs-lookup"><span data-stu-id="30b93-111">Remarks</span></span>

<span data-ttu-id="30b93-112">AddMarkup セルが TRUE に設定、レビュー担当者は、元の図面ページに、マークアップ オーバーレイ ページに追加のマークアップと変更が適用されます。</span><span class="sxs-lookup"><span data-stu-id="30b93-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="30b93-113">[Addmarkup] セルが FALSE で、校正履歴の記録とオフは、変更元の図面ページに適用されます。</span><span class="sxs-lookup"><span data-stu-id="30b93-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="30b93-114">GUARD 関数を使用して、ドキュメントのマークアップを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="30b93-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="30b93-115">AddMarkup セルに数式が含まれている場合は = GUARD(FALSE)、校正履歴の**記録**を無効にします。</span><span class="sxs-lookup"><span data-stu-id="30b93-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="30b93-116">この設定は、[**校閲**] タブの [**校正履歴**] グループにある [**校正履歴の記録**] コマンドに相当します。</span><span class="sxs-lookup"><span data-stu-id="30b93-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="30b93-117">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AddMarkup] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="30b93-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30b93-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="30b93-118">Cell name:</span></span>  <br/> |<span data-ttu-id="30b93-119">[Addmarkup]</span><span class="sxs-lookup"><span data-stu-id="30b93-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="30b93-120">プログラムから、インデックスによって [AddMarkup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="30b93-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="30b93-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="30b93-121">Section index:</span></span>  <br/> |<span data-ttu-id="30b93-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="30b93-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="30b93-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="30b93-123">Row index:</span></span>  <br/> |<span data-ttu-id="30b93-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="30b93-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="30b93-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="30b93-125">Cell index:</span></span>  <br/> |<span data-ttu-id="30b93-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="30b93-126">**visDocAddMarkup**</span></span> <br/> |
   

