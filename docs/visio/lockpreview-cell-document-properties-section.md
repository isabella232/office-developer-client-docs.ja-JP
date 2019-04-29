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
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418863"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="9da4f-103">[LockPreview] セル ([Document Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="9da4f-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="9da4f-104">図面を保存するたびにプレビューを保存するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="9da4f-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="9da4f-105">**値**</span><span class="sxs-lookup"><span data-stu-id="9da4f-105">**Value**</span></span>|<span data-ttu-id="9da4f-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="9da4f-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9da4f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9da4f-107">TRUE</span></span>  <br/> | <span data-ttu-id="9da4f-108">図面を保存するたびにプレビューを保存しません。</span><span class="sxs-lookup"><span data-stu-id="9da4f-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="9da4f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9da4f-109">FALSE</span></span>  <br/> | <span data-ttu-id="9da4f-110">図面を保存するたびにプレビューを保存します。</span><span class="sxs-lookup"><span data-stu-id="9da4f-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9da4f-111">注釈</span><span class="sxs-lookup"><span data-stu-id="9da4f-111">Remarks</span></span>

<span data-ttu-id="9da4f-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockPreview] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9da4f-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9da4f-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="9da4f-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9da4f-114">[lockpreview]</span><span class="sxs-lookup"><span data-stu-id="9da4f-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="9da4f-115">プログラムから、インデックスによって [LockPreview] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9da4f-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9da4f-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9da4f-116">Section index:</span></span>  <br/> |<span data-ttu-id="9da4f-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9da4f-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9da4f-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9da4f-118">Row index:</span></span>  <br/> |<span data-ttu-id="9da4f-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="9da4f-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="9da4f-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9da4f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9da4f-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="9da4f-121">**visDocLockPreview**</span></span> <br/> |
   

