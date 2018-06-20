---
title: '[LockPreview] セル ([Document Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: 図面を保存するたびにプレビューを保存するかどうかを指定します。
ms.openlocfilehash: 2ef5ea12669a7a6a2b37d599afd24635f7509ac2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805765"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="510ef-103">[LockPreview] セル ([Document Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="510ef-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="510ef-104">図面を保存するたびにプレビューを保存するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="510ef-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="510ef-105">**値**</span><span class="sxs-lookup"><span data-stu-id="510ef-105">**Value**</span></span>|<span data-ttu-id="510ef-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="510ef-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="510ef-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="510ef-107">TRUE</span></span>  <br/> | <span data-ttu-id="510ef-108">図面を保存するたびにプレビューを保存しません。</span><span class="sxs-lookup"><span data-stu-id="510ef-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="510ef-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="510ef-109">FALSE</span></span>  <br/> | <span data-ttu-id="510ef-110">図面を保存するたびにプレビューを保存します。</span><span class="sxs-lookup"><span data-stu-id="510ef-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="510ef-111">備考</span><span class="sxs-lookup"><span data-stu-id="510ef-111">Remarks</span></span>

<span data-ttu-id="510ef-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockPreview] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="510ef-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="510ef-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="510ef-113">Cell name:</span></span>  <br/> | <span data-ttu-id="510ef-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="510ef-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="510ef-115">プログラムから、インデックスによって [LockPreview] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="510ef-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="510ef-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="510ef-116">Section index:</span></span>  <br/> |<span data-ttu-id="510ef-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="510ef-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="510ef-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="510ef-118">Row index:</span></span>  <br/> |<span data-ttu-id="510ef-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="510ef-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="510ef-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="510ef-120">Cell index:</span></span>  <br/> |<span data-ttu-id="510ef-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="510ef-121">**visDocLockPreview**</span></span> <br/> |
   

