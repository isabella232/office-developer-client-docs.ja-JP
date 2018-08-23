---
title: '[BeginGroup] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: このアクションのメニューに区切り記号を挿入するかどうかを示します。
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804802"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="a04c0-103">[BeginGroup] セル ([操作] セクション)</span><span class="sxs-lookup"><span data-stu-id="a04c0-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="a04c0-104">このアクションのメニューに区切り記号を挿入するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a04c0-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="a04c0-105">**値**</span><span class="sxs-lookup"><span data-stu-id="a04c0-105">**Value**</span></span>|<span data-ttu-id="a04c0-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="a04c0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a04c0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a04c0-107">TRUE</span></span>  <br/> |<span data-ttu-id="a04c0-108">
          このアクションのメニューに区切り記号を挿入します。 
</span><span class="sxs-lookup"><span data-stu-id="a04c0-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="a04c0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a04c0-109">FALSE</span></span>  <br/> |<span data-ttu-id="a04c0-110">
          このアクションのメニューに区切り記号を挿入しません (既定値)。
</span><span class="sxs-lookup"><span data-stu-id="a04c0-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a04c0-111">注釈</span><span class="sxs-lookup"><span data-stu-id="a04c0-111">Remarks</span></span>

<span data-ttu-id="a04c0-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginGroup] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a04c0-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a04c0-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="a04c0-113">Cell name:</span></span>  <br/> |<span data-ttu-id="a04c0-114">アクションです。</span><span class="sxs-lookup"><span data-stu-id="a04c0-114">Actions.</span></span> <span data-ttu-id="a04c0-115">*名*です。BeginGroup で動作します。</span><span class="sxs-lookup"><span data-stu-id="a04c0-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="a04c0-116">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="a04c0-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="a04c0-117">プログラムから、インデックスによって [BeginGroup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a04c0-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a04c0-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a04c0-118">Section index:</span></span>  <br/> |<span data-ttu-id="a04c0-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a04c0-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a04c0-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a04c0-120">Row index:</span></span>  <br/> |<span data-ttu-id="a04c0-121">**visRowAction** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="a04c0-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a04c0-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a04c0-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a04c0-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="a04c0-123">**visActionBeginGroup**</span></span> <br/> |
   

