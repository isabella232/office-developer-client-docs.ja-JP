---
title: '[EnableTextProps] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
localization_priority: Normal
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: スタイルにテキストのプロパティを含めるかどうかを指定します。
ms.openlocfilehash: a51f83624192615e84292129d4788ae1e2779c6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805306"
---
# <a name="enabletextprops-cell-style-properties-section"></a><span data-ttu-id="c25fc-103">[EnableTextProps] セル ([Style Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="c25fc-103">EnableTextProps Cell (Style Properties Section)</span></span>

<span data-ttu-id="c25fc-104">スタイルにテキストのプロパティを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c25fc-104">Determines whether a style includes text properties.</span></span>
  
|<span data-ttu-id="c25fc-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c25fc-105">**Value**</span></span>|<span data-ttu-id="c25fc-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="c25fc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c25fc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c25fc-107">TRUE</span></span>  <br/> |<span data-ttu-id="c25fc-108">テキストのプロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="c25fc-108">Include text properties.</span></span>  <br/> |
|<span data-ttu-id="c25fc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c25fc-109">FALSE</span></span>  <br/> |<span data-ttu-id="c25fc-110">テキストのプロパティを含めません。</span><span class="sxs-lookup"><span data-stu-id="c25fc-110">Exclude text properties.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c25fc-111">注釈</span><span class="sxs-lookup"><span data-stu-id="c25fc-111">Remarks</span></span>

<span data-ttu-id="c25fc-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[EnableTextProps] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="c25fc-112">To get a reference to the EnableTextProps cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c25fc-113">セル名 :</span><span class="sxs-lookup"><span data-stu-id="c25fc-113">Cell name:</span></span>  <br/> |<span data-ttu-id="c25fc-114">EnableTextProps</span><span class="sxs-lookup"><span data-stu-id="c25fc-114">EnableTextProps</span></span>  <br/> |
   
<span data-ttu-id="c25fc-115">プログラムから、インデックスによって [EnableTextProps] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c25fc-115">To get a reference to the EnableTextProps cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c25fc-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c25fc-116">Section index:</span></span>  <br/> |<span data-ttu-id="c25fc-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c25fc-117">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c25fc-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c25fc-118">Row index:</span></span>  <br/> |<span data-ttu-id="c25fc-119">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="c25fc-119">**visRowStyle**</span></span> <br/> |
|<span data-ttu-id="c25fc-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c25fc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c25fc-121">**visStyleIncludesText**</span><span class="sxs-lookup"><span data-stu-id="c25fc-121">**visStyleIncludesText**</span></span> <br/> |
   

