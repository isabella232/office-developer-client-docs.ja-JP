---
title: ISTHEMED 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 91cde601-dca9-4737-afe1-bdf76638dfe3
description: 図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。
ms.openlocfilehash: 4311780d8686b5792e999c204ec182d23efb723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805646"
---
# <a name="isthemed-function"></a><span data-ttu-id="ced2e-103">ISTHEMED 関数</span><span class="sxs-lookup"><span data-stu-id="ced2e-103">ISTHEMED Function</span></span>

<span data-ttu-id="ced2e-104">図形に適用するテーマがあるかどうかを示すブール演算型の値を返します。</span><span class="sxs-lookup"><span data-stu-id="ced2e-104">Returns a Boolean value indicating whether a shape has a theme applied to it.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="ced2e-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="ced2e-105">Version Information</span></span>

<span data-ttu-id="ced2e-106">Visio 2013 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="ced2e-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ced2e-107">構文</span><span class="sxs-lookup"><span data-stu-id="ced2e-107">Syntax</span></span>

 <span data-ttu-id="ced2e-108">**ISTHEMED**()</span><span class="sxs-lookup"><span data-stu-id="ced2e-108">**ISTHEMED**()</span></span>
  
## <a name="return-value"></a><span data-ttu-id="ced2e-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ced2e-109">Return value</span></span>

<span data-ttu-id="ced2e-110">ブール型</span><span class="sxs-lookup"><span data-stu-id="ced2e-110">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ced2e-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="ced2e-111">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="ced2e-112">Visio 2013 には、 **ISTHEMED**関数は、Visio の以前のバージョンから**CELLISTHEMED**関数を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="ced2e-112">The **ISTHEMED** function in Visio 2013 replaces the **CELLISTHEMED** function from previous versions of Visio.</span></span> 
  
<span data-ttu-id="ced2e-113">**ISTHEMED**はテーマの書式設定の適切な部分を図形に割り当てることで機能しますが、テーマの書式を手動で適用される書式の他の部分を上書きする機能を保持します。</span><span class="sxs-lookup"><span data-stu-id="ced2e-113">The **ISTHEMED** function lets you assign appropriate parts of a theme's formatting to a shape but retain the ability to override other parts of the theme formatting with manually-applied formatting.</span></span> <span data-ttu-id="ced2e-114">後でテーマを再適用する場合手動で書式設定がオーバーライドされ、図形にはテーマの書式設定のすべて。</span><span class="sxs-lookup"><span data-stu-id="ced2e-114">If you subsequently reapply the theme, any manual formatting is overridden and the shape takes on all of the theme's formatting.</span></span> 
  
 <span data-ttu-id="ced2e-115">**ISTHEMED**は、図形内の[ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md)セルが 0 より大きい場合は TRUE に評価されます。</span><span class="sxs-lookup"><span data-stu-id="ced2e-115">**ISTHEMED** evaluates to TRUE if the [ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) cell in the shape is greater than 0.</span></span> <span data-ttu-id="ced2e-116">このセルが 0 の場合は、 **ISTHEMED**を評価し、false を指定します。</span><span class="sxs-lookup"><span data-stu-id="ced2e-116">If this cell is equal to 0, then **ISTHEMED** evaluates to FALSE.</span></span> <span data-ttu-id="ced2e-117">DocumentSheet と PageSheet のテーマは、シェイプ シートで使用する**ISTHEMED**関数の値に影響はありません。</span><span class="sxs-lookup"><span data-stu-id="ced2e-117">The theme of the DocumentSheet and PageSheet won't affect the value of the **ISTHEMED** function used in a ShapeSheet.</span></span> <span data-ttu-id="ced2e-118">**ISTHEMED**関数が表示される場合にのみ、PageSheet はページのテーマだけにします。</span><span class="sxs-lookup"><span data-stu-id="ced2e-118">Only if the **ISTHEMED** function shows up in the PageSheet does the page's theme matter.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ced2e-119">次の使用例では、テーブルからレコードを削除できないようにします。</span><span class="sxs-lookup"><span data-stu-id="ced2e-119">Example</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="ced2e-120">セル</span><span class="sxs-lookup"><span data-stu-id="ced2e-120">Cell</span></span>  <br/> |<span data-ttu-id="ced2e-121">Formula</span><span class="sxs-lookup"><span data-stu-id="ced2e-121">Formula</span></span>  <br/> |<span data-ttu-id="ced2e-122">結果</span><span class="sxs-lookup"><span data-stu-id="ced2e-122">Result</span></span>  <br/> |
|<span data-ttu-id="ced2e-123">Char.Font</span><span class="sxs-lookup"><span data-stu-id="ced2e-123">Char.Font</span></span>  <br/> |<span data-ttu-id="ced2e-124">IF(ISTHEMED()、THEMEVAL()、FONT("Calibri"))</span><span class="sxs-lookup"><span data-stu-id="ced2e-124">IF(ISTHEMED(), THEMEVAL(), FONT("Calibri"))</span></span>  <br/> |<span data-ttu-id="ced2e-125">図形にテーマを適用する場合、図形のテキストは、テーマのフォントを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="ced2e-125">If the shape has a themed applied to it, the shape text accepts the font formatting from the theme.</span></span> <span data-ttu-id="ced2e-126">図形がテーマではない場合は、「Calibri」フォントを使用して図形のテキストが書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="ced2e-126">If the shape is not themed, the shape text is formatted with the "Calibri" font.</span></span>  <br/> |
|<span data-ttu-id="ced2e-127">線の色</span><span class="sxs-lookup"><span data-stu-id="ced2e-127">LineColor</span></span>  <br/> |<span data-ttu-id="ced2e-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span><span class="sxs-lookup"><span data-stu-id="ced2e-128">IF(ISTHEMED, RGB(255, 0, 0), RGB(0, 255, 0))</span></span>  <br/> |<span data-ttu-id="ced2e-129">図形にテーマを適用する場合、図形の線の色は赤色です。</span><span class="sxs-lookup"><span data-stu-id="ced2e-129">If the shape has a themed applied to it, the shape's line color is red.</span></span> <span data-ttu-id="ced2e-130">図形がテーマではない場合は、図形の線の色は緑です。</span><span class="sxs-lookup"><span data-stu-id="ced2e-130">If the shape is not themed, the shape's line color is green.</span></span>  <br/> |
   

