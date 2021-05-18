---
title: '[Y Dynamics] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: コントロール ハンドルのアンカー ポイントの y 座標をローカル座標で表します。 アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404828"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="356f8-104">[Y Dynamics] セル ([Controls] セクション)</span><span class="sxs-lookup"><span data-stu-id="356f8-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="356f8-105">コントロール ハンドル  *のアンカー ポイントの y*  座標をローカル座標で表します。</span><span class="sxs-lookup"><span data-stu-id="356f8-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="356f8-106">アンカー ポイントは、ダイナミックス機能を使うときのラバーバンディングに使用されます。</span><span class="sxs-lookup"><span data-stu-id="356f8-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="356f8-107">注釈</span><span class="sxs-lookup"><span data-stu-id="356f8-107">Remarks</span></span>

<span data-ttu-id="356f8-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Dynamics] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="356f8-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="356f8-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="356f8-109">Cell name:</span></span>  <br/> | <span data-ttu-id="356f8-110">コントロール。</span><span class="sxs-lookup"><span data-stu-id="356f8-110">Controls.</span></span>  <span data-ttu-id="356f8-111">*name*  .YDynwhere コントロール。</span><span class="sxs-lookup"><span data-stu-id="356f8-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="356f8-112">*name*  は、コントロール行の名前です。</span><span class="sxs-lookup"><span data-stu-id="356f8-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="356f8-113">プログラムから、インデックスによって [Y Dynamics] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="356f8-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="356f8-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="356f8-114">Section index:</span></span>  <br/> |<span data-ttu-id="356f8-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="356f8-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="356f8-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="356f8-116">Row index:</span></span>  <br/> |<span data-ttu-id="356f8-117">**visRowControl**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="356f8-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="356f8-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="356f8-118">Cell index:</span></span>  <br/> |<span data-ttu-id="356f8-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="356f8-119">**visCtlYDyn**</span></span> <br/> |
   

