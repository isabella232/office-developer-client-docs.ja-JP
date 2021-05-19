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
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427634"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="1a695-103">[AddMarkup] セル ([Document Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="1a695-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="1a695-104">図面が校正履歴用にチェックされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="1a695-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="1a695-105">**値**</span><span class="sxs-lookup"><span data-stu-id="1a695-105">**Value**</span></span>|<span data-ttu-id="1a695-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="1a695-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a695-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="1a695-107">TRUE</span></span>  <br/> |<span data-ttu-id="1a695-108">図面はチェックされています。</span><span class="sxs-lookup"><span data-stu-id="1a695-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="1a695-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="1a695-109">FALSE</span></span>  <br/> |<span data-ttu-id="1a695-110">図面はチェックされていません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="1a695-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a695-111">注釈</span><span class="sxs-lookup"><span data-stu-id="1a695-111">Remarks</span></span>

<span data-ttu-id="1a695-112">AddMarkup セルが TRUE に設定されている場合、校閲者が校正履歴を追加しており、変更はオリジナルの図面ページではなく校正履歴のオーバーレイ ページに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1a695-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="1a695-113">AddMarkup セルが FALSE に設定されている場合、校正履歴の記録はオフになっており、変更はオリジナルの図面ページに適用されます。</span><span class="sxs-lookup"><span data-stu-id="1a695-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1a695-114">GUARD 関数を使用すると、ドキュメントのマークアップを防止できます。</span><span class="sxs-lookup"><span data-stu-id="1a695-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="1a695-115">[AddMarkup] セルに数式 =GUARD(FALSE) が含まれている場合、[マークアップの追跡] **コマンドは** 無効になります。</span><span class="sxs-lookup"><span data-stu-id="1a695-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="1a695-116">この設定は、[**校閲**] タブの [**校正履歴**] グループにある [**校正履歴の記録**] コマンドに相当します。</span><span class="sxs-lookup"><span data-stu-id="1a695-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="1a695-117">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AddMarkup] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1a695-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a695-118">セル名:</span><span class="sxs-lookup"><span data-stu-id="1a695-118">Cell name:</span></span>  <br/> |<span data-ttu-id="1a695-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="1a695-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="1a695-120">プログラムから、インデックスによって [AddMarkup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1a695-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1a695-121">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="1a695-121">Section index:</span></span>  <br/> |<span data-ttu-id="1a695-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1a695-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1a695-123">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="1a695-123">Row index:</span></span>  <br/> |<span data-ttu-id="1a695-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="1a695-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="1a695-125">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="1a695-125">Cell index:</span></span>  <br/> |<span data-ttu-id="1a695-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="1a695-126">**visDocAddMarkup**</span></span> <br/> |
   

