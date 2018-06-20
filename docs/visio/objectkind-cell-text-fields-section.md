---
title: '[ObjectKind] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: テキスト フィールドの種類を示します。
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805929"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="13f58-103">[ObjectKind] セル ([Text Fields] セクション)</span><span class="sxs-lookup"><span data-stu-id="13f58-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="13f58-104">テキスト フィールドの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="13f58-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="13f58-105">**値**</span><span class="sxs-lookup"><span data-stu-id="13f58-105">**Value**</span></span>|<span data-ttu-id="13f58-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="13f58-106">**Description**</span></span>|<span data-ttu-id="13f58-107">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="13f58-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="13f58-108">0</span><span class="sxs-lookup"><span data-stu-id="13f58-108">0</span></span>  <br/> | <span data-ttu-id="13f58-109">標準</span><span class="sxs-lookup"><span data-stu-id="13f58-109">Standard</span></span>  <br/> |<span data-ttu-id="13f58-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="13f58-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="13f58-111">1</span><span class="sxs-lookup"><span data-stu-id="13f58-111">1</span></span>  <br/> |<span data-ttu-id="13f58-112">縦中横</span><span class="sxs-lookup"><span data-stu-id="13f58-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="13f58-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="13f58-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13f58-114">備考</span><span class="sxs-lookup"><span data-stu-id="13f58-114">Remarks</span></span>

<span data-ttu-id="13f58-115">テキスト フィールドは、次のいずれかの種類に該当します。</span><span class="sxs-lookup"><span data-stu-id="13f58-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="13f58-116">標準 : フィールド カテゴリ別に挿入された横書きテキストであることを示すフィールドです。</span><span class="sxs-lookup"><span data-stu-id="13f58-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="13f58-117">縦中横 : 縦書きテキストの内部に設定された横書きテキストであることを示すフィールドです。</span><span class="sxs-lookup"><span data-stu-id="13f58-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="13f58-118">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ObjectKind] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="13f58-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13f58-119">セル名:</span><span class="sxs-lookup"><span data-stu-id="13f58-119">Cell name:</span></span>  <br/> | <span data-ttu-id="13f58-120">Fields.ObjectKind [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="13f58-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="13f58-121">プログラムから、インデックスによって [ObjectKind] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="13f58-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13f58-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="13f58-122">Section index:</span></span>  <br/> |<span data-ttu-id="13f58-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="13f58-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="13f58-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="13f58-124">Row index:</span></span>  <br/> |<span data-ttu-id="13f58-125">**visRowField** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="13f58-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="13f58-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="13f58-126">Cell index:</span></span>  <br/> |<span data-ttu-id="13f58-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="13f58-127">**visFieldObjectKind**</span></span> <br/> |
   

