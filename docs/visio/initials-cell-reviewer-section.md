---
title: '[Initials] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: 図面の校閲者の頭文字を格納します。
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411506"
---
# <a name="initials-cell-reviewer-section"></a><span data-ttu-id="8628e-103">[Initials] セル ([Reviewer] セクション)</span><span class="sxs-lookup"><span data-stu-id="8628e-103">Initials Cell (Reviewer Section)</span></span>

<span data-ttu-id="8628e-104">図面の校閲者の頭文字を格納します。</span><span class="sxs-lookup"><span data-stu-id="8628e-104">Contains the initials of a document reviewer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8628e-105">注釈</span><span class="sxs-lookup"><span data-stu-id="8628e-105">Remarks</span></span>

<span data-ttu-id="8628e-106">この値の既定値は、[ \*\*\*\* **Visio のオプション**] ダイアログボックス ([**ファイル**] タブをクリックし、[**オプション**] をクリックし、[**全般**] をクリックします) の [**全般**] タブの [イニシャル] ボックスに設定されています。</span><span class="sxs-lookup"><span data-stu-id="8628e-106">This value defaults to the initials in the **Initials** box on the **General** tab in the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **General** ).</span></span> 
  
<span data-ttu-id="8628e-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Initials] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="8628e-107">To get a reference to the Initials cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8628e-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="8628e-108">Cell name:</span></span>  <br/> | <span data-ttu-id="8628e-109">レビューアー [ *i* ] *i* = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="8628e-109">Reviewer.Initials [  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8628e-110">プログラムから、インデックスによって [Initials] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8628e-110">To get a reference to the Initials cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8628e-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="8628e-111">Section index:</span></span>  <br/> |<span data-ttu-id="8628e-112">**visSectionReviewer**</span><span class="sxs-lookup"><span data-stu-id="8628e-112">**visSectionReviewer**</span></span> <br/> |
| <span data-ttu-id="8628e-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="8628e-113">Row index:</span></span>  <br/> |<span data-ttu-id="8628e-114">**visRowReviewer** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="8628e-114">**visRowReviewer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8628e-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="8628e-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8628e-116">**visReviewerInitials**</span><span class="sxs-lookup"><span data-stu-id="8628e-116">**visReviewerInitials**</span></span> <br/> |
   

