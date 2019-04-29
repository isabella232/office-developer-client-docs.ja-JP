---
title: '[Checked] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438331"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="6624e-103">[Checked] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="6624e-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="6624e-104">ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="6624e-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6624e-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="6624e-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="6624e-106">**値**</span><span class="sxs-lookup"><span data-stu-id="6624e-106">**Value**</span></span>|<span data-ttu-id="6624e-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="6624e-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6624e-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="6624e-108">TRUE</span></span>  <br/> |<span data-ttu-id="6624e-109">チェック マークが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6624e-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="6624e-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="6624e-110">FALSE</span></span>  <br/> |<span data-ttu-id="6624e-111">チェック マークが表示されません (既定値)。</span><span class="sxs-lookup"><span data-stu-id="6624e-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6624e-112">注釈</span><span class="sxs-lookup"><span data-stu-id="6624e-112">Remarks</span></span>

<span data-ttu-id="6624e-113">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Checked] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6624e-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6624e-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="6624e-114">Cell name:</span></span>  <br/> |<span data-ttu-id="6624e-115">アクション.</span><span class="sxs-lookup"><span data-stu-id="6624e-115">Actions.</span></span> <span data-ttu-id="6624e-116">*名前*です。アクションを確認しました。</span><span class="sxs-lookup"><span data-stu-id="6624e-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="6624e-117">*name*は、Actions 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="6624e-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="6624e-118">プログラムから、インデックスによって [Checked] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6624e-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6624e-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6624e-119">Section index:</span></span>  <br/> |<span data-ttu-id="6624e-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="6624e-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="6624e-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6624e-121">Row index:</span></span>  <br/> |<span data-ttu-id="6624e-122">**visRowAction** +  *i* = \*\* 0、1、2、...</span><span class="sxs-lookup"><span data-stu-id="6624e-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="6624e-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6624e-123">Cell index:</span></span>  <br/> |<span data-ttu-id="6624e-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="6624e-124">**visActionChecked**</span></span> <br/> |
   

