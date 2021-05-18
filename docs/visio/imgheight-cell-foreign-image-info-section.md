---
title: '[ImgHeight] セル ([Foreign Image Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm445
localization_priority: Normal
ms.assetid: decb86a4-b711-35e1-b9dc-744a84ee177c
description: 枠内におけるオブジェクトのイメージの高さを指定します。既定の数式は次のとおりです。
ms.openlocfilehash: 956bc478604fd19d8dfdbb7079e092e9e8a16e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411198"
---
# <a name="imgheight-cell-foreign-image-info-section"></a><span data-ttu-id="c760b-104">[ImgHeight] セル ([Foreign Image Info] セクション)</span><span class="sxs-lookup"><span data-stu-id="c760b-104">ImgHeight Cell (Foreign Image Info Section)</span></span>

<span data-ttu-id="c760b-p102">枠内におけるオブジェクトのイメージの高さを指定します。既定の数式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c760b-p102">Determines the height of the object's image within its border. The default formula is:</span></span>
  
<span data-ttu-id="c760b-107">= 高 \* さ 1</span><span class="sxs-lookup"><span data-stu-id="c760b-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c760b-108">注釈</span><span class="sxs-lookup"><span data-stu-id="c760b-108">Remarks</span></span>

<span data-ttu-id="c760b-109">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ImgHeight] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c760b-109">To get a reference to the ImgHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c760b-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="c760b-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c760b-111">ImgHeight</span><span class="sxs-lookup"><span data-stu-id="c760b-111">ImgHeight</span></span>  <br/> |
   
<span data-ttu-id="c760b-112">プログラムから、インデックスによって [ImgHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c760b-112">To get a reference to the ImgHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c760b-113">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c760b-113">Section index:</span></span>  <br/> |<span data-ttu-id="c760b-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c760b-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c760b-115">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c760b-115">Row index:</span></span>  <br/> |<span data-ttu-id="c760b-116">**visRowForeign**</span><span class="sxs-lookup"><span data-stu-id="c760b-116">**visRowForeign**</span></span> <br/> |
| <span data-ttu-id="c760b-117">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c760b-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c760b-118">**visFrgnImgHeight**</span><span class="sxs-lookup"><span data-stu-id="c760b-118">**visFrgnImgHeight**</span></span> <br/> |
   

