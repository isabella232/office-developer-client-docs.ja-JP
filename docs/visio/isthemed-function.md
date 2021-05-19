---
title: ISTHEMED 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: 図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。
ms.openlocfilehash: 49f53eaaacbdc86a633703d6ef847e38097f5122
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418121"
---
# <a name="isthemed-function"></a><span data-ttu-id="e8a72-103">ISTHEMED 関数</span><span class="sxs-lookup"><span data-stu-id="e8a72-103">ISTHEMED Function</span></span>

<span data-ttu-id="e8a72-104">図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。</span><span class="sxs-lookup"><span data-stu-id="e8a72-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="e8a72-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="e8a72-105">Version Information</span></span>

<span data-ttu-id="e8a72-106">追加バージョン: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="e8a72-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e8a72-107">構文</span><span class="sxs-lookup"><span data-stu-id="e8a72-107">Syntax</span></span>

 <span data-ttu-id="e8a72-108">**ISTHEMED**()</span><span class="sxs-lookup"><span data-stu-id="e8a72-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e8a72-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="e8a72-109">Return value</span></span>

<span data-ttu-id="e8a72-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="e8a72-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8a72-111">注釈</span><span class="sxs-lookup"><span data-stu-id="e8a72-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="e8a72-112">2013 年Visio **ISTHEMED** 関数は、以前のバージョンの **CELLISTHEMED** 関数を置き換Visio。</span><span class="sxs-lookup"><span data-stu-id="e8a72-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="e8a72-113">**ISTHEMED** 関数を使用すると、テーマの書式設定の適切な部分を図形に割り当て、テーマの書式設定の他の部分を手動で適用した書式で上書きする機能を保持できます。</span><span class="sxs-lookup"><span data-stu-id="e8a72-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="e8a72-114">その後テーマを再適用すると、手動で書式設定が上書きされ、図形がテーマのすべての書式設定を受け取る。</span><span class="sxs-lookup"><span data-stu-id="e8a72-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="e8a72-115">図形の [[ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md)] セルが 0 より大きい場合、**ISTHEMED** は TRUE と評価されます。</span><span class="sxs-lookup"><span data-stu-id="e8a72-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="e8a72-116">セルが 0 と等しい場合は、**ISTHEMED** は FALSE と評価されます。</span><span class="sxs-lookup"><span data-stu-id="e8a72-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="e8a72-117">DocumentSheet と PageSheet のテーマは、シェイプシートで使用される **ISTHEMED** 関数の値には影響しません。</span><span class="sxs-lookup"><span data-stu-id="e8a72-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="e8a72-118">**ISTHEMED** 関数が PageSheet に表示される場合にのみ、ページのテーマが重要になります。</span><span class="sxs-lookup"><span data-stu-id="e8a72-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e8a72-119">例</span><span class="sxs-lookup"><span data-stu-id="e8a72-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="e8a72-120">Cell</span><span class="sxs-lookup"><span data-stu-id="e8a72-120">Cell</span></span>  <br/> |<span data-ttu-id="e8a72-121">式</span><span class="sxs-lookup"><span data-stu-id="e8a72-121">Formula</span></span>  <br/> |<span data-ttu-id="e8a72-122">結果</span><span class="sxs-lookup"><span data-stu-id="e8a72-122">Result</span></span>  <br/> |
|<span data-ttu-id="e8a72-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="e8a72-123">Char.Font</span></span>  <br/> |<span data-ttu-id="e8a72-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="e8a72-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="e8a72-125">図形に適用されたテーマがある場合、図形のテキストはテーマのフォント書式設定を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="e8a72-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="e8a72-126">図形を使用しない場合、図形のテキストは "Calibri" フォントで書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="e8a72-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="e8a72-127">LineColor</span><span class="sxs-lookup"><span data-stu-id="e8a72-127">LineColor</span></span>  <br/> |<span data-ttu-id="e8a72-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="e8a72-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="e8a72-129">図形に色を適用している場合、図形の線の色は赤です。</span><span class="sxs-lookup"><span data-stu-id="e8a72-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="e8a72-130">図形を使用しない場合、図形の線の色は緑になります。</span><span class="sxs-lookup"><span data-stu-id="e8a72-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

